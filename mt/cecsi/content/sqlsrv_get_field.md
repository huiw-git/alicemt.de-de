---
title: "sqlsrv_get_field"
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
  - sqlsrv_get_field
apitype: NA
ms.assetid: fa17cc56-fb38-433b-a40d-65642f04dc23
caps.latest.revision: 28
caps.handback.revision: 27
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
# sqlsrv_get_field
Ruft Daten vom angegebenen Feld der aktuellen Zeile ab. Auf die Felddaten muss gemäß der Reihenfolge zugegriffen werden. So kann beispielsweise nicht auf Daten aus dem ersten Feld zugegriffen werden nachdem auf Daten vom zweiten Feld zugegriffen wurde.  
  
## Syntax  
  
```  
  
sqlsrv_get_field( resource $stmt, int $fieldIndex [, int $getAsType])  
```  
  
#### Parameter  
*$stmt*: Eine Anweisungsressource, die einer ausgeführten Anweisung entspricht.  
  
*$fieldIndex*: Der Index des abzurufenden Felds. Indizes beginnen mit 0.  
  
*$getAsType* \[OPTIONAL\]: Eine **SQLSRV**-Konstante \(**SQLSRV\_PHPTYPE\_\***\), die den PHP-Datentyp für die zurückgegebenen Daten bestimmt. Informationen zu den unterstützten Datentypen finden Sie unter [Konstanten &#40;Microsoft-Treiber für PHP für SQL Server&#41;](../content/Constants--Microsoft-Drivers-for-PHP-for-SQL-Server-.md). Wenn kein Rückgabetyp spezifiziert ist, wird ein PHP-Typ zurückgegeben. Informationen zu PHP-Standardtypen finden Sie unter [Default PHP Data Types](../content/Default-PHP-Data-Types.md). Informationen zum Spezifizieren von PHP-Datentypen finden Sie unter [How to: Specify PHP Data Types](../Topic/How%20to:%20Specify%20PHP%20Data%20Types.md).  
  
## Rückgabewert  
Die Felddaten. Sie können den PHP-Datentyp der zurückgegebenen Daten festlegen, indem Sie den *$getAsType* -Parameter verwenden. Falls kein Rückgabedatentyp festgelegt ist, wird der PHP-Standarddatentyp zurückgegeben. Informationen zu PHP-Standardtypen finden Sie unter [Default PHP Data Types](../content/Default-PHP-Data-Types.md). Informationen zum Spezifizieren von PHP-Datentypen finden Sie unter [How to: Specify PHP Data Types](../Topic/How%20to:%20Specify%20PHP%20Data%20Types.md).  
  
## Hinweise  
Die Kombination von **sqlsrv\_fetch** und **sqlsrv\_get\_field** bewirkt, dass auf Daten nur vorangehend zugegriffen werden kann.  
  
Die Kombination aus **sqlsrv\_fetch**\/**sqlsrv\_get\_field** lädt nur ein Feld einer Zeile eines Resultsets in den Skriptspeicher und erlaubt die Festlegung von PHP-Rückgabetypen. \(Weitere Informationen zur Angabe des PHP-Rückgabetyps finden Sie unter [How to: Specify PHP Data Types](../Topic/How%20to:%20Specify%20PHP%20Data%20Types.md) (Gewusst wie: Festlegen von PHP-Datentypen).\) Diese Kombination von Funktionen macht es möglich Daten als Stream abzurufen. \(Informationen zum Abrufen von Daten als Stream finden Sie unter [Retrieving Data as a Stream Using the SQLSRV Driver](../content/Retrieving-Data-as-a-Stream-Using-the-SQLSRV-Driver.md) (Abrufen von Daten als Stream mithilfe des SQLSRV-Treibers).\)  
  
## Beispiel  
Das folgende Beispiel ruft eine Datenzeile ab, die eine Produktprüfung enthält, sowie den Namen des Prüfers. Zum Abrufen von Daten aus dem Resultset wird **sqlsrv\_get\_field** verwendet. Das Beispiel setzt voraus, dass SQL Server und die [AdventureWorks](http://go.microsoft.com/fwlink/?LinkID=67739) -Datenbank auf dem lokalen Computer installiert sind. Wenn das Beispiel über die Befehlszeile ausgeführt wird, werden alle Ausgaben in die Konsole geschrieben.  
  
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
Comments are of the SQL Server nvarchar type. */  
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
if( sqlsrv_fetch( $stmt ) === false )  
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
while( !feof( $stream))  
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
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
[Abrufen von Daten](../content/Retrieving-Data.md)  
[Informationen zu den Codebeispielen in der Dokumentation](../content/About-Code-Examples-in-the-Documentation.md)  
  
