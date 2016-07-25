---
title: "sqlsrv_field_metadata"
ms.custom: na
ms.date: 06/28/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - sqlsrv_field_metadata
apitype: NA
ms.assetid: c02f6942-0484-4567-a78e-fe8aa2053536
caps.latest.revision: 34
caps.handback.revision: 33
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
# sqlsrv_field_metadata
Ruft Metadaten für die Felder einer vorbereiteten Anweisung ab. Informationen zum Vorbereiten einer Anweisung finden Sie unter [sqlsrv_query](../content/sqlsrv_query.md) oder [sqlsrv_prepare](../content/sqlsrv_prepare.md). Beachten Sie, dass **sqlsrv\_field\_metadata** sowohl vor als auch nach der Ausführung von jeder Anweisung aufgerufen werden kann.  
  
## Syntax  
  
```  
  
sqlsrv_field_metadata( resource $stmt)  
```  
  
#### Parameter  
*$stmt*: Eine Anweisungsressource für die Feldmetadaten gewünscht werden.  
  
## Rückgabewert  
Ein **Array** von Arrays oder **false**. Das Array besteht aus einem Array für jedes Feld im Resultset. Jedes Teilarray hat Schlüssel, wie in der unten stehenden Tabelle beschrieben. Falls beim Abrufen der Feldmetadaten ein Fehler auftritt, wird **false** zurückgegeben.  
  
|Key|Beschreibung|  
|-------|---------------|  
|Name|Name der Spalte, der das Feld entspricht|  
|Typ|Numerischer Wert, der einem SQL-Typ entspricht|  
|Größe|Anzahl der Zeichen für Felder der Zeichentypen \(char\(n\), varchar\(n\), nchar\(n\), nvarchar\(n\), XML\). Anzahl der Bytes für Felder vom Typ „binär“ \(binary\(n\), varbinary\(n\), UDT\). **NULL** für andere SQL Server-Datentypen.|  
|Genauigkeit|Die Genauigkeit für die Typen mit variabler Genauigkeit \(real, numeric, decimal, datetime2, datetimeoffset und time\). **NULL** für andere SQL Server-Datentypen.|  
|Dezimalstellen|Die Skalierung für die Typen mit variabler Skalierung \(numeric, decimal, datetime2, datetimeoffset und time\). **NULL** für andere SQL Server-Datentypen.|  
|NULL zulassen|Ein Aufzählungswert, der anzeigt, ob die Spalte NULL-Werte zulässt \(**SQLSRV\_NULLABLE\_YES**\), oder nicht \(**SQLSRV\_NULLABLE\_NO**\), oder ob diese Eigenschaft nicht bekannt ist \(**SQLSRV\_NULLABLE\_UNKNOWN**\).|  
  
Die folgende Tabelle enthält mehr Informationen zu den Schlüsseln für jedes Teilarray \(weiter Informationen zu diesen Typen finden Sie in der Dokumentation zu SQL Server\):  
  
|SQL Server 2008-Datentyp|Typ|Min\/Max Precision|Min\/Max Scale|Größe|  
|-----------------------------|--------|----------------------|------------------|--------|  
|bigint|SQL\_BIGINT \(\-5\)|||8|  
|binary|SQL\_BINARY \(\-2\)|||0 < *n* < 8000 <sup>1</sup>|  
|bit|SQL\_BIT \(\-7\)||||  
|char|SQL\_CHAR \(1\)|||0 < *n* < 8000 <sup>1</sup>|  
|Datum|SQL\_TYPE\_DATE \(91\)|10\/10|0\/0||  
|datetime|SQL\_TYPE\_TIMESTAMP \(93\)|23\/23|3\/3||  
|datetime2|SQL\_TYPE\_TIMESTAMP \(93\)|19\/27|0\/7||  
|datetimeoffset|SQL\_SS\_TIMESTAMPOFFSET \(\-155\)|26\/34|0\/7||  
|decimal|SQL\_DECIMAL \(3\)|1\/38|0\/Genauigkeitswert||  
|float|SQL\_FLOAT \(6\)|4\/8|||  
|image|SQL\_LONGVARBINARY \(\-4\)|||2 GB|  
|int|SQL\_INTEGER \(4\)||||  
|money|SQL\_DECIMAL \(3\)|19\/19|4\/4||  
|nchar|SQL\_WCHAR \(\-8\)|||0 < *n* < 4000 <sup>1</sup>|  
|ntext|SQL\_WLONGVARCHAR \(\-10\)|||1 GB|  
|numeric|SQL\_NUMERIC \(2\)|1\/38|0\/Genauigkeitswert||  
|nvarchar|SQL\_WVARCHAR \(\-9\)|||0 < *n* < 4000 <sup>1</sup>|  
|real|SQL\_REAL \(7\)|4\/4|||  
|smalldatetime|SQL\_TYPE\_TIMESTAMP \(93\)|16\/16|0\/0||  
|smallint|SQL\_SMALLINT \(5\)|||2 Bytes|  
|Smallmoney|SQL\_DECIMAL \(3\)|10\/10|4\/4||  
|text|SQL\_LONGVARCHAR \(\-1\)|||2 GB|  
|Uhrzeit|SQL\_SS\_TIME2 \(\-154\)|8\/16|0\/7||  
|timestamp|SQL\_BINARY \(\-2\)|||8 Byte|  
|tinyint|SQL\_TINYINT \(\-6\)|||1 Byte|  
|udt|SQL\_SS\_UDT \(\-151\)|||variable|  
|uniqueidentifier|SQL\_GUID \(\-11\)|||16|  
|varbinary|SQL\_VARBINARY \(\-3\)|||0 < *n* < 8000 <sup>1</sup>|  
|varchar|SQL\_VARCHAR \(12\)|||0 < *n* < 8000 <sup>1</sup>|  
|xml|SQL\_SS\_XML \(\-152\)|||0|  
  
\(1\) Die Null \(0\) gibt an, das die Maximalgröße zulässig ist.  
  
Ein Schlüssel der NULL-Werte zulässt, kann entweder „Ja“ oder „Nein“ sein.  
  
## Beispiel  
Das folgende Beispiel erstellt eine Anweisungsressource, ruft  die Feldmetadaten ab und stellt sie dar. Das Beispiel setzt voraus, dass SQL Server und die [AdventureWorks](http://go.microsoft.com/fwlink/?LinkID=67739) -Datenbank auf dem lokalen Computer installiert sind. Wenn das Beispiel über die Befehlszeile ausgeführt wird, werden alle Ausgaben in die Konsole geschrieben.  
  
```  
<?php  
/* Connect to the local server using Windows Authentication and  
specify the AdventureWorks database as the database in use. */  
$serverName = "(local)";  
$connectionInfo = array( "Database"=>"AdventureWorks");  
$conn = sqlsrv_connect( $serverName, $connectionInfo);  
if( $conn === false )  
{  
     echo "Could not connect.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Prepare the statement. */  
$tsql = "SELECT ReviewerName, Comments FROM Production.ProductReview";  
$stmt = sqlsrv_prepare( $conn, $tsql);  
  
/* Get and display field metadata. */  
foreach( sqlsrv_field_metadata( $stmt) as $fieldMetadata)  
{  
      foreach( $fieldMetadata as $name => $value)  
      {  
           echo "$name: $value\n";  
      }  
      echo "\n";  
}  
  
/* Note: sqlsrv_field_metadata can be called on any statement  
resource, pre- or post-execution. */  
  
/* Free statement and connection resources. */  
sqlsrv_free_stmt( $stmt);  
sqlsrv_close( $conn);  
?>  
```  
  
## Siehe auch  
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
[Konstanten &#40;Microsoft-Treiber für PHP für SQL Server&#41;](../content/Constants--Microsoft-Drivers-for-PHP-for-SQL-Server-.md)  
[Informationen zu den Codebeispielen in der Dokumentation](../content/About-Code-Examples-in-the-Documentation.md)  
  
