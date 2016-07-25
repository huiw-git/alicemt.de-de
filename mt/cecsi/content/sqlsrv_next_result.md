---
title: "sqlsrv_next_result"
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
  - sqlsrv_next_result
apitype: NA
ms.assetid: 41270d16-0003-417c-b837-ea51439654cd
caps.latest.revision: 26
caps.handback.revision: 25
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
# sqlsrv_next_result
Aktiviert das nächste Ergebnis \(Resultset, Zeilenanzahl oder Ausgabeparameter\) der angegebenen Anweisung.  
  
> [!NOTE]  
> Das erste \(oder einzige\) Ergebnis, das von einer Batchabfrage oder gespeicherten Prozedur zurückgegeben wird, ist ohne einen Aufruf von **sqlsrv\_next\_result** aktiv.  
  
## Syntax  
  
```  
  
sqlsrv_next_result( resource $stmt )  
```  
  
#### Parameter  
*$stmt*: Die ausgeführte Anweisung, auf die das nächste Ergebnis aktiviert wird.  
  
## Rückgabewert  
Wenn das nächste Ergebnis erfolgreich aktiviert wurde, wird der boolesche Wert **true** zurückgegeben. Wenn beim Aktivieren des nächsten Ergebnisses ein Fehler auftritt, wird **false** zurückgegeben. Wenn keine weiteren Ergebnisse verfügbar sind, wird **NULL** zurückgegeben.  
  
## Beispiel  
Im folgenden Beispiel wird eine gespeicherte Prozedur erstellt und ausgeführt, die eine Produktprüfung in die *Production.ProductReview* -Tabelle einfügt und dann alle Bewertungen für das angegebene Produkt wählt. Nach der Ausführung der gespeicherten Prozedur wird das erste Ergebnis \(die Anzahl der Zeilen, die von der INSERT-Abfrage in der gespeicherten Prozedur betroffen sind\) genutzt, ohne **sqlsrv\_next\_result** aufzurufen. Das nächste Ergebnis \(die von der SELECT-Abfrage in der gespeicherten Prozedur zurückgegebenen Zeilen\) wird durch Aufrufen von **sqlsrv\_next\_result** zur Verfügung gestellt und mit [sqlsrv_fetch_array](../content/sqlsrv_fetch_array.md) verarbeitet.  
  
> [!NOTE]  
> Die Verwendung kanonischer Syntax stellt die empfohlene Vorgehensweise für das Abrufen gespeicherter Prozeduren dar. Weitere Informationen zur kanonischen Syntax finden Sie unter [Aufrufen einer gespeicherten Prozedur](http://go.microsoft.com/fwlink/?linkid=119517).  
  
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
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Drop the stored procedure if it already exists. */  
$tsql_dropSP = "IF OBJECT_ID('InsertProductReview', 'P') IS NOT NULL  
                DROP PROCEDURE InsertProductReview";  
$stmt1 = sqlsrv_query( $conn, $tsql_dropSP);  
if( $stmt1 === false )  
{  
     echo "Error in executing statement 1.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Create the stored procedure. */  
$tsql_createSP = " CREATE PROCEDURE InsertProductReview  
                                    @ProductID int,  
                                    @ReviewerName nvarchar(50),  
                                    @ReviewDate datetime,  
                                    @EmailAddress nvarchar(50),  
                                    @Rating int,  
                                    @Comments nvarchar(3850)  
                   AS  
                       BEGIN  
                             INSERT INTO Production.ProductReview   
                                         (ProductID,  
                                          ReviewerName,  
                                          ReviewDate,  
                                          EmailAddress,  
                                          Rating,  
                                          Comments)  
                                    VALUES  
                                         (@ProductID,  
                                          @ReviewerName,  
                                          @ReviewDate,  
                                          @EmailAddress,  
                                          @Rating,  
                                          @Comments);  
                             SELECT * FROM Production.ProductReview  
                                WHERE ProductID = @ProductID;  
                       END";  
$stmt2 = sqlsrv_query( $conn, $tsql_createSP);  
  
if( $stmt2 === false)  
{  
     echo "Error in executing statement 2.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
/*-------- The next few steps call the stored procedure. --------*/  
  
/* Define the Transact-SQL query. Use question marks (?) in place of the  
parameters to be passed to the stored procedure */  
$tsql_callSP = "{call InsertProductReview(?, ?, ?, ?, ?, ?)}";  
  
/* Define the parameter array. */  
$productID = 709;  
$reviewerName = "Customer Name";  
$reviewDate = "2008-02-12";  
$emailAddress = "customer@email.com";  
$rating = 3;  
$comments = "[Insert comments here.]";  
$params = array(   
                 $productID,  
                 $reviewerName,  
                 $reviewDate,  
                 $emailAddress,  
                 $rating,  
                 $comments  
               );  
  
/* Execute the query. */  
$stmt3 = sqlsrv_query( $conn, $tsql_callSP, $params);  
if( $stmt3 === false)  
{  
     echo "Error in executing statement 3.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Consume the first result (rows affected by INSERT query in the  
stored procedure) without calling sqlsrv_next_result. */  
echo "Rows affectd: ".sqlsrv_rows_affected($stmt3)."-----\n";  
  
/* Move to the next result and display results. */  
$next_result = sqlsrv_next_result($stmt3);  
if( $next_result )  
{  
     echo "\nReview information for product ID ".$productID.".---\n";  
     while( $row = sqlsrv_fetch_array( $stmt3, SQLSRV_FETCH_ASSOC))  
     {  
          echo "ReviewerName: ".$row['ReviewerName']."\n";  
          echo "ReviewDate: ".date_format($row['ReviewDate'],  
                                             "M j, Y")."\n";  
          echo "EmailAddress: ".$row['EmailAddress']."\n";  
          echo "Rating: ".$row['Rating']."\n\n";  
     }  
}  
elseif( is_null($next_result))  
{  
     echo "No more results.\n";  
}  
else  
{  
     echo "Error in moving to next result.\n";  
     die(print_r(sqlsrv_errors(), true));  
}  
  
/* Free statement and connection resources. */  
sqlsrv_free_stmt( $stmt1 );  
sqlsrv_free_stmt( $stmt2 );  
sqlsrv_free_stmt( $stmt3 );  
sqlsrv_close( $conn );  
?>  
```  
  
Beim Ausführen einer gespeicherten Prozedur, die Ausgabeparameter besitzt, wird empfohlen, dass alle anderen Ergebnisse verarbeitet werden, bevor der Zugriff auf die Werte von Ausgabeparametern erfolgt. Weitere Informationen finden Sie unter [Vorgehensweise: Angeben der Parameterrichtung mit dem SQLSRV-Treiber](../Topic/How%20to:%20Specify%20Parameter%20Direction%20Using%20the%20SQLSRV%20Driver.md)  
  
## Beispiel  
Im folgenden Beispiel wird eine Batchabfrage durchgeführt, die eine Produktprüfungsinformation für eine angegebene Produkt-ID abruft, dann eine Prüfung für das Produkt einfügt und anschließend erneut die Produktprüfungsinformationen für die angegebene Produkt-ID abruft. Die neu eingefügte Produktprüfung wird im endgültigen Resultset der Batchabfrage enthalten sein. Im Beispiel wird [sqlsrv\_next\_result](../content/sqlsrv_next_result.md) verwendet, um von einem Ergebnis der Batchabfrage zum nächsten zu wechseln.  
  
> [!NOTE]  
> Das erste \(oder einzige\) Ergebnis, das von einer Batchabfrage oder gespeicherten Prozedur zurückgegeben wird, ist ohne einen Aufruf von **sqlsrv\_next\_result** aktiv.  
  
Im Beispiel wird die *Purchasing.ProductReview*-Tabelle mit der [AdventureWorks-Datenbank](http://go.microsoft.com/fwlink/?linkid=67739) verwendet. Es wird vorausgesetzt, dass diese Datenbank auf dem Server installiert ist. Wenn das Beispiel über die Befehlszeile ausgeführt wird, werden alle Ausgaben in die Konsole geschrieben.  
  
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
  
/* Define the batch query. */  
$tsql = "--Query 1  
         SELECT ProductID, ReviewerName, Rating   
         FROM Production.ProductReview   
         WHERE ProductID=?;  
  
         --Query 2  
         INSERT INTO Production.ProductReview (ProductID,   
                                               ReviewerName,   
                                               ReviewDate,   
                                               EmailAddress,   
                                               Rating)  
         VALUES (?, ?, ?, ?, ?);  
  
         --Query 3  
         SELECT ProductID, ReviewerName, Rating   
         FROM Production.ProductReview   
         WHERE ProductID=?;";  
  
/* Assign parameter values and execute the query. */  
$params = array(798,   
                798,   
                'CustomerName',   
                '2008-4-15',   
                'test@customer.com',   
                3,   
                798 );  
$stmt = sqlsrv_query($conn, $tsql, $params);  
if( $stmt === false )  
{  
     echo "Error in statement execution.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Retrieve and display the first result. */  
echo "Query 1 result:\n";  
while( $row = sqlsrv_fetch_array( $stmt, SQLSRV_FETCH_NUMERIC ))  
{  
     print_r($row);  
}  
  
/* Move to the next result of the batch query. */  
sqlsrv_next_result($stmt);  
  
/* Display the result of the second query. */  
echo "Query 2 result:\n";  
echo "Rows Affected: ".sqlsrv_rows_affected($stmt)."\n";  
  
/* Move to the next result of the batch query. */  
sqlsrv_next_result($stmt);  
  
/* Retrieve and display the third result. */  
echo "Query 3 result:\n";  
while( $row = sqlsrv_fetch_array( $stmt, SQLSRV_FETCH_NUMERIC ))  
{  
     print_r($row);  
}  
  
/* Free statement and connection resources. */  
sqlsrv_free_stmt( $stmt );  
sqlsrv_close( $conn );  
?>  
```  
  
## Siehe auch  
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
[Informationen zu den Codebeispielen in der Dokumentation](../content/About-Code-Examples-in-the-Documentation.md)  
[Abrufen von Daten](../content/Retrieving-Data.md)  
[Aktualisieren von Daten &#40;Microsoft-Treiber für PHP für SQL Server&#41;](../content/Updating-Data--Microsoft-Drivers-for-PHP-for-SQL-Server-.md)  
[Beispielanwendung &#40;SQLSRV-Treiber&#41;](../content/Example-Application--SQLSRV-Driver-.md)  
  
