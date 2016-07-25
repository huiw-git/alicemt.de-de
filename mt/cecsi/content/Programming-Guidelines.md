---
title: "Programmierrichtlinien"
ms.custom: na
ms.date: 06/09/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0cc8686c-e27b-4963-b674-dc420fcbd3d2
caps.latest.revision: 39
caps.handback.revision: 35
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
# Programmierrichtlinien
Die Features für die Programmierung des [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] ODBC Driver 11 for [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] on Linux basieren auf ODBC in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Native Client \([SQL Server Native Client \(ODBC\)](http://go.microsoft.com/fwlink/?LinkID=134151)\).[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Native Client basiert auf ODBC in Windows Data Access Components \([Referenz für ODBC\-Programmierer](http://go.microsoft.com/fwlink/?LinkID=45250)\).  
  
> [!IMPORTANT]  
> Diese Anleitungen beziehen sich auf „msodbcsql\-11.0.2270.0.tar.gz“, die Installationsdatei für Red Hat Linux. Wenn Sie die CTP\-Version von SUSE Linux installieren, lautet der Dateiname „msodbcsql\-11.0.2260.0.tar.gz“.  
  
Eine ODBC\-Anwendung kann Multiple Active Result Sets \(MARS\) und andere [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-spezifische Besonderheiten verwenden, indem Sie dazu „\/opt\/microsoft\/msodbcsql\/11.0.2270.0\/msodbcsql.h“ einschließen, nachdem die unixODBC\-Header \(sql.h, sqlext.h, sqltypes.h und sqlucode.h\) eingeschlossen wurden. Verwenden Sie anschließend die gleichen symbolischen Namen  für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-spezifische Elemente, die Sie auch in Ihrer Windows\-ODBC\-Anwendung verwenden würden.  
  
## Verfügbare Funktionen  
Die folgenden Abschnitte aus der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Native Client Dokumentation für ODBC \([SQL Server Native Client \(ODBC\)](http://go.microsoft.com/fwlink/?LinkID=134151)\) sind gültig, wenn der ODBC\-Treiber unter Linux verwendet wird:  
  
-   [Kommunikation mit SQL Server \(ODBC\)](http://msdn.microsoft.com/library/ms131692.aspx)  
  
-   [Verbindungs\- und Abfragetimeout\-Unterstützung](http://msdn.microsoft.com/library/ms130822.aspx)  
  
-   [Cursor](http://msdn.microsoft.com/library/ms130794(SQL.110).aspx)  
  
-   [Datums\-\/Uhrzeitverbesserungen \(ODBC\)](http://msdn.microsoft.com/library/bb677319.aspx)  
  
-   [Ausführen von Abfragen \(ODBC\)](http://msdn.microsoft.com/library/ms131677.aspx)  
  
-   [Behandlung von Fehlern und Meldungen](http://msdn.microsoft.com/library/ms131289.aspx)  
  
-   [Kerberos\-Authentifizierung](http://msdn.microsoft.com/library/cc280459.aspx)  
  
-   [Große benutzerdefinierte CLR\-Typen \(ODBC\)](http://msdn.microsoft.com/library/bb677316.aspx)  
  
-   [Ausführen von Transaktionen \(ODBC\) \(mit Ausnahme der verteilten Transaktionen\)](http://msdn.microsoft.com/library/ms131706.aspx)  
  
-   [Verarbeiten von Ergebnissen \(ODBC\)](http://msdn.microsoft.com/library/ms130812.aspx)  
  
-   [Ausführen gespeicherter Prozeduren](http://msdn.microsoft.com/library/ms131440.aspx)  
  
-   [Unterstützung für Spalten mit geringer Dichte \(ODBC\)](http://msdn.microsoft.com/library/cc280357.aspx)  
  
-   [SSL\-Verschlüsselung](http://msdn.microsoft.com/library/ms131691.aspx)  
  
-   [UTF\-8 und UTF\-16 für die Befehls\- und Daten\-API](http://msdn.microsoft.com/library/ff878241.aspx)  
  
-   [Verwenden von Katalogfunktionen](http://msdn.microsoft.com/library/ms131490.aspx)  
  
## Nicht verfügbare Funktionen  
Die folgenden Funktionen sind nicht in dieser Version des ODBC\-Treibers für Linux verfügbar:  
  
-   Funktionen zum Massenkopieren \(z. B. bcp\_batch\)  
  
-   Verteilte Transaktionen \(das Attribut SQL\_ATTR\_ENLIST\_IN\_DTC wird nicht unterstützt\)  
  
-   Datenbankspiegelung  
  
-   FILESTREAM  
  
-   Leistungsprofil für den ODBC\-Treiber, erläutert in [SQLSetConnectAttr](http://go.microsoft.com/fwlink/?LinkId=234099), sowie die folgenden leistungsbezogenen Verbindungsattribute:  
  
    -   SQL\_COPT\_SS\_PERF\_DATA  
  
    -   SQL\_COPT\_SS\_PERF\_DATA\_LOG  
  
    -   SQL\_COPT\_SS\_PERF\_DATA\_LOG\_NOW  
  
    -   SQL\_COPT\_SS\_PERF\_QUERY  
  
    -   SQL\_COPT\_SS\_PERF\_QUERY\_INTERVAL  
  
    -   SQL\_COPT\_SS\_PERF\_QUERY\_LOG  
  
-   SQLBrowseConnect  
  
-   Tabellenwertparameter \(TVP\)  
  
-   C\-Intervall\-Typen, wie z. B. SQL\_C\_INTERVAL\_YEAR\_TO\_MONTH \(dokumentiert in [\-Datentypbezeichnungen und Deskriptoren](http://msdn.microsoft.com/library/ms716351(VS.85).aspx)\), werden derzeit nicht unterstützt.  
  
-   Nicht unterstützt: der Wert SQL\_CUR\_USE\_ODBC, des Attributs SQL\_ATTR\_ODBC\_CURSORS der Funktion SQLSetConnectAttr.  
  
## Zeichenunterstützung  
SQLCHAR\-Daten müssen UTF\-8 sein. SQLWCHAR\-Daten müssen UTF\-16LE \(Little Endian\) sein.  
  
Wenn SQLDescribeParameter keinen SQL\-Typ auf dem Server angibt, verwendet der Treiber den SQL\-Typ, der im *ParameterType*\-Parameter von SQLBindParameter angegeben ist. Wenn ein schmaler SQL\-Datentyp, wie SQL\_VARCHAR, in SQLBindParameter angegeben ist, konvertiert der Treiber die angegebenen UTF\-8\-Daten auf die Standardcodepage von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]. \(Die Standardcodepage von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ist in der Regel 1252.\) Es können jedoch Datenverluste auftreten. Wenn Codepage 1252 ein Zeichen nicht darstellen kann, konvertiert der Treiber das Zeichen in ein Fragezeichen \(„?“\). Um diese Datenverluste zu vermeiden, geben Sie in SQLBindParameter einen Unicode SQL\-Zeichentyp an, z. B. SQL\_NVARCHAR. In diesem Fall konvertiert der Treiber die bereitgestellten, in UTF\-8 codierten Daten ohne Genauigkeitsverlust in UTF\-16.  
  
Es besteht ein Konversionsunterschied in der Textcodierung zwischen Windows und der iconv\-Bibliothek unter Linux. Textdaten, die in der Codepage 1255 \(Hebräisch\) codiert sind, enthalten einen Codepunkt \(0xCA\), der sich auf beiden Plattformen unterschiedlich verhält. Konvertieren in Unicode unter Windows erzeugt einen UTF\-16\-Codepunkt des Werts 0x05BA. Konvertieren in Unicode unter Linux erzeugt einen UTF\-16\-Codepunkt des Werts 0x00CA. Der Codepunkt 0xCA in Codepage 1255 ist nicht als Zeichen definiert. Eine Anwendung sollte nicht Logik einschließen, die den \(nicht definierten\) Codepunkt 0xCA verwendet.  
  
Wenn UTF\-8\-Mehrbytezeichen oder UTF\-16\-Ersatzzeichen auf SQLPutData\-Puffer aufgeteilt werden, entsteht Datenbeschädigung. Für das Streamen von SQLPutData, verwenden Sie Puffer, die nicht in partiellen Zeichencodierungen enden.  
  
## Weitere Probleme  
  
1.  Sie können eine dedizierte Administratorverbindung \(DAC\) herstellen, indem Sie die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Authentifizierung und **Host, Port** verwenden. Ein Mitglied der Sysadmin\-Rolle muss zunächst den DAC\-Port ermitteln. Wenn beispielsweise der DAC\-Port „33000“ wäre, könnten Sie mit „sqlcmd“ wie folgt eine Verbindung herstellen:  
  
    ```  
    sqlcmd –U <user> -P <pwd> -S <host>,33000  
    ```  
  
2.  Der UnixODBC\-Treiber\-Manager gibt „ Attribut\-\/Optionsbezeichner ungültig“ für alle Anweisungsattribute zurück, wenn sie über SQLSetConnectAttr übergeben werden. Wenn SQLSetConnectAttr unter Windows einen Anweisungsattributwert erhält, verursacht dieser, dass der Treiber diesen Wert für alle aktiven Anweisungen festlegt, die dem Verbindungshandle untergeordnet sind.  
  
    > [!NOTE]  
    > DAC\-Verbindungen müssen [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Authentifizierung verwenden.  
  
## Siehe auch  
[Microsoft ODBC Driver for SQL Server on Linux](../content/Microsoft-ODBC-Driver-for-SQL-Server-on-Linux.md)  
  
