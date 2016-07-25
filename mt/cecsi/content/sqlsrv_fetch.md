---
title: "sqlsrv_fetch"
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
  - sqlsrv_fetch
apitype: NA
ms.assetid: a5a640a1-6e7d-452e-8b66-850a4dc2ce89
caps.latest.revision: 39
caps.handback.revision: 38
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
# sqlsrv_fetch
Macht die nächste Zeile eines Resultsets zum Lesen verfügbar. Verwenden Sie [sqlsrv\_get\_field](../content/sqlsrv_get_field.md), um Felder einer Zeile zu lesen.  
  
## Syntax  
  
```  
  
sqlsrv_fetch( resource $stmt[, row[, ]offset])  
```  
  
#### Parameter  
*$stmt*: Eine Anweisungsressource, die einer ausgeführten Anweisung entspricht.  
  
> [!NOTE]  
> Eine Anweisung muss ausgeführt werden, bevor Ergebnisse abgerufen werden können. Informationen zur Ausführung einer Anweisung finden Sie unter [sqlsrv_query](../content/sqlsrv_query.md) und [sqlsrv_execute](../content/sqlsrv_execute.md).  
  
*row* \[OPTIONAL\]: Einer der folgenden Werte, der die Zeile spezifiziert, auf die in einem Resultset zugegriffen wird, welches einen scrollfähigen Cursor verwendet:  
  
-   SQLSRV\_SCROLL\_NEXT  
  
-   SQLSRV\_SCROLL\_PRIOR  
  
-   SQLSRV\_SCROLL\_FIRST  
  
-   SQLSRV\_SCROLL\_LAST  
  
-   SQLSRV\_SCROLL\_ABSOLUTE  
  
-   SQLSRV\_SCROLL\_RELATIVE  
  
Weitere Informationen zu diesen Werten finden Sie unter [Festlegen eines Cursortyps und Zeilenauswahl](../content/Specifying-a-Cursor-Type-and-Selecting-Rows.md).  
  
*offset* \[OPTIONAL\]: In Verbindung mit SQLSRV\_SCROLL\_ABSOLUTE und SQLSRV\_SCROLL\_RELATIVE verwendet, um die abzurufende Zeile anzugeben. Der erste Datensatz im Resultset ist „0“.  
  
## Rückgabewert  
Wenn die nächste Zeile des Resultsets erfolgreich abgerufen wurde, wird **true** zurückgegeben. Wenn keine weiteren Ergebnisse im Resultset vorhanden sind, wird **NULL** zurückgegeben. Wenn ein Fehler aufgetreten ist, wird **false** zurückgegeben.  
  
## Beispiel  
Im folgenden Beispiel wird **sqlsrv\_fetch** verwendet, um eine Zeile von Daten abzurufen, die eine Produktprüfung und den Namen des Bearbeiters enthält. Zum Abrufen von Daten aus dem Resultset wird [sqlsrv\_get\_field](../content/sqlsrv_get_field.md) verwendet. Das Beispiel setzt voraus, dass SQL Server und die [AdventureWorks](http://go.microsoft.com/fwlink/?LinkID=67739) -Datenbank auf dem lokalen Computer installiert sind. Wenn das Beispiel über die Befehlszeile ausgeführt wird, werden alle Ausgaben in die Konsole geschrieben.  
  
```  
<?php  
/*Connect to the local server using Windows Authentication and  
specify the AdventureWorks database as the database in use. */  
$serverName = "(local)";  
$connectionInfo = array( "Database"=>"AdventureWorks");  
$conn = sqlsrv_connect( $serverName, $connectionInfo);  
if( $conn === false )  
{  
     echo "Could not connect.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Set up and execute the query. Note that both ReviewerName and  
Comments are of SQL Server type nvarchar. */  
$tsql = "SELECT ReviewerName, Comments   
         FROM Production.ProductReview  
         WHERE ProductReviewID=1";  
$stmt = sqlsrv_query( $conn, $tsql);  
if( $stmt === false )  
{  
     echo "Error in statement preparation/execution.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Make the first row of the result set available for reading. */  
if( sqlsrv_fetch( $stmt ) === false)  
{  
     echo "Error in retrieving row.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Note: Fields must be accessed in order.  
Get the first field of the row. Note that no return type is  
specified. Data will be returned as a string, the default for  
a field of type nvarchar.*/  
$name = sqlsrv_get_field( $stmt, 0);  
echo "$name: ";  
  
/*Get the second field of the row as a stream.  
Because the default return type for a nvarchar field is a  
string, the return type must be specified as a stream. */  
$stream = sqlsrv_get_field( $stmt, 1,   
                            SQLSRV_PHPTYPE_STREAM( SQLSRV_ENC_CHAR));  
while( !feof( $stream ))  
{   
    $str = fread( $stream, 10000);  
    echo $str;  
}  
  
/* Free the statement and connection resources. */  
sqlsrv_free_stmt( $stmt);  
sqlsrv_close( $conn);  
?>  
```  
  
## Siehe auch  
[Abrufen von Daten](../content/Retrieving-Data.md)  
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
[Informationen zu den Codebeispielen in der Dokumentation](../content/About-Code-Examples-in-the-Documentation.md)  
  
