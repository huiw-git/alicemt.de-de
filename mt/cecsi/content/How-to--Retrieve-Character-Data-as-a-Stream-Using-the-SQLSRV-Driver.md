---
title: "Vorgehensweise: Abrufen von Zeichendaten als Stream mit dem SQLSRV-Treiber"
ms.custom: na
ms.date: 06/16/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3c0dbca4-abfc-4449-b133-66c819681840
caps.latest.revision: 27
caps.handback.revision: 26
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
# Vorgehensweise: Abrufen von Zeichendaten als Stream mit dem SQLSRV-Treiber
Das Abrufen von Daten als Stream ist nur im SQLSRV-Treiber von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] und nicht im PDO\_SQLSRV-Treiber verfügbar.  
  
Der SQLSRV-Treiber nutzt PHP-Streams zum Abrufen großer Datenmengen vom Server. Im Beispiel in diesem Thema wird veranschaulicht, wie Zeichendaten als Stream abgerufen werden.  
  
## Beispiel  
Im folgenden Beispiel wird eine einzelne Zeile von der *Production.ProductReview* -Tabelle der AdventureWorks-Datenbank abgerufen. Das *Comments*-Feld der zurückgegebenen Zeile wird als Stream abgerufen und mithilfe der PHP-Funktion [fpassthru](http://go.microsoft.com/fwlink/?LinkId=217496) angezeigt.  
  
Das Abrufen von Daten als Stream erfolgt mithilfe von [sqlsrv_fetch](../content/sqlsrv_fetch.md) und [sqlsrv_get_field](../content/sqlsrv_get_field.md) als Zeichenstream spezifizierten Rückgabetyp. Der Rückgabetyp wird mithilfe der Konstanten **SQLSRV\_PHPTYPE\_STREAM** angegeben. Informationen zu **sqlsrv**-Konstanten finden Sie unter [Konstanten &#40;Microsoft-Treiber für PHP für SQL Server&#41;](../content/Constants--Microsoft-Drivers-for-PHP-for-SQL-Server-.md).  
  
Das Beispiel setzt voraus, dass [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] und die [AdventureWorks](http://go.microsoft.com/fwlink/?LinkID=67739) -Datenbank auf dem lokalen Computer installiert sind. Wenn das Beispiel über die Befehlszeile ausgeführt wird, werden alle Ausgaben in die Konsole geschrieben.  
  
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
  
/* Set up the Transact-SQL query. */  
$tsql = "SELECT ReviewerName,   
               CONVERT(varchar(32), ReviewDate, 107) AS [ReviewDate],  
               Rating,   
               Comments   
         FROM Production.ProductReview   
         WHERE ProductReviewID = ? ";  
  
/* Set the parameter value. */  
$productReviewID = 1;  
$params = array( $productReviewID);  
  
/* Execute the query. */  
$stmt = sqlsrv_query($conn, $tsql, $params);  
if( $stmt === false )  
{  
     echo "Error in statement execution.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Retrieve and display the data. The first three fields are retrieved  
as strings and the fourth as a stream with character encoding. */  
if(sqlsrv_fetch( $stmt ) === false )  
{  
     echo "Error in retrieving row.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
echo "Name: ".sqlsrv_get_field( $stmt, 0 )."\n";  
echo "Date: ".sqlsrv_get_field( $stmt, 1 )."\n";  
echo "Rating: ".sqlsrv_get_field( $stmt, 2 )."\n";  
echo "Comments: ";  
$comments = sqlsrv_get_field( $stmt, 3,   
                             SQLSRV_PHPTYPE_STREAM(SQLSRV_ENC_CHAR));  
fpassthru($comments);  
  
/* Free the statement and connection resources. */  
sqlsrv_free_stmt( $stmt);  
sqlsrv_close( $conn);  
?>  
```  
  
Die ersten drei Felder werden entsprechend des jeweiligen PHP-Standardtyps zurückgegeben, da für sie kein PHP-Rückgabetyp angegeben ist. Informationen zu PHP-Datentypen finden Sie unter [Default PHP Data Types](../content/Default-PHP-Data-Types.md). Weitere Informationen zum Angeben von PHP-Rückgabetypen finden Sie unter [How to: Specify PHP Data Types](../Topic/How%20to:%20Specify%20PHP%20Data%20Types.md).  
  
## Siehe auch  
[Abrufen von Daten](../content/Retrieving-Data.md)  
[Abrufen von Daten als Stream mit dem SQLSRV-Treiber](../content/Retrieving-Data-as-a-Stream-Using-the-SQLSRV-Driver.md)  
[Informationen zu den Codebeispielen in der Dokumentation](../content/About-Code-Examples-in-the-Documentation.md)  
  
