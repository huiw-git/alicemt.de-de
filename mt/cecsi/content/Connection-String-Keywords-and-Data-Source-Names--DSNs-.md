---
title: "Schl&#252;sselw&#246;rter f&#252;r Verbindungszeichenfolgen und Datenquellennamen (DSNs)"
ms.custom: na
ms.date: 06/09/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f95cdbce-e7c2-4e56-a9f7-8fa3a920a125
caps.latest.revision: 41
caps.handback.revision: 40
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
  - zh-cn
  - zh-tw
---
# Schl&#252;sselw&#246;rter f&#252;r Verbindungszeichenfolgen und Datenquellennamen (DSNs)
Dieses Thema beschreibt, wie Sie eine Verbindung mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank herstellen können.  
  
## Verbindungseigenschaften  
Für diese Version des [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] ODBC Driver for [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] on Linux können Sie die folgenden Verbindungsschlüsselwörter verwenden:  
  
||||||  
|-|-|-|-|-|  
|Addr|Adresse|ApplicationIntent|AutoTranslate|Datenbank|  
|Treiber|DSN|Encrypt|FileDSN|MARS\_Connection|  
|MultiSubnetFailover|PWD|Server|Trusted\_Connection|TrustServerCertificate|  
|UID|WSID||||  
  
> [!IMPORTANT]  
> Geben Sie beim Herstellen einer Verbindung mit einer Datenbank, welche Datenbankspiegelung verwendet \(oder einen Failoverpartner hat\), nicht den Namen der Datenbank in der Verbindungszeichenfolge an. Schicken Sie stattdessen einen **Verwende** *database\_name*\-Befehl, um sich mit der Datenbank zu verbinden, bevor Sie Ihre Abfragen ausführen.  
  
Weitere Informationen zu diesen Schlüsselwörtern finden Sie im ODBC\-Abschnitt von [Schlüsselwörter für Verbindungszeichenfolgen mit SQL Native Client verwenden](http://go.microsoft.com/fwlink/?LinkID=126696).  
  
Der Wert, der an das **Treiber**\-Schlüsselwort übermittelt wird, kann einer dieser beiden sein:  
  
-   Der Name, den Sie verwendet haben, als Sie den Treiber installiert haben. Oder  
  
-   Der Pfad zum Treiber, welcher in der Vorlagen\-INI\-Datei angegeben war, die wiederum verwendet wurde, um den Treiber zu installieren.  
  
Um ein DSN zu erstellen, erstellen \(falls nötig\) und bearbeiten Sie die Datei **~\/.odbc.ini** \(odbc.ini in Ihrem Basisverzeichnis\). Hier folgt eine Beispieldatei, welche die erforderlichen Einträge für eine DSN zeigt:  
  
```  
[MSSQLTest]  
Driver = ODBC Driver 11 for SQL Server  
Server = [protocol:]server[,port]  
#   
# Note:  
# Port is not a valid keyword in the ~/.odbc.ini file  
# for the Microsoft ODBC driver on Linux  
#  
```  
  
Sie können optional das Protokoll und den Port für die Verbindung mit dem Server angeben. Beispielsweise **Server \= tcp:***servername***,12345**.  
  
Um eine Verbindung mit einer benannten Instanz auf einem statischen Port herzustellen, verwenden Sie **Server \=** *servername***,***port\_number*. Das Verbinden mit dynamischen Ports wird nicht unterstützt.  
  
Optional können Sie die DSN\-Informationen auch einer Vorlagendatei hinzufügen und den folgenden Befehl ausführen: **odbcinst \-i \-s \-f** *template\_file*  
  
Sie können ISQL verwenden, um die Verbindung zu testen und zu überprüfen, ob Ihr Treiber funktioniert. Alternativ können Sie diesen Befehl verwenden: **bcp master.INFORMATION\_SCHEMA.TABLES out OutFile.dat \-S <server> \-U <name> \-P <password>**  
  
## Secure Sockets Layer \(SSL\) verwenden  
Sie können Secure Sockets Layer \(SSL\) verwenden, um Verbindungen mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] zu verschlüsseln. SSL schützt [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Benutzernamen und \-Kennwörter über das Netzwerk. SSL überprüft auch die Identität des Servers, um Schutz vor „man\-in\-the\-middle“\-Attacken \(MITM\) zu bieten.  
  
Das Aktivieren der Verschlüsselung erhöht die Sicherheit auf Kosten der Leistung.  
  
Weitere Informationen finden Sie unter [Verschlüsseln von Verbindungen zu SQL Server](http://go.microsoft.com/fwlink/?LinkId=220900).  
  
Unabhängig von den Einstellungen für **Encrypt** und **TrustServerCertificate** werden die Serveranmeldeinformationen \(Benutzername und Kennwort\) immer verschlüsselt. Die folgende Tabelle zeigt den Effekt der Einstellungen für **Encrypt** und **TrustServerCertificate**.  
  
||**TrustServerCertificate\=false**|**TrustServerCertificate\=true**|  
|-|-------------------------------------|------------------------------------|  
|**Encrypt\=no**|Das Serverzertifikat wird nicht überprüft.<br /><br />Zwischen dem Client und dem Server verschickte Daten sind nicht verschlüsselt.|Das Serverzertifikat wird nicht überprüft.<br /><br />Zwischen dem Client und dem Server verschickte Daten sind nicht verschlüsselt.|  
|**Encrypt\=yes**|Serverzertifikat wird überprüft.<br /><br />Zwischen dem Client und dem Server verschickte Daten sind verschlüsselt.<br /><br />Der Name \(oder die IP\-Adresse\) in einem allgemeinen Namen \(Common Name \(CN\)\) oder alternativen Antragsstellernamen \(Subject Alternative Name \(SAN\)\) in einem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-SSL\-Zertifikat sollte genau mit dem Servernamen \(oder der IP\-Adresse\), der in der Verbindungszeichenfolge angegeben wurde, übereinstimmen.|Das Serverzertifikat wird nicht überprüft.<br /><br />Zwischen dem Client und dem Server verschickte Daten sind verschlüsselt.|  
  
Standardmäßig überprüfen verschlüsselte Verbindungen immer das Zertifikat des Servers. Wenn Sie jedoch zu einem Server eine Verbindung herstellen, der ein selbstsigniertes Zertifikat hat, fügen Sie die TrustServerCertificateOption hinzu:  
  
```  
Driver='ODBC Driver 11 for SQL Server';Server=ServerNameHere;Encrypt=YES;TrustServerCertificate=YES  
```  
  
SSL verwendet die OpenSSL\-Bibliothek. Die folgende Tabelle zeigt die minimalen unterstützten Versionen von OpenSSL und die Zertifikatsvertrauensspeicherorte für jede Plattform:  
  
|Platform|Minimale OpenSSL\-Version|Standard\-Zertifikatsvertrauensspeicherort|  
|------------|-----------------------------|----------------------------------------------|  
|Red Hat Enterprise Linux 5|0.9.8e|\/etc\/pki\/tls\/cert.pem|  
|Red Hat Enterprise Linux 6|1.0.0\-10|\/etc\/pki\/tls\/cert.pem|  
|SuSE Linux Enterprise 11 Service Pack 2|0.9.8j|\/etc\/ssl\/certs|  
  
Sie können **SQLDriverConnect** verwenden, um Verschlüsselung in der Verbindungszeichenfolge festzulegen.  
  
## Siehe auch  
[Microsoft ODBC Driver for SQL Server on Linux](../content/Microsoft-ODBC-Driver-for-SQL-Server-on-Linux.md)  
[Den Microsoft ODBC Driver for SQL Server on Linux installieren](../content/Installing-the-Microsoft-ODBC-Driver-for-SQL-Server-on-Linux.md)  
  
