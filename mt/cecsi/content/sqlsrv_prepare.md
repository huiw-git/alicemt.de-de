---
title: "sqlsrv_prepare"
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
  - sqlsrv_prepare
apitype: NA
ms.assetid: 8c74c697-3296-4f5d-8fb9-e361f53f19a6
caps.latest.revision: 52
caps.handback.revision: 51
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
# sqlsrv_prepare
Erstellt eine Anweisungsressource, die mit der angegebenen Verbindung verknüpft ist. Diese Funktion ist nützlich für die Ausführung mehrerer Abfragen.  
  
## Syntax  
  
```  
  
sqlsrv_prepare( resource $conn, string $tsql [, array $params [, array $options]])  
```  
  
#### Parameter  
*$conn*: Mit der erstellten Anweisung verknüpfte Verbindungsressource.  
  
*$tsql*: Transact\-SQL-Ausdruck, der der erstellten Anweisung entspricht.  
  
*$params* \[OPTIONAL\]: Ein **Array** von Werten, die Parametern in einer parametrisierten Abfrage entsprechen. Jedes Element des Arrays kann eines der folgenden sein:  
  
-   Ein Literalwert  
  
-   Ein Verweis auf eine PHP-Variable.  
  
-   Ein **Array** mit der folgenden Struktur:  
  
    ```  
    array(&$value [, $direction [, $phpType [, $sqlType]]])  
    ```  
  
    > [!NOTE]  
    > Als Abfrageparameter übergebene Variablen sollten durch Verweis und nicht als Wert übergeben werden. Übergeben Sie beispielsweise `&$myVariable` anstelle von `$myVariable`. Beim Ausführen einer Abfrage mit Nach\-Wert-Parametern wird eine PHP-Warnung ausgelöst.  
  
    In der folgenden Tabelle sind die Elemente des Arrays beschrieben.  
  
    |Element|Beschreibung|  
    |-----------|---------------|  
    |*&$value*|Ein Literalwert oder ein Verweis auf eine PHP-Variable.|  
    |*$direction*\[OPTIONAL\]|Eine der folgenden verwendeten **SQLSRV\_PARAM\_\***-Konstanten, um die Parameterrichtung anzugeben: **SQLSRV\_PARAM\_IN**, **SQLSRV\_PARAM\_OUT**, **SQLSRV\_PARAM\_INOUT**. Der Standardwert ist **SQLSRV\_PARAM\_IN**.<br /><br />Weitere Informationen zu PHP-Konstanten finden Sie unter [Konstanten &#40;Microsoft-Treiber für PHP für SQL Server&#41;](../content/Constants--Microsoft-Drivers-for-PHP-for-SQL-Server-.md).|  
    |*$phpType*\[OPTIONAL\]|Eine **SQLSRV\_PHPTYPE\_\***-Konstante, die den PHP-Datentyp des zurückgegebenen Werts angibt.|  
    |*$sqlType*\[OPTIONAL\]|Eine **SQLSRV\_SQLTYPE\_\***-Konstante, die den SQL Server-Datentyp des Eingabewerts angibt.|  
  
*$options* \[OPTIONAL\]: Ein assoziatives Array, das Abfrageeigenschaften festlegt. In der folgenden Tabelle sind die unterstützten Schlüssel und die entsprechenden Werte aufgeführt:  
  
|Key|Unterstützte Werte|Beschreibung|  
|-------|--------------------|---------------|  
|QueryTimeout|Ein positiver ganzzahliger Wert|Legt das Abfragetimeout in Sekunden fest. Standardmäßig wartet der Treiber unbegrenzt auf Ergebnisse.|  
|SendStreamParamsAtExec|**WAHR** oder **FALSCH**<br /><br />Der Standardwert ist **true**.|Konfiguriert den Treiber, um alle Streamdaten bei der Ausführung zu senden \(**true**\) oder Streamdaten in Blöcken \(**false**\) zu senden. In der Standardeinstellung ist dieser Wert mit **true**festgelegt. Weitere Informationen finden Sie unter [sqlsrv_send_stream_data](../content/sqlsrv_send_stream_data.md).|  
|Bildlauffähigkeit|SQLSRV\_CURSOR\_FORWARD<br /><br />SQLSRV\_CURSOR\_STATIC<br /><br />SQLSRV\_CURSOR\_DYNAMIC<br /><br />SQLSRV\_CURSOR\_KEYSET<br /><br />SQLSRV\_CURSOR\_CLIENT\_BUFFERED|Weitere Informationen zu diesen Werten finden Sie unter [Festlegen eines Cursortyps und Zeilenauswahl](../content/Specifying-a-Cursor-Type-and-Selecting-Rows.md).|  
  
## Rückgabewert  
Eine Anweisungsressource. Wenn die Anweisungsressource nicht erstellt werden kann, wird **false** zurückgegeben.  
  
## Hinweise  
Wenn Sie eine Anweisung vorbereiten, die Variablen als Parameter verwendet, werden die Variablen an die Anweisung gebunden. Das bedeutet, dass die Anweisung beim nächsten Ausführen mit aktualisierten Parametern laufen wird, wenn Sie die Variablenwerte aktualisieren.  
  
Die Kombination von **sqlsrv\_prepare** und **sqlsrv\_execute** trennt Anweisungsvorbereitung und Ausführen der Anweisung in zwei Funktionsaufrufe und kann verwendet werden, um parametrisierte Abfragen ausführen. Diese Funktion eignet sich zum mehrfachen Ausführen einer Anweisung mit verschiedenen Parameterwerten für jede Ausführung.  
  
Alternative Strategien zum Schreiben und Lesen großer Datenmengen finden Sie unter [Batches von SQL-Anweisungen](http://go.microsoft.com/fwlink/?LinkId=104225) und [BULK INSERT](http://go.microsoft.com/fwlink/?LinkId=104226).  
  
Weitere Informationen finden Sie unter [How to: Retrieve Output Parameters Using the SQLSRV Driver](../Topic/How%20to:%20Retrieve%20Output%20Parameters%20Using%20the%20SQLSRV%20Driver.md).  
  
## Beispiel  
Im folgenden Beispiel wird eine Anweisung vorbereitet und ausgeführt. Wenn die Anweisung ausgeführt wird \(siehe [sqlsrv_execute](../content/sqlsrv_execute.md)\), aktualisiert diese ein Feld in der *Sales.SalesOrderDetail*-Tabelle der AdventureWorks-Datenbank. Das Beispiel setzt voraus, dass SQL Server und die [AdventureWorks](http://go.microsoft.com/fwlink/?LinkID=67739) -Datenbank auf dem lokalen Computer installiert sind. Wenn das Beispiel über die Befehlszeile ausgeführt wird, werden alle Ausgaben in die Konsole geschrieben.  
  
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
  
/* Set up Transact-SQL query. */  
$tsql = "UPDATE Sales.SalesOrderDetail   
         SET OrderQty = ?   
         WHERE SalesOrderDetailID = ?";  
  
/* Assign parameter values. */  
$param1 = 5;  
$param2 = 10;  
$params = array( &$param1, &$param2);  
  
/* Prepare the statement. */  
if( $stmt = sqlsrv_prepare( $conn, $tsql, $params))  
{  
      echo "Statement prepared.\n";  
}   
else  
{  
      echo "Statement could not be prepared.\n";  
      die( print_r( sqlsrv_errors(), true));  
}  
  
/* Execute the statement. */  
if( sqlsrv_execute( $stmt))  
{  
      echo "Statement executed.\n";  
}  
else  
{  
      echo "Statement could not be executed.\n";  
      die( print_r( sqlsrv_errors(), true));  
}  
  
/* Free the statement and connection resources. */  
sqlsrv_free_stmt( $stmt);  
sqlsrv_close( $conn);  
?>  
```  
  
## Beispiel  
Im folgenden Beispiel wird veranschaulicht, wie eine Anweisung vorbereitet wird und diese dann mit verschiedenen Parameterwerten erneut ausgeführt wird. Im Beispiel wird die *OrderQty* -Spalte der *Sales.SalesOrderDetail* -Tabelle der AdventureWorks-Datenbank aktualisiert. Nachdem die Updates abgeschlossen sind, wird die Datenbank abgefragt, um sicherzustellen, dass erfolgreich aktualisiert wurde. Das Beispiel setzt voraus, dass SQL Server und die [AdventureWorks](http://go.microsoft.com/fwlink/?LinkID=67739) -Datenbank auf dem lokalen Computer installiert sind. Wenn das Beispiel über die Befehlszeile ausgeführt wird, werden alle Ausgaben in die Konsole geschrieben.  
  
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
  
/* Define the parameterized query. */  
$tsql = "UPDATE Sales.SalesOrderDetail  
         SET OrderQty = ?  
         WHERE SalesOrderDetailID = ?";  
  
/* Initialize parameters and prepare the statement. Variables $qty  
and $id are bound to the statement, $stmt1. */  
$qty = 0; $id = 0;  
$stmt1 = sqlsrv_prepare( $conn, $tsql, array( &$qty, &$id));  
if( $stmt1 )  
{  
     echo "Statement 1 prepared.\n";  
}   
else   
{  
     echo "Error in statement preparation.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Set up the SalesOrderDetailID and OrderQty information. This array  
maps the order ID to order quantity in key=>value pairs. */  
$orders = array( 1=>10, 2=>20, 3=>30);  
  
/* Execute the statement for each order. */  
foreach( $orders as $id => $qty)  
{  
     // Because $id and $qty are bound to $stmt1, their updated  
     // values are used with each execution of the statement.   
     if( sqlsrv_execute( $stmt1) === false )  
     {  
          echo "Error in statement execution.\n";  
          die( print_r( sqlsrv_errors(), true));  
     }  
}  
echo "Orders updated.\n";  
  
/* Free $stmt1 resources.  This allows $id and $qty to be bound to a different statement.*/  
sqlsrv_free_stmt( $stmt1);  
  
/* Now verify that the results were successfully written by selecting   
the newly inserted rows. */  
$tsql = "SELECT OrderQty   
         FROM Sales.SalesOrderDetail   
         WHERE SalesOrderDetailID = ?";  
  
/* Prepare the statement. Variable $id is bound to $stmt2. */  
$stmt2 = sqlsrv_prepare( $conn, $tsql, array( &$id));  
if( $stmt2 )  
{  
     echo "Statement 2 prepared.\n";  
}   
else   
{  
     echo "Error in statement preparation.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Execute the statement for each order. */  
foreach( array_keys($orders) as $id)  
{  
     /* Because $id is bound to $stmt2, its updated value   
        is used with each execution of the statement. */  
     if( sqlsrv_execute( $stmt2))  
     {  
          sqlsrv_fetch( $stmt2);  
          $quantity = sqlsrv_get_field( $stmt2, 0);  
          echo "Order $id is for $quantity units.\n";  
     }  
     else  
     {  
          echo "Error in statement execution.\n";  
          die( print_r( sqlsrv_errors(), true));  
     }  
}  
  
/* Free $stmt2 and connection resources. */  
sqlsrv_free_stmt( $stmt2);  
sqlsrv_close( $conn);  
?>  
```  
  
## Siehe auch  
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
[Vorgehensweise: Ausführen von parametrisierten Abfragen](../Topic/How%20to:%20Perform%20Parameterized%20Queries.md)  
[Informationen zu den Codebeispielen in der Dokumentation](../content/About-Code-Examples-in-the-Documentation.md)  
[Vorgehensweise: Streamen von Daten](../Topic/How%20to:%20Send%20Data%20as%20a%20Stream.md)  
[Verwenden direktionaler Parameter](../content/Using-Directional-Parameters.md)  
[Abrufen von Daten](../content/Retrieving-Data.md)  
[Aktualisieren von Daten &#40;Microsoft-Treiber für PHP für SQL Server&#41;](../content/Updating-Data--Microsoft-Drivers-for-PHP-for-SQL-Server-.md)  
  
