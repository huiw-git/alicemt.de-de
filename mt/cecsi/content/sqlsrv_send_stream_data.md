---
title: "sqlsrv_send_stream_data"
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
  - sqlsrv_send_stream_data
apitype: NA
ms.assetid: 826c2d45-694f-42b8-b12b-cd4523a31883
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
# sqlsrv_send_stream_data
Sendet Daten aus Parameterstreams an den Server. Mit jedem Aufruf werden bis zu acht Kilobyte \(8 KB\) Daten an **sqlsrv\_send\_stream\_data** gesendet.  
  
> [!NOTE]  
> In der Standardeinstellung werden alle Streamdaten an den Server gesendet, wenn eine Abfrage ausgeführt wird. Wenn dieses Standardverhalten nicht geändert wird, müssen Sie **sqlsrv\_send\_stream\_data** nicht verwenden, um Datenstromdaten an den Server zu senden. Informationen zum Ändern des Standardverhaltens finden Sie im Parameter-Abschnitt [sqlsrv_query](../content/sqlsrv_query.md) oder [sqlsrv_prepare](../content/sqlsrv_prepare.md).  
  
## Syntax  
  
```  
  
sqlsrv_send_stream_data( resource $stmt)  
```  
  
#### Parameter  
*$stmt*: Eine Anweisungsressource, die einer ausgeführten Anweisung entspricht.  
  
## Rückgabewert  
Boolescher Wert: **true** wenn weitere Daten gesendet werden sollen. Andernfalls lautet der Wert **false**.  
  
## Beispiel  
Im folgenden Beispiel wird eine Produktprüfung als Stream geöffnet und an den Server gesendet. Das Standardverhalten, alle Streamdaten zum Zeitpunkt der Ausführung zu senden, ist deaktiviert. Das Beispiel setzt voraus, dass SQL Server und die [AdventureWorks](http://go.microsoft.com/fwlink/?LinkID=67739) -Datenbank auf dem lokalen Computer installiert sind. Wenn das Beispiel über die Befehlszeile ausgeführt wird, werden alle Ausgaben in die Konsole geschrieben.  
  
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
  
/* Define the query. */  
$tsql = "UPDATE Production.ProductReview   
         SET Comments = ( ?)   
         WHERE ProductReviewID = 3";  
  
/* Open parameter data as a stream and put it in the $params array. */  
$comment = fopen( "data://text/plain,[ Insert lengthy comment.]", "r");  
$params = array( &$comment);  
  
/* Prepare the statement. Use the $options array to turn off the  
default behavior, which is to send all stream data at the time of query  
execution. */  
$options = array("SendStreamParamsAtExec"=>0);  
$stmt = sqlsrv_prepare( $conn, $tsql, $params, $options);  
  
/* Execute the statement. */  
sqlsrv_execute( $stmt);  
  
/* Send up to 8K of parameter data to the server with each call to  
sqlsrv_send_stream_data. Count the calls. */  
$i = 1;  
while( sqlsrv_send_stream_data( $stmt))   
{  
      echo "$i call(s) made.\n";  
      $i++;  
}  
  
/* Free statement and connection resources. */  
sqlsrv_free_stmt( $stmt);  
sqlsrv_close( $conn);  
?>  
```  
  
## Siehe auch  
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
[Aktualisieren von Daten &#40;Microsoft-Treiber für PHP für SQL Server&#41;](../content/Updating-Data--Microsoft-Drivers-for-PHP-for-SQL-Server-.md)  
[Informationen zu den Codebeispielen in der Dokumentation](../content/About-Code-Examples-in-the-Documentation.md)  
  
