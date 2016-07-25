---
title: "Den Microsoft ODBC Driver for SQL Server on Linux installieren"
ms.custom: na
ms.date: 06/28/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f78b81ed-5214-43ec-a600-9bfe51c5745a
caps.latest.revision: 62
caps.handback.revision: 58
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
# Den Microsoft ODBC Driver for SQL Server on Linux installieren
Dieses Thema erklärt wie der [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] ODBC Driver 13 \(Preview\) und 11 for [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] on Linux installiert wird. Sie müssen den unixODBC\-Treiber\-Manager installieren, bevor Sie den Treiber verwenden können. Weitere Informationen finden Sie unter [Installieren des Treiber-Managers](../content/Installing-the-Driver-Manager.md).  
  
## Installieren des Microsoft ODBC Driver 13 \(Preview\) for SQL Server on Linux  
**Installationsschritte**  
  
Den Treiber installieren:  
  
1.  Stellen Sie sicher, dass Sie die Root\-Berechtigung besitzen.  
  
2.  Wechseln Sie zu dem Verzeichnis, in das der ODBC\-Treiber unter Linux die Datei namens „msodbcsql 13.0.0.0.tar.gz“ platziert hat. Stellen Sie sicher, dass Sie die zu Ihrer Linux\-Version passende Datei „\*.tar.g“ besitzen. Führen Sie den folgenden Befehl aus, um die Dateien zu extrahieren **tar xvzf msodbcsql\-13.0.0.0.tar.gz**  
  
3.  Wechseln Sie zum „msodbcsql 13.0.0.0.tar.gz“\-Verzeichnis; es sollte Ihnen eine Datei namens „install.sh“ angezeigt werden  
  
4.  Um eine Liste aller verfügbaren Installationsoptionen zu erhalten, führen Sie den folgenden Befehl aus: **.\/install.sh**  
  
5.  Führen Sie eine Sicherung von **odbcinst.ini** mittels Backup durch. Die Treiberinstallation aktualisiert **odbcinst.ini**. „odbcinst.ini“ beinhaltet die Liste der Treiber, die beim unixODBC\-Treiber\-Manager registriert sind. Um den Speicherort von „odbcinst.ini“ auf Ihrem Computer zu finden, führen Sie den folgenden Befehl aus: **odbc\_config \-\-odbcinstini**  
  
6.  Führen Sie den folgenden Befehl aus, bevor Sie den Treiber installieren: **.\/install.sh verify**. Die Ausgabe von **.\/install.sh verify** berichtet, ob Ihr Computer über die erforderliche Software verfügt, um den ODBC\-Treiber unter Linux zu unterstützen.  
  
7.  Wenn Sie bereit sind, den ODBC\-Treiber unter Linux zu installieren, führen Sie diesen Befehl aus: **.\/install.sh install**. Falls Sie einen Installationsbefehl angeben müssen \(**bin\-dir** oder **lib\-dir**\), geben Sie den Befehl nach der **install**\-Option an.  
  
8.  Lesen Sie die Lizenzvereinbarung und geben Sie **YES** ein, um mit der Installation fortzufahren.  
  
Die Installation platziert den Treiber in „\/opt\/microsoft\/msodbcsql\/13.0.0.0“. Der Treiber und seine Unterstützungsdateien müssen sich in „\/opt\/microsoft\/msodbcsql\/13.0.0.0“ befinden.  
  
Um zu überprüfen, ob der OBCD\-Treiber unter Linux erfolgreich registriert wurde, führen Sie den folgenden Befehl aus: **odbcinst \-q \-d \-n "ODBC Driver 13 for SQL Server"**.  
  
[Verwende bestehende MSDN C\+\+ ODBC\-Beispiele für den ODBC\-Treiber unter Linux](http://blogs.msdn.com/b/sqlblog/archive/2012/01/26/use-existing-msdn-c-odbc-samples-for-microsoft-linux-odbc-driver.aspx) zeigt ein Beispiel, das mittels des ODBC\-Treibers unter Linux eine Verbindung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] herstellt.  
  
**Deinstallieren**  
  
Sie können den ODBC\-Treiber unter Linux deinstallieren, indem Sie die folgenden Befehle ausführen:  
  
1.  rm \-f \/usr\/bin\/sqlcmd  
  
2.  rm \-f \/usr\/bin\/bcp  
  
3.  rm \-rf \/opt\/microsoft\/msodbcsql  
  
4.  odbcinst \-u \-d \-n "ODBC Driver 13 für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]"  
  
## Installieren des Microsoft ODBC Driver 11 for SQL Server on Linux  
**Installationsschritte**  
  
> [!IMPORTANT]  
> Diese Anleitung bezieht sich auf „msodbcsql\-11.0.2270.0.tar.gz“, die Installationsdatei für Red Hat Linux. Wenn Sie die Preview für SUSE Linux installieren, ist der Dateiname msodbcsql 11.0.2260.0.tar.gz.  
  
Den Treiber installieren:  
  
1.  Stellen Sie sicher, dass Sie die Root\-Berechtigung besitzen.  
  
2.  Wechseln Sie zu dem Verzeichnis, in das der ODBC\-Treiber unter Linux die Datei namens „msodbcsql\-11.0.2270.0.tar.gz“ platziert hat. Stellen Sie sicher, dass Sie die zu Ihrer Linux\-Version passende Datei „\*.tar.g“ besitzen. Führen Sie den folgenden Befehl aus, um die Dateien zu extrahieren **tar xvzf msodbcsql\-11.0.2270.0.tar.gz**.  
  
3.  Wechseln Sie zum „msodbcsql 11.0.2270.0.tar.gz“\-Verzeichnis; es sollte Ihnen eine Datei namens „install.sh“ angezeigt werden.  
  
4.  Um eine Liste aller verfügbaren Installationsoptionen zu erhalten, führen Sie den folgenden Befehl aus: **.\/install.sh**.  
  
5.  Führen Sie eine Sicherung von **odbcinst.ini** mittels Backup durch. Die Treiberinstallation aktualisiert **odbcinst.ini**. „odbcinst.ini“ beinhaltet die Liste der Treiber, die beim unixODBC\-Treiber\-Manager registriert sind. Um den Speicherort von „odbcinst.ini“ auf Ihrem Computer zu finden, führen Sie den folgenden Befehl aus: **odbc\_config \-\-odbcinstini**.  
  
6.  Führen Sie den folgenden Befehl aus, bevor Sie den Treiber installieren: **.\/install.sh verify**. Die Ausgabe von **.\/install.sh verify** berichtet, ob Ihr Computer über die erforderliche Software verfügt, um den ODBC\-Treiber unter Linux zu unterstützen.  
  
7.  Wenn Sie bereit sind, den ODBC\-Treiber unter Linux zu installieren, führen Sie diesen Befehl aus: **.\/install.sh install**. Falls Sie einen Installationsbefehl angeben müssen \(**bin\-dir** oder **lib\-dir**\), geben Sie den Befehl nach der **install**\-Option an.  
  
8.  Lesen Sie die Lizenzvereinbarung und geben Sie **YES** ein, um mit der Installation fortzufahren.  
  
Die Installation platziert den Treiber in „\/opt\/microsoft\/msodbcsql\/11.0.2270.0“. Der Treiber und seine Unterstützungsdateien müssen sich in „\/opt\/microsoft\/msodbcsql\/11.0.2270.0“ befinden.  
  
Um zu überprüfen, ob der OBCD\-Treiber unter Linux erfolgreich registriert wurde, führen Sie den folgenden Befehl aus: **odbcinst \-q \-d \-n "ODBC Driver 11 for SQL Server"**.  
  
[Verwende bestehende MSDN C\+\+ ODBC\-Beispiele für den ODBC\-Treiber unter Linux](http://blogs.msdn.com/b/sqlblog/archive/2012/01/26/use-existing-msdn-c-odbc-samples-for-microsoft-linux-odbc-driver.aspx) zeigt ein Beispiel, das mittels des ODBC\-Treibers unter Linux eine Verbindung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] herstellt.  
  
**Deinstallieren**  
  
Sie können den ODBC\-Treiber unter Linux deinstallieren, indem Sie die folgenden Befehle ausführen:  
  
1.  rm \-f \/usr\/bin\/sqlcmd  
  
2.  rm \-f \/usr\/bin\/bcp  
  
3.  rm \-rf \/opt\/microsoft\/msodbcsql  
  
4.  odbcinst \-u \-d \-n "ODBC Driver 11 für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]"  
  
## Beheben von Verbindungsproblemen  
Falls Sie keine Verbindung mittels ODBC\-Treiber unter Linux mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] herstellen können, verwenden Sie die folgenden Informationen, um das Problem zu identifizieren.  
  
Das häufigste Verbindungsproblem besteht darin, dass der unixODBC\-Treiber\-Manager doppelt installiert wurde. Durchsuchen Sie „\/usr“ nach „libodbc\*.so\*“. Falls Sie mehr als eine Version der Datei sehen, haben Sie \(möglicherweise\) mehr als einen Treiber\-Manager installiert. Ihre Anwendung verwendet eventuell die falsche Version. Falls Sie das unixODBC\-Treiber\-Manager\-Paket installiert sehen, wenn Sie \(in Red Hat\) den Befehl **yum list unixODBC** ausführen, löschen Sie das Paket.  
  
Aktivieren Sie das Verbindungsprotokoll, indem Sie bestätigen, dass Ihre „odbcinst.ini“\-Datei den Abschnitt und diese Elemente enthält:  
  
```  
[ODBC]  
Trace = Yes  
TraceFile = (your log file)  
```  
  
Falls der Verbindungsversuch wieder fehlschlägt und Ihnen keine Protokolldatei angezeigt wird, gibt es \(möglicherweise\) zwei Kopien des Treiber\-Managers auf Ihrem Computer. Andernfalls sollte die Ausgabe des Protokolls etwa so aussehen:  
  
```  
[ODBC][28783][1321576347.077780][SQLDriverConnectW.c][290]  
        Entry:  
            Connection = 0x17c858e0  
            Window Hdl = (nil)  
            Str In = [DRIVER={ODBC Driver 11 for SQL Server};SERVER={contoso.com};Trusted_Connection={YES};WSID={mydb.contoso.com};AP...][length = 139 (SQL_NTS)]  
            Str Out = (nil)  
            Str Out Max = 0  
            Str Out Ptr = (nil)  
            Completion = 0  
        UNICODE Using encoding ASCII 'UTF8' and UNICODE 'UTF16LE'  
```  
  
Falls die Zeichencodierung beispielsweise nicht UTF\-8 ist:  
  
```  
UNICODE Using encoding ASCII 'ISO8859-1' and UNICODE 'UCS-2LE'  
```  
  
Mehr als ein Treiber\-Manager sind installiert und Ihre Anwendung verwendet den falschen. Oder der Treiber\-Manager wurde falsch gebaut.  
  
Weitere Informationen zum Beheben von Verbindungsproblemen finden Sie hier:  
  
-   [Schritte zum Beheben von SQL\-Konnektivitätsproblemen](http://blogs.msdn.com/b/sql_protocols/archive/2008/04/30/steps-to-troubleshoot-connectivity-issues.aspx)  
  
-   [SQL Server 2005 Beheben von Konnektivitätsproblemen – Teil I](http://blogs.msdn.com/b/sql_protocols/archive/2005/10/22/sql-server-2005-connectivity-issue-troubleshoot-part-i.aspx)  
  
-   [Konnektivitätsproblembehebung in SQL Server 2008 mit dem Konnektivitätsringpuffer](http://blogs.msdn.com/b/sql_protocols/archive/2008/05/20/connectivity-troubleshooting-in-sql-server-2008-with-the-connectivity-ring-buffer.aspx)  
  
-   [Problembehebung für die SQL Server\-Authentifizierung](http://blogs.msdn.com/b/sqlsecurity/archive/2010/03/29/sql-server-authentication-troubleshooter.aspx)  
  
-   [Fehlerdetails \(http:\/\/www.microsoft.com\/products\/ee\/transform.aspx?ProdName\=Microsoft\+SQL\+Server&EvtSrc\=MSSQLServer&EvtID\=11001\)](http://www.microsoft.com/products/ee/transform.aspx?ProdName=Microsoft+SQL+Server&EvtSrc=MSSQLServer&EvtID=001)  
  
    Die in der URL spezifizierte Fehlernummer \(11001\) sollte geändert werden, damit sie mit dem Ihnen angezeigten Fehler übereinstimmt.  
  
## Siehe auch  
[Microsoft ODBC Driver for SQL Server on Linux](../content/Microsoft-ODBC-Driver-for-SQL-Server-on-Linux.md)  
  
