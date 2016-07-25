---
title: "Vorgehensweise: Abrufen von Bin&#228;rdaten als Stream mithilfe des SQLSRV-Treibers"
ms.custom: na
ms.date: 06/16/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cd8d6382-abe6-48ee-9d10-4e6c52c0cb9a
caps.latest.revision: 21
caps.handback.revision: 20
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
# Vorgehensweise: Abrufen von Bin&#228;rdaten als Stream mithilfe des SQLSRV-Treibers
Das Abrufen von Daten als Stream ist nur im SQLSRV-Treiber von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] und nicht im PDO\_SQLSRV-Treiber verfügbar.  
  
 [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] nutzt PHP-Streams zum Abrufen großer Binärdatenmengen vom Server. Dieses Thema veranschaulicht, wie Binärdaten als Stream abgerufen werden.  
  
Verwenden der Streams zum Abrufen von Binärdaten, z. B. Bildern, verzichtet auf die Verwendung großer Mengen Skriptspeicher, indem nur Datenblöcke und nicht ganze Objekte in den Skriptspeicher geladen werden.  
  
## Beispiel  
Im folgenden Beispiel werden Binärdaten, z. B. ein Bild, aus der *Production.ProductPhoto* -Tabelle der AdventureWorks-Datenbank abgerufen. Das Bild wird als Stream abgerufen und im Browser angezeigt.  
  
Das Abrufen von Bilddaten als Stream erfolgt mithilfe von [sqlsrv_fetch](../content/sqlsrv_fetch.md) und [sqlsrv_get_field](../content/sqlsrv_get_field.md) mit einem binären Stream als Rückgabetyp. Der Rückgabetyp wird mithilfe der Konstanten **SQLSRV\_PHPTYPE\_STREAM** angegeben. Informationen zu **sqlsrv**-Konstanten finden Sie unter [Konstanten &#40;Microsoft-Treiber für PHP für SQL Server&#41;](../content/Constants--Microsoft-Drivers-for-PHP-for-SQL-Server-.md).  
  
Das Beispiel setzt voraus, dass SQL Server und die [AdventureWorks](http://go.microsoft.com/fwlink/?LinkID=67739) -Datenbank auf dem lokalen Computer installiert sind. Wenn das Beispiel über den Browser ausgeführt wird, werden alle Ausgaben im Browser geschrieben.  
  
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
  
/* Set up the Transact-SQL query. */  
$tsql = "SELECT LargePhoto   
         FROM Production.ProductPhoto   
         WHERE ProductPhotoID = ?";  
  
/* Set the parameter values and put them in an array. */  
$productPhotoID = 70;  
$params = array( $productPhotoID);  
  
/* Execute the query. */  
$stmt = sqlsrv_query($conn, $tsql, $params);  
if( $stmt === false )  
{  
     echo "Error in statement execution.</br>";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Retrieve and display the data.  
The return data is retrieved as a binary stream. */  
if ( sqlsrv_fetch( $stmt ) )  
{  
   $image = sqlsrv_get_field( $stmt, 0,   
                      SQLSRV_PHPTYPE_STREAM(SQLSRV_ENC_BINARY));  
   header("Content-Type: image/jpg");  
   fpassthru($image);  
}  
else  
{  
     echo "Error in retrieving data.</br>";  
     die(print_r( sqlsrv_errors(), true));  
}  
  
/* Free statement and connection resources. */  
sqlsrv_free_stmt( $stmt);  
sqlsrv_close( $conn);  
?>  
```  
  
Die Angabe des Rückgabetyps im Beispiel veranschaulicht, wie der PHP-Rückgabetyp als binärer Stream angegeben wird. Technisch gesehen ist er nicht zwingend im Beispiel anzugeben, weil das *LargePhoto*-Feld den SQL Server-Typ „varbinary\(max\)“ aufweist und dieser daher standardmäßig als binärer Stream zurückgegeben wird. Informationen zu PHP-Datentypen finden Sie unter [Default PHP Data Types](../content/Default-PHP-Data-Types.md). Weitere Informationen zum Angeben von PHP-Rückgabetypen finden Sie unter [How to: Specify PHP Data Types](../Topic/How%20to:%20Specify%20PHP%20Data%20Types.md).  
  
## Siehe auch  
[Abrufen von Daten](../content/Retrieving-Data.md)  
[Abrufen von Daten als Stream mit dem SQLSRV-Treiber](../content/Retrieving-Data-as-a-Stream-Using-the-SQLSRV-Driver.md)  
[Informationen zu den Codebeispielen in der Dokumentation](../content/About-Code-Examples-in-the-Documentation.md)  
  
