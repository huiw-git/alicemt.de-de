---
title: "Herstellen einer Verbindung mit einer Azure SQL-Datenbank"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 49645b1f-39b1-4757-bda1-c51ebc375c34
caps.latest.revision: 18
caps.handback.revision: 13
manager: jhubbard
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pt-br
  - ru-ru
  - sv-se
  - zh-cn
  - zh-tw
---
# Herstellen einer Verbindung mit einer Azure SQL-Datenbank
  In diesem Thema werden Probleme behandelt, die auftreten können, wenn über den [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] eine Verbindung mit einer [!INCLUDE[ssAzure](../content/includes/ssAzure_md.md)] hergestellt wird. Weitere Informationen zur Verbindung mit einer [!INCLUDE[ssAzure](../content/includes/ssAzure_md.md)] finden Sie unter:  
  
-   [SQL Azure\-Datenbank](http://go.microsoft.com/fwlink/?LinkID=202490)  
  
-   [Vorgehensweise: Herstellen einer Verbindung mit SQL Azure mithilfe von JDBC](http://msdn.microsoft.com/library/gg715284.aspx)  
  
-   [Verwenden von SQL Azure in Java](http://msdn.microsoft.com/library/windowsazure/hh749029(VS.103).aspx)  
  
## Details  
 Bei der Verbindung mit einer [!INCLUDE[ssAzure](../content/includes/ssAzure_md.md)] sollten Sie eine Verbindung mit der Masterdatenbank herstellen, um **SQLServerDatabaseMetaData.getCatalogs** aufzurufen.  
 Die Rückgabe sämtlicher Kataloge aus einer Benutzerdatenbank wird von einer [!INCLUDE[ssAzure](../content/includes/ssAzure_md.md)] nicht unterstützt.**SQLServerDatabaseMetaData.getCatalogs** verwendet die sys.databases\-Sicht, um die Kataloge abzurufen. Lesen Sie die Beschreibung zu den Berechtigungen unter [sys.databases \(SQL Azure\-Datenbank\)](http://go.microsoft.com/fwlink/?LinkId=217396), um sich mit dem **SQLServerDatabaseMetaData.getCatalogs**\-Verhalten für eine [!INCLUDE[ssAzure](../content/includes/ssAzure_md.md)] vertraut zu machen.  
  
 Getrennte Verbindungen  
 Bei der Verbindung mit einer [!INCLUDE[ssAzure](../content/includes/ssAzure_md.md)] können Verbindungen im Leerlauf nach einer Phase ohne Aktivität durch eine Netzwerkkomponente \(z. B. eine Firewall\) getrennt werden. In diesem Kontext werden zwei Arten von inaktiven Verbindungen behandelt:  
  
-   Inaktive Verbindungen auf der TCP\-Ebene, wobei Verbindungen von einer beliebigen Anzahl von Netzwerkgeräten gelöscht werden können.  
  
-   Durch das SQL Azure\-Gateway ermittelte, inaktive Verbindungen. Dabei kann TCP **keepalive**\-Meldungen ausgeben \(wodurch sie aus TCP\-Sicht nicht inaktiv sind\), über die jedoch in den letzten 30 Minuten keine aktive Abfrage ausgeführt wurde. In diesem Szenario wird durch das Gateway ermittelt, ob die TDS\-Verbindung 30 Minuten inaktiv war, und die Verbindung wird beendet.  
  
 Um zu vermeiden, dass Verbindungen im Leerlauf durch eine Netzwerkkomponente getrennt werden, sollten die folgenden Registrierungseinstellungen \(bzw. deren Nicht\-Windows\-Äquivalente\) für das Betriebssystem festgelegt werden, unter dem der Treiber geladen wurde:  
  
|Registrierungseinstellung|Empfohlener Wert|  
|-------------------------------|----------------------|  
|HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\Tcpip\\Parameters\\KeepAliveTime|30000|  
|HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\Tcpip\\Parameters\\KeepAliveInterval|1000|  
|HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\Tcpip\\Parameters\\TcpMaxDataRetransmission|10|  
  
 Anschließend müssen Sie den Computer neu starten, damit die Registrierungseinstellungen wirksam werden.  
  
 Um diese Aktion in Windows Azure auszuführen, erstellen Sie einen Starttask, durch den die Registrierungsschlüssel hinzugefügt werden.  Fügen Sie der Dienstdefinitionsdatei beispielsweise folgenden Starttask hinzu:  
  
```  
<Startup>  
    <Task commandLine="AddKeepAlive.cmd" executionContext="elevated" taskType="simple">  
    </Task>  
</Startup>  
```  
  
 Fügen Sie dem Projekt anschließend die Datei „AddKeepAlive.cmd“ hinzu. Legen Sie die Einstellung „In Ausgabeverzeichnis kopieren“ auf „Immer kopieren“ fest. Das folgende Beispiel veranschaulicht eine Datei „AddKeepAlive.cmd“:  
  
```  
if exist keepalive.txt goto done  
time /t > keepalive.txt  
REM Workaround for JDBC keep alive on SQL Azure  
REG ADD HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters /v KeepAliveTime /t REG_DWORD /d 30000 >> keepalive.txt  
REG ADD HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters /v KeepAliveInterval /t REG_DWORD /d 1000 >> keepalive.txt  
REG ADD HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters /v TcpMaxDataRetransmission /t REG_DWORD /d 10 >> keepalive.txt  
shutdown /r /t 1  
:done  
```  
  
 Anfügen des Servernamens an die UserId in der Verbindungszeichenfolge  
 Vor [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)], Version 4.0, war es bei der Verbindung mit einer [!INCLUDE[ssAzure](../content/includes/ssAzure_md.md)] erforderlich, den Servernamen an die UserId in der Verbindungszeichenfolge anzufügen. z. B. „Benutzer@Servername“. Ab [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)], Version 4.0, muss "@Servername" nicht mehr an die UserId in der Verbindungszeichenfolge angefügt werden.  
  
 Einstellung "hostNameInCertificate" zur Verwendung der Verschlüsselung erforderlich  
 Bei der Verbindung mit einer [!INCLUDE[ssAzure](../content/includes/ssAzure_md.md)] sollte auch **hostNameInCertificate** angegeben werden, wenn **encrypt\=true** festgelegt ist. \(Wenn der Servername in der Verbindungszeichenfolge *shortName*.*domainName* lautet, legen Sie die **hostNameInCertificate**\-Eigenschaft auf \*.*domainName* fest.\)  
  
 Beispiel:  
  
```  
jdbc:sqlserver://abcd.int.mscds.com;databaseName= myDatabase;user=myName;password=myPassword;encrypt=true;hostNameInCertificate= *.int.mscds.com;  
```  
  
## Siehe auch  
 [Verbinden von SQL Server mit dem JDBC-Treiber](../content/Connecting-to-SQL-Server-with-the-JDBC-Driver.md)  
  
  