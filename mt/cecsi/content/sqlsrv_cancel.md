---
title: "sqlsrv_cancel"
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
  - sqlsrv_cancel
apitype: NA
ms.assetid: 75798c9b-f711-445d-9b8f-ba4d405ca50a
caps.latest.revision: 32
caps.handback.revision: 31
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
# sqlsrv_cancel
Bricht eine Anweisung ab. Dies bedeutet, dass alle ausstehenden Ergebnisse für die Anweisung verworfen werden. Nachdem diese Funktion aufgerufen wurde, kann die Anweisung erneut ausgeführt werden, wenn sie mit [sqlsrv_prepare](../content/sqlsrv_prepare.md) vorbereitet wurde. Das Aufrufen dieser Funktion ist nicht erforderlich, wenn alle Ergebnisse, die der Anweisung zugeordnet sind, verwendet wurden.  
  
## Syntax  
  
```  
  
sqlsrv_cancel( resource $stmt)  
```  
  
#### Parameter  
*$stmt*: Die Anweisung, die abgebrochen werden soll.  
  
## Rückgabewert  
Ein boolescher Wert: **true** , wenn der Vorgang erfolgreich war. Andernfalls lautet der Wert **false**.  
  
## Beispiel  
Das folgende Beispiel nimmt die [AdventureWorks](http://go.microsoft.com/fwlink/?LinkID=67739)-Datenbank als Ziel zur Ausführung einer Abfrage. Es werden dann Ergebnisse verarbeitet und gezählt, bis die Variable *$salesTotal* einen angegebenen Betrag erreicht. Die verbleibenden Abfrageergebnisse werden anschließend verworfen. Das Beispiel setzt voraus, dass SQL Server und die AdventureWorks-Datenbank auf dem lokalen Computer installiert sind. Wenn das Beispiel über die Befehlszeile ausgeführt wird, werden alle Ausgaben in die Konsole geschrieben.  
  
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
  
/* Prepare and execute the query. */  
$tsql = "SELECT OrderQty, UnitPrice FROM Sales.SalesOrderDetail";  
$stmt = sqlsrv_prepare( $conn, $tsql);  
if( $stmt === false )  
{  
     echo "Error in statement preparation.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
if( sqlsrv_execute( $stmt ) === false)  
{  
     echo "Error in statement execution.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Initialize tracking variables. */  
$salesTotal = 0;  
$count = 0;  
  
/* Count and display the number of sales that produce revenue  
of $100,000. */  
while( ($row = sqlsrv_fetch_array( $stmt)) && $salesTotal <=100000)  
{  
     $qty = $row[0];  
     $price = $row[1];  
     $salesTotal += ( $price * $qty);  
     $count++;  
}  
echo "$count sales accounted for the first $$salesTotal in revenue.\n";  
  
/* Cancel the pending results. The statement can be reused. */  
sqlsrv_cancel( $stmt);  
?>  
```  
  
## Kommentare  
Eine Anweisung, die mit der Kombination von [sqlsrv_prepare](../content/sqlsrv_prepare.md) und [sqlsrv_execute](../content/sqlsrv_execute.md) vorbereitet und ausgeführt wird, kann erneut mit **sqlsrv\_execute** nach dem Aufruf von **sqlsrv\_cancel** ausgeführt werden. Eine Anweisung, die mit [sqlsrv_query](../content/sqlsrv_query.md) ausgeführt wird, kann nach dem Aufruf von **sqlsrv\_cancel** nicht erneut ausgeführt werden.  
  
## Siehe auch  
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
[Verbinden mit dem Server](../content/Connecting-to-the-Server.md)  
[Abrufen von Daten](../content/Retrieving-Data.md)  
[Informationen zu den Codebeispielen in der Dokumentation](../content/About-Code-Examples-in-the-Documentation.md)  
[sqlsrv_free_stmt](../content/sqlsrv_free_stmt.md)  
  
