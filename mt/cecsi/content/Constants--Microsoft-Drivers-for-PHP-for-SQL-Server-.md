---
title: "Konstanten (Microsoft-Treiber f&#252;r PHP f&#252;r SQL Server)"
ms.custom: na
ms.date: 07/18/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9727c944-b645-48d6-9012-18dbde35ee3c
caps.latest.revision: 70
caps.handback.revision: 69
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
# Konstanten (Microsoft-Treiber f&#252;r PHP f&#252;r SQL Server)
In diesem Thema werden die Konstanten erläutert, die durch [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]definiert sind.  
  
## PDO\_SQLSRV-Treiberkonstanten  
Die Konstanten, die auf der [PDO Website](http://go.microsoft.com/fwlink/?LinkID=187441) aufgeführt sind, gelten in der [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)].  
  
Im Folgenden werden die Microsoft-spezifischen Konstanten im PDO\_SQLSRV-Treiber beschrieben.  
  
### Konstanten der Transaktionsisolationsebene  
Der **TransactionIsolation** -Schlüssel, der mit [PDO::__construct](../Topic/PDO::__construct.md)verwendet wird, akzeptiert eine der folgenden Konstanten:  
  
-   PDO::SQLSRV\_TXN\_READ\_UNCOMMITTED  
  
-   PDO::SQLSRV\_TXN\_READ\_COMMITTED  
  
-   PDO::SQLSRV\_TXN\_REPEATABLE\_READ  
  
-   PDO::SQLSRV\_TXN\_SNAPSHOT  
  
-   PDO::SQLSRV\_TXN\_SERIALIZABLE  
  
Weitere Informationen zum **TransactionIsolation** -Schlüssel finden Sie unter [Connection Options](../content/Connection-Options.md).  
  
### Codierungskonstanten  
Das PDO::SQLSRV\_ATTR\_ENCODING-Attribut kann an [PDOStatement::setAttribute](../Topic/PDOStatement::setAttribute.md), [PDO::setAttribute](../Topic/PDO::setAttribute.md), [PDO::prepare](../Topic/PDO::prepare.md), [PDOStatement::bindColumn](../Topic/PDOStatement::bindColumn.md) und [PDOStatement::bindParam](../Topic/PDOStatement::bindParam.md) übergeben werden.  
  
Die verfügbaren Werte, die an PDO::SQLSRV\_ATTR\_ENCODING übergeben werden können, sind  
  
|PDO\_SQLSRV-Treiberkonstanten|Beschreibung|  
|-------------------------------|---------------|  
|PDO::SQLSRV\_ENCODING\_BINARY|Die Daten sind ein einfacher, uncodierter und nicht übersetzter Strom aus unbearbeiteten Bytes.<br /><br />Dies gilt nicht für PDO::setAttribute.|  
|PDO::SQLSRV\_ENCODING\_SYSTEM|Daten stellen 8\-Bit-Zeichen gemäß der Codepage des im System eingestellten Windows-Gebietsschemas dar. Alle Multi\-Byte-Zeichen oder Zeichen, die nicht in dieser Codepage abgebildet sind, werden durch ein aus einem einzelnen Byte bestehendes Fragezeichen \(?\) ersetzt.|  
|PDO::SQLSRV\_ENCODING\_UTF8|Die Daten liegen in UTF\-8-Codierung vor. Diese ist die Standardcodierung.|  
|PDO::SQLSRV\_ENCODING\_DEFAULT|Verwendet PDO::SQLSRV\_ENCODING\_SYSTEM, wenn das während des Verbindungsaufbaus angegeben wird.<br /><br />Verwenden Sie die Codierung der Verbindung, wenn diese in einer Prepare-Anweisung angegeben ist.|  
  
### Abfragetimeout  
Das PDO::SQLSRV\_ATTR\_QUERY\_TIMEOUT-Attribut ist eine beliebige nicht negative ganze Zahl, die das Timeout in Sekunden darstellt. Null \(0\) ist die Standardeinstellung und bedeutet kein Timeout.  
  
Sie können das PDO::SQLSRV\_ATTR\_QUERY\_TIMEOUT-Attribut mit [PDOStatement::setAttribute](../Topic/PDOStatement::setAttribute.md), [PDO::setAttribute](../Topic/PDO::setAttribute.md) und [PDO::prepare](../Topic/PDO::prepare.md) angeben.  
  
### Direkte oder vorbereitete Ausführung  
Sie können die Ausführung von direkten Abfragen oder die vorbereitete Ausführung mit dem Attribut PDO::SQLSRV\_ATTR\_DIRECT\_QUERY auswählen. PDO::SQLSRV\_ATTR\_DIRECT\_QUERY kann mit [PDO::prepare](../Topic/PDO::prepare.md) oder [PDO::setAttribute](../Topic/PDO::setAttribute.md) festgelegt werden. Weitere Informationen zu PDO::SQLSRV\_ATTR\_DIRECT\_QUERY finden Sie unter [Direkte Anweisungsausführung und vorbereitete Anweisungsausführung im PDO_SQLSRV-Treiber](../Topic/Direct%20Statement%20Execution%20and%20Prepared%20Statement%20Execution%20in%20the%20PDO_SQLSRV%20Driver.md).  
  
## Konstanten zum Treiber SQLSRV  
Die folgenden Abschnitte listen die Konstanten auf, die der SQLSRV-Treiber verwendet.  
  
### ERR-Konstanten  
Die folgende Tabelle enthält die Konstanten, die verwendet werden, um anzugeben, ob [sqlsrv\_errors](../content/sqlsrv_errors.md) Fehler, Warnungen oder beides zurückgibt.  
  
|Wert|Beschreibung|  
|---------|---------------|  
|SQLSRV\_ERR\_ALL|Fehler und Warnungen, die beim letzten **sqlsrv** -Funktionsaufruf generiert wurden, werden zurückgegeben. Dies ist der Standardwert.|  
|SQLSRV\_ERR\_ERRORS|Fehler und Warnungen aus dem letzten **sqlsrv** -Funktionsaufruf werden zurückgegeben.|  
|SQLSRV\_ERR\_WARNINGS|Warnungen aus dem letzten **sqlsrv** -Funktionsaufruf werden zurückgegeben.|  
  
### FETCH-Konstanten  
Die folgende Tabelle enthält die Konstanten, die verwendet werden, um den Typ des von [sqlsrv_fetch_array](../content/sqlsrv_fetch_array.md)zurückgegebenen Arrays anzugeben.  
  
|SQLSRV-Konstante|Beschreibung|  
|-------------------|---------------|  
|SQLSRV\_FETCH\_ASSOC|**sqlsrv\_fetch\_array** gibt die nächste Datenzeile als assoziatives Array zurück.|  
|SQLSRV\_FETCH\_BOTH|**sqlsrv\_fetch\_array** gibt die nächste Datenzeile als Array zurück, das sowohl numerische als auch assoziative Schlüssel aufweist. Dies ist der Standardwert.|  
|SQLSRV\_FETCH\_NUMERIC|**sqlsrv\_fetch\_array** gibt die nächste Datenzeile als numerisch indiziertes Array zurück.|  
  
### Protokollierungskonstanten  
In diesem Abschnitt sind die Konstanten aufgelistet, die verwendet werden, um die Protokollierungseinstellungen mit [sqlsrv_configure](../content/sqlsrv_configure.md)zu ändern. Weitere Informationen zur Protokollierung von Aktivitäten finden Sie unter [Logging Activity](../content/Logging-Activity.md).  
  
Die folgende Tabelle beschreibt die Konstanten, die als Wert für die **LogSubsystems** Einstellung verwendet werden können:  
  
|SQLSRV-Konstante \(entsprechende ganze Zahl in Klammern\)|Beschreibung|  
|----------------------------------------------------------|---------------|  
|SQLSRV\_LOG\_SYSTEM\_ALL \(\-1\)|Aktiviert die Protokollierung aller Subsysteme.|  
|SQLSRV\_LOG\_SYSTEM\_CONN \(2\)|Aktiviert die Protokollierung der Verbindungsaktivität.|  
|SQLSRV\_LOG\_SYSTEM\_INIT \(1\)|Aktiviert die Protokollierung der Initialisierungsaktivität.|  
|SQLSRV\_LOG\_SYSTEM\_OFF \(0\)|Deaktiviert die Protokollierung.|  
|SQLSRV\_LOG\_SYSTEM\_STMT \(4\)|Aktiviert die Protokollierung der Anweisungsaktivität.|  
|SQLSRV\_LOG\_SYSTEM\_UTIL \(8\)|Aktiviert die Protokollierung der Fehlerfunktionsaktivität \(z. B. **handle\_error** und **handle\_warning**\).|  
  
Die folgende Tabelle listet die Konstanten auf, die als Wert für die **LogSeverity** -Einstellung verwendet werden können:  
  
|SQLSRV-Konstante \(entsprechende ganze Zahl in Klammern\)|Beschreibung|  
|----------------------------------------------------------|---------------|  
|SQLSRV\_LOG\_SEVERITY\_ALL \(\-1\)|Gibt an, dass Fehler, Warnungen und Hinweise protokolliert werden.|  
|SQLSRV\_LOG\_SEVERITY\_ERROR \(1\)|Gibt an, dass Fehler protokolliert werden.|  
|SQLSRV\_LOG\_SEVERITY\_NOTICE \(4\)|Gibt an, dass Hinweise protokolliert werden.|  
|SQLSRV\_LOG\_SEVERITY\_WARNING \(2\)|Gibt an, dass Warnungen protokolliert werden.|  
  
### NULL-Wert-Konstanten  
Die folgende Tabelle enthält die Konstanten, die Sie verwenden können, um zu bestimmen, ob eine Spalte NULL-Werte zulässt oder ob diese Information nicht verfügbar ist. Sie können den Wert des **Nullable** -Schlüssels vergleichen, der von [sqlsrv_field_metadata](../content/sqlsrv_field_metadata.md) zurückgegeben wird, um den Status der NULL-Wert-Behandlung der Spalte zu bestimmen.  
  
|SQLSRV-Konstante \(entsprechende ganze Zahl in Klammern\)|Beschreibung|  
|----------------------------------------------------------|---------------|  
|SQLSRV\_NULLABLE\_YES \(0\)|In der Spalte ist NULL zulässig.|  
|SQLSRV\_NULLABLE\_NO \(1\)|NULL-Werte sind in der Spalte nicht zulässig.|  
|SQLSRV\_NULLABLE\_UNKNOWN \(2\)|Es ist nicht bekannt, ob die Spalte NULL-Werte zulässt.|  
  
### PARAM-Konstanten  
Die folgende Liste enthält die Konstanten für die Angabe der Parameterrichtung, wenn Sie [sqlsrv_query](../content/sqlsrv_query.md) oder [sqlsrv_prepare](../content/sqlsrv_prepare.md)aufrufen.  
  
|SQLSRV-Konstante|Beschreibung|  
|-------------------|---------------|  
|SQLSRV\_PARAM\_IN|Gibt einen Eingabeparameter an.|  
|SQLSRV\_PARAM\_INOUT|Gibt einen bidirektionalen Parameter an.|  
|SQLSRV\_PARAM\_OUT|Gibt einen Ausgabeparameter an.|  
  
### PHPTYPE-Konstanten  
Die folgende Tabelle enthält die Konstanten, die verwendet werden, um die PHP-Datentypen zu beschreiben. Informationen zu PHP-Datentypen finden Sie unter [PHP-Typen](http://go.microsoft.com/fwlink/?LinkId=104881).  
  
|SQLSRV-Konstante|PHP-Datentyp|  
|-------------------|-----------------|  
|SQLSRV\_PHPTYPE\_INT|Integer|  
|SQLSRV\_PHPTYPE\_DATETIME|Datetime|  
|SQLSRV\_PHPTYPE\_FLOAT|Float|  
|SQLSRV\_PHPTYPE\_STREAM\(<encoding><sup>1</sup>\)|Datenstrom|  
|SQLSRV\_PHPTYPE\_STRING\(<encoding><sup>1</sup>\)|String|  
  
1. **SQLSRV\_PHPTYPE\_STREAM** and **SQLSRV\_PHPTYPE\_STRING** nimmt einen Parameter an, der die Codierung des Datenstroms angibt. Die folgende Tabelle enthält die SQLSRV-Konstanten, die als Parameter akzeptiert werden sowie eine Beschreibung der zugehörigen Codierung.  
  
|SQLSRV-Konstante|Beschreibung|  
|-------------------|---------------|  
|SQLSRV\_ENC\_BINARY|Die Daten werden als uncodierter und nicht übersetzter Strom aus unbearbeiteten Bytes vom Server zurückgegeben.|  
|SQLSRV\_ENC\_CHAR|Daten werden in 8\-Bit-Zeichen gemäß der Codepage des Windows-Gebietsschemas zurückgegeben, das auf dem System installiert ist. Alle Multi\-Byte-Zeichen oder Zeichen, die nicht in dieser Codepage abgebildet sind, werden durch ein aus einem einzelnen Byte bestehendes Fragezeichen \(?\) enthalten.<br /><br />Diese ist die Standardcodierung.|  
|„UTF\-8“|Die Daten werden in UTF\-8-Codierung zurückgegeben. Diese Konstante wurde in Version 1.1 von der [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt. Weitere Informationen zur UTF\-8-Unterstützung finden Sie unter [Gewusst wie: Senden und Abrufen von UTF-8-Daten mithilfe der eingebauten UTF-8-Unterstützung.](../Topic/How%20to:%20Send%20and%20Retrieve%20UTF-8%20Data%20Using%20Built-In%20UTF-8%20Support.md).|  
  
> [!NOTE]  
> Bei Verwendung von **SQLSRV\_PHPTYPE\_STREAM** oder **SQLSRV\_PHPTYPE\_STRING** muss die Codierung angegeben werden. Wenn kein Parameter angegeben wird, wird ein Fehler zurückgegeben.  
  
Weiter Informationen zu diesen Konstanten finden Sie unter [Gewusst wie: Angeben von PHP-Datentypen](../Topic/How%20to:%20Specify%20PHP%20Data%20Types.md), [Gewusst wie: Abrufen von Zeichendaten als Stream mit dem SQLSRV-Treiber](../Topic/How%20to:%20Retrieve%20Character%20Data%20as%20a%20Stream%20Using%20the%20SQLSRV%20Driver.md).  
  
### SQLTYPE-Konstanten  
Die folgende Tabelle enthält die Konstanten, die verwendet werden, um die SQL Server-Datentypen zu beschreiben. Einige Konstanten erfordern Parameter, die der Genauigkeit, den Dezimalstellen und\/oder der Länge entsprechen. Informationen zu allen unterstützten SQL Server-Datentypen finden Sie unter [Datentypen \(Transact\-SQL\).](http://go.microsoft.com/fwlink/?LinkId=104883) Informationen zu Genauigkeit, Dezimalstellen und Länge finden Sie unter [Genauigkeit, Dezimalstellen und Länge \(Transact\-SQL\).](http://go.microsoft.com/fwlink/?LinkId=104885)  
  
|SQLSRV-Konstante|SQL Server-Datentyp|  
|-------------------|------------------------|  
|SQLSRV\_SQLTYPE\_BIGINT|bigint|  
|SQLSRV\_SQLTYPE\_BINARY|binary|  
|SQLSRV\_SQLTYPE\_BIT|bit|  
|SQLSRV\_SQLTYPE\_CHAR\($charCount\)|char|  
|SQLSRV\_SQLTYPE\_DATE|Datum<sup>4</sup>|  
|SQLSRV\_SQLTYPE\_DATETIME|Datetime|  
|SQLSRV\_SQLTYPE\_DATETIME2|datetime2<sup>4</sup>|  
|SQLSRV\_SQLTYPE\_DATETIMEOFFSET|datetimeoffset<sup>4</sup>|  
|SQLSRV\_SQLTYPE\_DECIMAL\($precision, $scale\)|decimal|  
|SQLSRV\_SQLTYPE\_FLOAT|Float|  
|SQLSRV\_SQLTYPE\_IMAGE|image<sup>1</sup>|  
|SQLSRV\_SQLTYPE\_INT|int|  
|SQLSRV\_SQLTYPE\_MONEY|money|  
|SQLSRV\_SQLTYPE\_NCHAR\($charCount\)|nchar|  
|SQLSRV\_SQLTYPE\_NUMERIC\($precision, $scale\)|numeric|  
|SQLSRV\_SQLTYPE\_NVARCHAR\($charCount\)|nvarchar|  
|SQLSRV\_SQLTYPE\_NVARCHAR\('max'\)|nvarchar\(MAX\)|  
|SQLSRV\_SQLTYPE\_NTEXT|ntext<sup>2</sup>|  
|SQLSRV\_SQLTYPE\_REAL|real|  
|SQLSRV\_SQLTYPE\_SMALLDATETIME|smalldatetime|  
|SQLSRV\_SQLTYPE\_SMALLINT|smallint|  
|SQLSRV\_SQLTYPE\_SMALLMONEY|smallmoney|  
|SQLSRV\_SQLTYPE\_TEXT|text<sup>3</sup>|  
|SQLSRV\_SQLTYPE\_TIME|time<sup>4</sup>|  
|SQLSRV\_SQLTYPE\_TIMESTAMP|timestamp|  
|SQLSRV\_SQLTYPE\_TINYINT|tinyint|  
|SQLSRV\_SQLTYPE\_UNIQUEIDENTIFIER|uniqueidentifier|  
|SQLSRV\_SQLTYPE\_UDT|UDT|  
|SQLSRV\_SQLTYPE\_VARBINARY\($byteCount\)|varbinary|  
|SQLSRV\_SQLTYPE\_VARBINARY\('max'\)|varbinary\(MAX\)|  
|SQLSRV\_SQLTYPE\_VARCHAR\($charCount\)|varchar|  
|SQLSRV\_SQLTYPE\_VARCHAR\('max'\)|varchar\(MAX\)|  
|SQLSRV\_SQLTYPE\_XML|xml|  
  
1.  Dies ist ein veralteter Typ, der dem varbinary\(max\)-Typ zugeordnet ist.  
  
2.  Dies ist ein veralteter Typ, der dem neueren nvarchar-Typ zugeordnet ist.  
  
3.  Dies ist ein veralteter Typ, der dem neueren varchar-Typ zugeordnet ist.  
  
4.  Unterstützung für diesen Typ wurde in Version 1.1 der [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt.  
  
Die folgende Tabelle enthält die SQLTYPE-Konstanten, die Parameter und den Bereich der zulässigen Werte für den Parameter akzeptieren.  
  
|SQLTYPE|Parameter|Für Parameter zulässiger Bereich|  
|-----------|-------------|---------------------------------|  
|SQLSRV\_SQLTYPE\_CHAR,<br /><br />SQLSRV\_SQLTYPE\_VARCHAR|charCount|1 \- 8000|  
|SQLSRV\_SQLTYPE\_NCHAR,<br /><br />SQLSRV\_SQLTYPE\_NVARCHAR|charCount|1 \- 4000|  
|SQLSRV\_SQLTYPE\_BINARY,<br /><br />SQLSRV\_SQLTYPE\_VARBINARY|byteCount|1 \- 8000|  
|SQLSRV\_SQLTYPE\_DECIMAL,<br /><br />SQLSRV\_SQLTYPE\_NUMERIC|precision|1 \- 38|  
|SQLSRV\_SQLTYPE\_DECIMAL,<br /><br />SQLSRV\_SQLTYPE\_NUMERIC|scale|1 \- precision|  
  
### Konstanten der Transaktionsisolationsebene  
Der **TransactionIsolation** -Schlüssel, der mit [sqlsrv_connect](../content/sqlsrv_connect.md)verwendet wird, akzeptiert eine der folgenden Konstanten:  
  
-   SQLSRV\_TXN\_READ\_UNCOMMITTED  
  
-   SQLSRV\_TXN\_READ\_COMMITTED  
  
-   SQLSRV\_TXN\_REPEATABLE\_READ  
  
-   SQLSRV\_TXN\_SNAPSHOT  
  
-   SQLSRV\_TXN\_SERIALIZABLE  
  
### Konstanten für Cursor und Durchführen eines Bildlaufs  
Die folgenden Konstanten geben die Art des Cursors an, den Sie in einem Resultset verwenden können:  
  
-   SQLSRV\_CURSOR\_FORWARD  
  
-   SQLSRV\_CURSOR\_STATIC  
  
-   SQLSRV\_CURSOR\_DYNAMIC  
  
-   SQLSRV\_CURSOR\_KEYSET  
  
-   SQLSRV\_CURSOR\_CLIENT\_BUFFERED  
  
Die folgenden Konstanten geben an, welche Zeile im Resultset ausgewählt werden soll:  
  
-   SQLSRV\_SCROLL\_NEXT  
  
-   SQLSRV\_SCROLL\_PRIOR  
  
-   SQLSRV\_SCROLL\_FIRST  
  
-   SQLSRV\_SCROLL\_LAST  
  
-   SQLSRV\_SCROLL\_ABSOLUTE  
  
-   SQLSRV\_SCROLL\_RELATIVE  
  
Weitere Informationen zu diesen Konstanten finden Sie unter [Specifying a Cursor Type and Selecting Rows](../content/Specifying-a-Cursor-Type-and-Selecting-Rows.md).  
  
## Siehe auch  
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
  
