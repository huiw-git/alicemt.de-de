---
title: "sqlsrv_num_rows"
ms.custom: na
ms.date: 07/18/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c832210e-bb2a-47b5-a505-160b02d1d95e
caps.latest.revision: 13
caps.handback.revision: 12
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
# sqlsrv_num_rows
Berichtet über die Anzahl der Zeilen in einem Resultset.  
  
## Syntax  
  
```  
  
sqlsrv_num_rows( resource $stmt )  
```  
  
#### Parameter  
*$stmt*: Das Resultset für das die Zeilen gezählt werden sollen.  
  
## Rückgabewert  
Falls es bei der Berechnung der Anzahl der Zeilen einen Fehler gab, wird**false** zurückgegeben. Ansonsten gibt der Befehl die Anzahl der Zeilen im Resultset zurück.  
  
## Hinweise  
sqlsrv\_num\_rows erfordert einen clientseitigen, statischen oder Keysetcursor und gibt **false** zurück wenn Sie einen Vorwärtscursor oder einen dynamischen Cursor verwenden. \(Standard ist der Vorwärtscursor.\) Weitere Informationen zu Cursorn finden Sie unter [sqlsrv_query](../content/sqlsrv_query.md) und [Cursortypen &#40;SQLSRV-Treiber&#41;](../Topic/Cursor%20Types%20(SQLSRV%20Driver).md).  
  
## Beispiel  
  
```  
<?php  
   $server = "server_name";  
   $conn = sqlsrv_connect( $server, array( 'Database' => 'Northwind' ) );  
  
   $stmt = sqlsrv_query( $conn, "select * from orders where CustomerID = 'VINET'" , array(), array( "Scrollable" => SQLSRV_CURSOR_KEYSET ));  
  
   $row_count = sqlsrv_num_rows( $stmt );  
  
   if ($row_count === false)  
      echo "\nerror\n";  
   else if ($row_count >=0)  
      echo "\n$row_count\n";  
?>  
```  
  
Das folgende Beispiel zeigt, das, wenn es mehr als ein Resultset gibt, \(eine Batchabfrage\) die Anzahl der Zeilen nur verfügbar ist, wenn Sie einen clientseitigen Cursor verwenden.  
  
```  
<?php  
$serverName = "(local)";  
$connectionInfo = array("Database"=>"AdventureWorks");  
$conn = sqlsrv_connect( $serverName, $connectionInfo);  
  
$tsql = "select * from HumanResources.Department";  
  
// Client-side cursor and batch statements  
$tsql = "select top 2 * from HumanResources.Employee;Select top 3 * from HumanResources.EmployeeAddress";  
  
// works  
$stmt = sqlsrv_query($conn, $tsql, array(), array("Scrollable"=>"buffered"));  
  
// fails  
// $stmt = sqlsrv_query($conn, $tsql);  
// $stmt = sqlsrv_query($conn, $tsql, array(), array("Scrollable"=>"forward"));  
// $stmt = sqlsrv_query($conn, $tsql, array(), array("Scrollable"=>"static"));  
// $stmt = sqlsrv_query($conn, $tsql, array(), array("Scrollable"=>"keyset"));  
// $stmt = sqlsrv_query($conn, $tsql, array(), array("Scrollable"=>"dynamic"));  
  
$row_count = sqlsrv_num_rows( $stmt );  
echo "\nRow count for first result set = $row_count\n";  
  
sqlsrv_next_result($stmt);  
  
$row_count = sqlsrv_num_rows( $stmt );  
echo "\nRow count for second result set = $row_count\n";  
?>  
```  
  
## Siehe auch  
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
  
