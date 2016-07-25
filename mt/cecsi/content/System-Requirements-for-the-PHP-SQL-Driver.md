---
title: "Systemanforderungen f&#252;r den PHP_SQL-Treiber"
ms.custom: na
ms.date: 07/02/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5db4b75f-c605-4785-9560-399a533c0fc9
caps.latest.revision: 91
caps.handback.revision: 87
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
# Systemanforderungen f&#252;r den PHP_SQL-Treiber
Um mit dem [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]\(SQL Server 2008 oder neuer, falls Sie Version 3.2 oder 3.1 verwenden\) auf Daten im SQL Server 2005 oder einer neueren Datenbank zuzugreifen, müssen die folgenden Komponenten auf Ihrem PC installiert sein:  
  
-   Die unterstützten Betriebssysteme für die Versionen 3.2 und 3.1 des Treibers beinhalten:   
    -   Windows Server 2008 R2 SP1  
    -   Windows Vista SP2  
    -   Windows Server 2008 SP2  
    -   Windows 7 SP1  
    -   Windows Server 2012  
    -   Windows Server 2012 R2  
    -   Windows 8  
    -   Windows 8.1  
  
-   Die unterstützten Betriebssysteme für die Version 3.0 des Treibers beinhalten:  
    -   Windows Server 2008 R2 SP1  
    -   Windows Vista SP2  
    -   Windows Server 2008 SP2  
    -   Windows 7 SP1  
  
-   Die unterstützten Betriebssysteme für die Version 2.0 des Treibers beinhalten:  
    -   Die unterstützten Betriebssysteme für die Version 2.0 des Treibers beinhalten:  
    -   [!INCLUDE[winxpsvr](../content/includes/winxpsvr_md.md)] Service Pack 1  
    -   Windows XP Service Pack 3  
    -   Windows Vista Service Pack 1 oder neuer  
    -   Windows Server 2008  
    -   Windows Server 2008 R2  
    -   Windows 7  
  
-   SQL Azure-Datenbanken werden unterstützt. Weitere Informationen finden Sie unter [Connecting to Windows Azure SQL Database](../Topic/Connecting%20to%20Windows%20Azure%20SQL%20Database.md).  
  
-   PHP 5.x ist erforderlich. Weitere Informationen zum Herunterladen und Installieren von stabilen Binärdateien finden Sie unter [http:\/\/php.net](http://go.microsoft.com/fwlink/?LinkId=101876).  
  
-   Versionen von Microsoft Drivers for PHP for SQL Server erfordern die in der folgenden Tabelle aufgeführten PHP-Versionen:  
  
|Version von Microsoft Drivers for PHP for SQL Server |Unterstützte PHP-Versionen|  
|----------------------------------------------------|--------------------------|  
|3.2|PHP 5.6.4\+ oder<br /><br />PHP 5.5.16\+ oder<br /><br />PHP 5.4.32|  
|3.1|PHP 5.5.16\+ oder<br /><br />PHP 5.4.32|  
|3.0|PHP 5.4.32 oder<br /><br />PHP 5.3.0|  
|2.0|PHP 5.3.0 oder<br /><br />PHP 5.2.4 oder<br /><br />PHP 5.2.13|  
  
-   Eine Version der Treiberdatei muss sich in Ihrem PHP-Erweiterungsverzeichnis befinden. Weiter unten in diesem Text finden Sie unter „Treiberversionen“ weitere Informationen zu den verschiedenen Treiberdateien. Unter [Laden des PHP-SQL-Treibers](../content/Loading-the-PHP-SQL-Driver.md) finden Sie weitere Informationen zur Konfiguration der Treiber für die PHP-Laufzeit. Zum Herunterladen der Treiber, gehen Sie zu [Microsoft Drivers for PHP for SQL Server](http://www.microsoft.com/download/details.aspx?id=20098).  
  
-   Ein Webserver ist erforderlich. Ihr Webserver muss für die Ausführung von PHP konfiguriert sein. Informationen zum Hosten von PHP-Anwendungen mit Internetinformationsdiensten \(IIS\) 6.0 finden Sie unter [Verwenden von FastCGI zum Hosten von PHP-Anwendungen auf IIS 6.0](http://go.microsoft.com/fwlink/?LinkId=117131). Informationen zum Hosten von PHP-Anwendungen mit IIS 7.0 finden Sie unter [FastCGI zum Hosten von PHP-Anwendungen auf IIS 7.0 verwenden](http://go.microsoft.com/fwlink/?LinkId=117132).  
  
    [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] wurde auf IIS 6 und IIS 7 mit FastCGI getestet.  
  
    > [!NOTE]  
    > Microsoft bietet lediglich für IIS Support.  
  
-   Die Versionen 3.2 und 3.1 erfordern Microsoft ODBC Driver 11 for SQL Server \(oder höher\). Um den Microsoft ODBC Driver 11 for PHP for SQL Server herunterzuladen, gehen Sie zu [Microsoft ODBC Driver 11 for SQL Server](http://www.microsoft.com/download/details.aspx?id=36434).  
  
    Falls Sie den SQLSRV-Treiber verwenden, teilt [sqlsrv_client_info](../content/sqlsrv_client_info.md) Ihnen mit, welche Version des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Native Clients von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] verwendet wird. Fall Sie den PDO\_SQLSRV-Treiber verwenden, können Sie die Version mithilfe von [PDO::getAttribute](../Topic/PDO::getAttribute.md) abrufen.  
  
-   Für die Versionen 3.0 und 2.0 ist die x86-Version des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Native Clients auf dem Computer, der PHP ausführt, erforderlich. Falls Sie ein 64\-Bit-Betriebssystem verwenden, wird die x64-Version des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Native Clients zusammen mit der mit der x86-Version des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Native Clients installiert \(installieren Sie nicht die x86-Version des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Native Clients auf einem x64-Betriebssystem\).  
  
    Falls Sie den SQLSRV-Treiber verwenden, teilt [sqlsrv_client_info](../content/sqlsrv_client_info.md) Ihnen mit, welche Version des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Native Clients von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] verwendet wird. Fall Sie den PDO\_SQLSRV-Treiber verwenden, können Sie die Version mithilfe von [PDO::getAttribute](../Topic/PDO::getAttribute.md) abrufen.  
  
    -   Version 3.0 des Treibers erfordert Microsoft [!INCLUDE[ssSQL11](../content/includes/ssSQL11_md.md)] Native Client. Sie können den Microsoft [!INCLUDE[ssSQL11](../content/includes/ssSQL11_md.md)] Native Client von der [SQL Server 2012 Feature Pack-Seite](http://go.microsoft.com/fwlink/?LinkID=236805)herunterladen.  
  
    -   Die Version 2.0 des Treibers erfordert den Microsoft [!INCLUDE[ssKilimanjaro](../content/includes/ssKilimanjaro_md.md)] Native Client. Klicken Sie unten auf den passenden Link:  
  
        [X86-Paket herunterladen](http://go.microsoft.com/fwlink/?LinkID=188400&clcid=0x409)  
  
        [X64-Paket herunterladen](http://go.microsoft.com/fwlink/?LinkID=188401&clcid=0x409)  
  
## Treiberversionen  
Dieser Abschnitt listet die in den Versionen 3.2, 3.1, 3.0 und 2.0 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]enthaltenen Treiber auf.  
  
Folgen Sie den Anweisungen [Laden des PHP-SQL-Treibers](../content/Loading-the-PHP-SQL-Driver.md), um den Treiber für die Verwendung mit der PHP-Laufzeit zu konfigurieren.  
  
**Microsoft Drivers 3.2 for PHP for SQL Server installiert die folgenden Versionen des Treibers:**  
  
|Treiberdatei|PHP-Version|Threadsicher?|Zu verwendende PHP .dll|  
|---------------|---------------|----------------|---------------------|  
|php\_sqlsrv\_54\_nts.dll<br /><br />php\_pdo\_sqlsrv\_54\_nts.dll|5.4|nein|php5.dll|  
|php\_sqlsrv\_54\_ts.dll<br /><br />php\_pdo\_sqlsrv\_54\_ts.dll|5.4|ja|php5ts.dll|  
|php\_sqlsrv\_55\_nts.dll<br /><br />php\_pdo\_sqlsrv\_55\_nts.dll|5.5|nein|php5.dll|  
|php\_sqlsrv\_55\_ts.dll<br /><br />php\_pdo\_sqlsrv\_55\_ts.dll|5.5|ja|php5ts.dll|  
|php\_sqlsrv\_56\_nts.dll<br /><br />php\_pdo\_sqlsrv\_56\_nts.dll|5.6|nein|php5.dll|  
|php\_sqlsrv\_56\_ts.dll<br /><br />php\_pdo\_sqlsrv\_56\_ts.dll|5.6|ja|php5ts.dll|  
  
**Microsoft Drivers 3.1 for PHP for SQL Server installiert die folgenden Versionen des Treibers:**  
  
|Treiberdatei|PHP-Version|Threadsicher?|Zu verwendende PHP .dll|  
|---------------|---------------|----------------|---------------------|  
|php\_sqlsrv\_54\_nts.dll<br /><br />php\_pdo\_sqlsrv\_54\_nts.dll|5.4|nein|php5.dll|  
|php\_sqlsrv\_54\_ts.dll<br /><br />php\_pdo\_sqlsrv\_54\_ts.dll|5.4|ja|php5ts.dll|  
|php\_sqlsrv\_55\_nts.dll<br /><br />php\_pdo\_sqlsrv\_55\_nts.dll|5.5|nein|php5.dll|  
|php\_sqlsrv\_55\_ts.dll<br /><br />php\_pdo\_sqlsrv\_55\_ts.dll|5.5|ja|php5ts.dll|  
  
**Microsoft Drivers 3.0 for PHP for SQL Server installiert die folgenden Versionen des Treibers:**  
  
|Treiberdatei|PHP-Version|Threadsicher?|Zu verwendende PHP .dll|  
|---------------|---------------|----------------|---------------------|  
|php\_sqlsrv\_53\_nts.dll<br /><br />php\_pdo\_sqlsrv\_53\_nts.dll|5.3|nein|php5.dll|  
|php\_sqlsrv\_53\_ts.dll<br /><br />php\_pdo\_sqlsrv\_53\_ts.dll|5.3|ja|php5ts.dll|  
|php\_sqlsrv\_54\_nts.dll<br /><br />php\_pdo\_sqlsrv\_54\_nts.dll|5.4|nein|php5.dll|  
|php\_sqlsrv\_54\_ts.dll<br /><br />php\_pdo\_sqlsrv\_54\_ts.dll|5.4|ja|php5ts.dll|  
  
**Microsoft Drivers 2.0 for PHP for SQL Server installiert die folgenden Versionen des Treibers:**  
  
|Treiberdatei|PHP-Version|Threadsicher?|Zu verwendende PHP .dll|  
|---------------|---------------|----------------|---------------------|  
|php\_sqlsrv\_53\_nts\_vc6.dll<br /><br />php\_pdo\_sqlsrv\_53\_nts\_vc6.dll|5.3|nein|php5.dll|  
|php\_sqlsrv\_53\_nts\_vc9.dll<br /><br />php\_pdo\_sqlsrv\_53\_nts\_vc9.dll|5.3|nein|php5.dll|  
|php\_sqlsrv\_53\_ts\_vc6.dll<br /><br />php\_pdo\_sqlsrv\_53\_ts\_vc6.dll|5.3|ja|php5ts.dll|  
|php\_sqlsrv\_53\_ts\_vc9.dll<br /><br />php\_pdo\_sqlsrv\_53\_ts\_vc9.dll|5.3|ja|php5ts.dll|  
|php\_sqlsrv\_52\_nts\_vc6.dll<br /><br />php\_pdo\_sqlsrv\_52\_nts\_vc6.dll|5.2|nein|php5.dll|  
|php\_sqlsrv\_52\_ts\_vc6.dll<br /><br />php\_pdo\_sqlsrv\_52\_ts\_vc6.dll|5.2|ja|php5ts.dll|  
  
Wenn der Name der Treiberdatei „vc9“ enthält, sollte er mit einer PHP-Version, die mit Visual C\+\+ 9.0 kompiliert wurde, verwendet werden.  
  
## Siehe auch  
[Erste Schritte mit dem PHP-SQL-Treiber](../content/Getting-Started-with-the-PHP-SQL-Driver.md)
[Programmierhandbuch für den PHP-SQL-Treiber](../content/Programming-Guide-for-PHP-SQL-Driver.md)
[SQLSRV-Treiber – API-Referenz](../content/SQLSRV-Driver-API-Reference.md)  
  
