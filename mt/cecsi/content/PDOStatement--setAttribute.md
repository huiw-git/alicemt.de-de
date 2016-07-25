---
title: "PDOStatement::setAttribute"
ms.custom: na
ms.date: 07/18/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 329d9b5e-1c5d-40b0-9127-1051d0646fc7
caps.latest.revision: 20
caps.handback.revision: 19
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
# PDOStatement::setAttribute
Legt einen Attributwert fest. Entweder ein vordefiniertes PDO-Attribut oder ein benutzerdefiniertes Treiberattribut.  
  
## Syntax  
  
```  
  
bool PDOStatement::setAttribute ($attribute, $value );  
```  
  
#### Parameter  
$*attribute*: Eine ganze Zahl, eine der Konstanten PDO::ATTR\_\* oder PDO::SQLSRV\_ATTR\_\*-Konstanten. Eine Liste der verfügbaren Attribute finden Sie im Abschnitt „Anmerkungen“.  
  
$*value*: Der \(gemischte\) Wert, der für die angegebene $*attribute* festgelegt werden soll.  
  
## Rückgabewert  
„true“ bei Erfolg, andernfalls „false“.  
  
## Hinweise  
Die folgende Tabelle enthält die Liste mit den verfügbaren Attributen:  
  
|Attribut|Werte|Beschreibung|  
|-------------|----------|---------------|  
|PDO::SQLSRV\_ATTR\_CLIENT\_BUFFER\_MAX\_KB\_SIZE|1 bis zur Grenze des PHP-Speichers.|Konfiguriert die Größe des Puffers, der das Resultset für einen clientseitigen Cursor enthält.<br /><br />Die Standardeinstellung ist 10240 KB \(10 MB\).<br /><br />Weitere Informationen zu clientseitigen Cursorn finden Sie unter [Cursortypen &#40;PDO_SQLSRV-Treiber&#41;](../Topic/Cursor%20Types%20(PDO_SQLSRV%20Driver).md).|  
|PDO::SQLSRV\_ATTR\_ENCODING|Integer<br /><br />PDO::SQLSRV\_ENCODING\_UTF8 \(Standardwert\)<br /><br />PDO::SQLSRV\_ENCODING\_SYSTEM<br /><br />PDO::SQLSRV\_ENCODING\_BINARY|Legt die Zeichensatzcodierung fest, die vom Treiber verwendet wird, um mit dem Server zu kommunizieren.|  
|PDO::SQLSRV\_ATTR\_QUERY\_TIMEOUT|Integer|Legt das Abfragetimeout in Sekunden fest.<br /><br />Standardmäßig wartet der Treiber unbegrenzt auf Ergebnisse. Negative Zahlen sind nicht zulässig.<br /><br />„0“ bedeutet „kein Timeout“.|  
  
## Beispiel  
  
```  
<?php  
$database = "AdventureWorks";  
$server = "(local)";  
$conn = new PDO( "sqlsrv:server=$server ; Database = $database", "", "", array('MultipleActiveResultSets'=>false )  );  
  
$stmt = $conn->prepare('SELECT * FROM Person.ContactType');  
  
echo $stmt->getAttribute( constant( "PDO::ATTR_CURSOR" ) );  
  
echo "\n";  
  
$stmt->setAttribute(PDO::SQLSRV_ATTR_QUERY_TIMEOUT, 2);  
echo $stmt->getAttribute( constant( "PDO::SQLSRV_ATTR_QUERY_TIMEOUT" ) );  
?>  
```  
  
## Siehe auch  
[PDOStatement-Klasse](../content/PDOStatement-Class.md)  
[PDO](http://go.microsoft.com/fwlink/?LinkID=187441)  
  
