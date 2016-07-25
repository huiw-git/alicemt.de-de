---
title: "sqlsrv_begin_transaction"
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
  - sqlsrv_begin_transaction
apitype: NA
ms.assetid: 0b223bc8-4047-4329-9cbf-d350ab0fb886
caps.latest.revision: 24
caps.handback.revision: 23
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
# sqlsrv_begin_transaction
Beginnt eine Transaktion für eine angegebene Verbindung Die aktuelle Transaktion enthält alle Anweisungen für die angegebene Verbindung, die nach dem Aufruf von **sqlsrv\_begin\_transaction** und vor allen Aufrufen von [sqlsrv_rollback](../content/sqlsrv_rollback.md) oder [sqlsrv_commit](../content/sqlsrv_commit.md) ausgeführt wurden.  
  
> [!NOTE]  
> [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] befindet sich im Autocommit\-Modus. Dies bedeutet, dass alle Abfragen bei Erfolg automatisch committet werden, es sei denn, sie wurden durch **sqlsrv\_begin\_transaction** als Teil einer expliziten Transaktion gekennzeichnet.  
  
> [!NOTE]  
> Wenn **sqlsrv\_begin\_transaction** aufgerufen wird, nachdem eine Transaktion bereits für die Verbindung initiiert, aber nicht durch Aufrufen von entweder **sqlsrv\_commit** oder **sqlsrv\_rollback** abgeschlossen wurde, gibt der Aufruf **false** zurück, und der Fehlerauflistung wird ein *Already in Transaction*-Fehler hinzugefügt.  
  
## Syntax  
  
```  
  
sqlsrv_begin_transaction( resource $conn)  
```  
  
#### Parameter  
*$conn*: Die Verbindung, der die Transaktion zugeordnet ist.  
  
## Rückgabewert  
Ein boolescher Wert: **true** , wenn die Transaktion erfolgreich gestartet wurde. Andernfalls lautet der Wert **false**.  
  
## Beispiel  
Im folgenden Beispiel werden zwei Abfragen im Rahmen einer Transaktion ausgeführt. Wenn beide Abfragen erfolgreich sind, wird die Transaktion committet. Wenn bei einer \(oder beiden\) Abfrage(n) ein Fehler auftritt, wird für die Transaktion ein Rollback ausgeführt.  
  
Die erste Abfrage im Beispiel fügt einen neuen Verkaufsauftrag in die *Sales.SalesOrderDetail* -Tabelle der AdventureWorks-Datenbank ein. Der Auftrag umfasst fünf Einheiten des Produkts, das die Produkt-ID 709 besitzt. In der zweiten Abfrage wird der Lagerbestand des Produkts mit der ID 709 um fünf Einheiten reduziert. Diese Abfragen werden in eine Transaktion aufgenommen, weil beide Abfragen erfolgreich ausgeführt werden müssen, damit die Datenbank den Status von Aufträgen und die Verfügbarkeit von Produkten korrekt widerspiegelt.  
  
Das Beispiel setzt voraus, dass SQL Server und die [AdventureWorks](http://go.microsoft.com/fwlink/?LinkID=67739) -Datenbank auf dem lokalen Computer installiert sind. Wenn das Beispiel über die Befehlszeile ausgeführt wird, werden alle Ausgaben in die Konsole geschrieben.  
  
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
     die( print_r( sqlsrv_errors(), true ));  
}  
  
/* Initiate transaction. */  
/* Exit script if transaction cannot be initiated. */  
if ( sqlsrv_begin_transaction( $conn ) === false )  
{  
     echo "Could not begin transaction.\n";  
     die( print_r( sqlsrv_errors(), true ));  
}  
  
/* Initialize parameter values. */  
$orderId = 43659; $qty = 5; $productId = 709;  
$offerId = 1; $price = 5.70;  
  
/* Set up and execute the first query. */  
$tsql1 = "INSERT INTO Sales.SalesOrderDetail   
                     (SalesOrderID,   
                      OrderQty,   
                      ProductID,   
                      SpecialOfferID,   
                      UnitPrice)  
          VALUES (?, ?, ?, ?, ?)";  
$params1 = array( $orderId, $qty, $productId, $offerId, $price);  
$stmt1 = sqlsrv_query( $conn, $tsql1, $params1 );  
  
/* Set up and execute the second query. */  
$tsql2 = "UPDATE Production.ProductInventory   
          SET Quantity = (Quantity - ?)   
          WHERE ProductID = ?";  
$params2 = array($qty, $productId);  
$stmt2 = sqlsrv_query( $conn, $tsql2, $params2 );  
  
/* If both queries were successful, commit the transaction. */  
/* Otherwise, rollback the transaction. */  
if( $stmt1 && $stmt2 )  
{  
     sqlsrv_commit( $conn );  
     echo "Transaction was committed.\n";  
}  
else  
{  
     sqlsrv_rollback( $conn );  
     echo "Transaction was rolled back.\n";  
}  
  
/* Free statement and connection resources. */  
sqlsrv_free_stmt( $stmt1);  
sqlsrv_free_stmt( $stmt2);  
sqlsrv_close( $conn);  
?>  
```  
  
Da wir uns auf die Überwachung des Transaktionsverhaltens konzentrieren, sind Teile der empfohlenen Fehlerbehandlung im vorherigen Beispiel nicht enthalten. Für eine Produktionsanwendung wird empfohlen, dass jeder Aufruf einer **sqlsrv** -Funktion auf Fehler überprüft und entsprechend behandelt wird.  
  
> [!NOTE]  
> Verwenden Sie eingebettetes Transact\-SQL nicht zum Ausführen von Transaktionen. Führen Sie z. B. keine Anweisung mit "BEGIN TRANSACTION" als Transact\-SQL-Abfrage aus, um eine Transaktion zu beginnen. Das erwartete Transaktionsverhalten kann nicht garantiert werden, wenn eingebettetes Transact\-SQL zum Durchführen von Transaktionen verwendet wird.  
  
## Siehe auch  
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
[Vorgehensweise: Ausführen von Transaktionen](../Topic/How%20to:%20Perform%20Transactions.md)  
[Übersicht zum PHP-SQL-Treiber](../content/Overview-of-the-PHP-SQL-Driver.md) 
  
