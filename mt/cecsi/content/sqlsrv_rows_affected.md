---
title: "sqlsrv_rows_affected"
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
  - sqlsrv_rows_affected
apitype: NA
ms.assetid: 6f43fbfc-fc92-449b-82d0-33fa780e8f09
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
# sqlsrv_rows_affected
Gibt die Anzahl von Zeilen zurück, die von der zuletzt ausgeführten Anweisung geändert wurden. Diese Funktion gibt nicht die Anzahl der von einer SELECT-Anweisung zurückgegebenen Zeilen zurück.  
  
## Syntax  
  
```  
  
sqlsrv_rows_affected( resource $stmt)  
```  
  
#### Parameter  
*$stmt*: Eine Anweisungsressource, die einer ausgeführten Anweisung entspricht.  
  
## Rückgabewert  
Eine ganze Zahl, die die Anzahl der Zeilen angibt, die durch die zuletzt ausgeführte Anweisung geändert wurden. Wenn keine Zeilen geändert wurden, wird Null \(0\) zurückgegeben. Wenn keine Informationen über die Anzahl der geänderten Zeilen verfügbar sind, wird die negative Eins \(\-1\) zurückgegeben. Wenn ein Fehler beim Abrufen der geänderten Zeilen aufgetreten ist, wird **false** zurückgegeben.  
  
## Beispiel  
Das folgende Beispiel zeigt die Anzahl der Zeilen, die durch eine UPDATE-Anweisung geändert wurden. Das Beispiel setzt voraus, dass SQL Server und die [AdventureWorks](http://go.microsoft.com/fwlink/?LinkID=67739) -Datenbank auf dem lokalen Computer installiert sind. Wenn das Beispiel über die Befehlszeile ausgeführt wird, werden alle Ausgaben in die Konsole geschrieben.  
  
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
         SET SpecialOfferID = ?   
         WHERE ProductID = ?";  
  
/* Set parameter values. */  
$params = array(2, 709);  
  
/* Execute the statement. */  
$stmt = sqlsrv_query( $conn, $tsql, $params);  
  
/* Get the number of rows affected and display appropriate message.*/  
$rows_affected = sqlsrv_rows_affected( $stmt);  
if( $rows_affected === false)  
{  
     echo "Error in calling sqlsrv_rows_affected.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
elseif( $rows_affected == -1)  
{  
      echo "No information available.\n";  
}  
else  
{  
      echo $rows_affected." rows were updated.\n";  
}  
  
/* Free statement and connection resources. */  
sqlsrv_free_stmt( $stmt);  
sqlsrv_close( $conn);  
?>  
```  
  
## Siehe auch  
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
[Informationen zu den Codebeispielen in der Dokumentation](../content/About-Code-Examples-in-the-Documentation.md)  
[Aktualisieren von Daten &#40;Microsoft-Treiber für PHP für SQL Server&#41;](../content/Updating-Data--Microsoft-Drivers-for-PHP-for-SQL-Server-.md)  
  
