---
title: "Vorgehensweise: PHP-Datentypen festlegen"
ms.custom: na
ms.date: 06/16/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fee6e6b8-aad9-496b-84a2-18d2950470a4
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
# Vorgehensweise: PHP-Datentypen festlegen
Wenn Sie den PDO\_SQLSRV-Treiber verwenden, können Sie beim Abrufen von Daten von Servern mittels „PDOStatement::bindColumn“ und „PDOStatement::bindParam“ den PHP-Datentyp festlegen. Weitere Informationen finden Sie unter [PDOStatement::bindColumn](../Topic/PDOStatement::bindColumn.md) und [PDOStatement::bindParam](../Topic/PDOStatement::bindParam.md) .  
  
Die folgenden Schritten zeigen zusammenfassend, wie PHP-Datentypen beim Abruf vom Server mit dem SQLSRV-Treiber festgelegt werden:  
  
1.  Richten Sie eine Transact\-SQL-Abfrage mit [sqlsrv_query](../content/sqlsrv_query.md) oder der Kombination aus [sqlsrv_prepare](../content/sqlsrv_prepare.md)\/[sqlsrv_execute](../content/sqlsrv_execute.md) ein, und führen Sie sie aus.  
  
2.  Stellen Sie eine Datenzeile für das Lesen mit [sqlsrv_fetch](../content/sqlsrv_fetch.md)bereit.  
  
3.  Verwenden Sie [sqlsrv_get_field](../content/sqlsrv_get_field.md) , um die Felddaten einer ausgegebenen Zeile mit dem gewünschten, im dritten optionalen Parameter festgelegten PHP-Datentyp abzurufen. Falls der optionale dritte Parameter nicht festgelegt ist, werden die Daten laut den PHP-Standarddatentypen zurückgegeben. Informationen zu den PHP-Standarddatentypen finden Sie unter [Default PHP Data Types](../content/Default-PHP-Data-Types.md).  
  
    Informationen zu den Konstanten, die zur Festlegung der PHP-Datentypen verwendet werden, finden Sie im PHPTYPEs-Abschnitt von [Konstanten &#40;Microsoft-Treiber für PHP für SQL Server&#41;](../content/Constants--Microsoft-Drivers-for-PHP-for-SQL-Server-.md).  
  
## Beispiel  
Im folgenden Beispiel werden Zeilen von der *Production.ProductReview* -Tabelle der AdventureWorks-Datenbank abgerufen. In jeder ausgegebenen Zeile wird das *ReviewDate* -Feld als Zeichenfolge und das *Comments* -Feld als Stream abgerufen. Die Streamdateien werden mit der PHP [fpassthru](http://php.net/manual/en/function.fpassthru.php) -Funktion dargestellt.  
  
Das Beispiel setzt voraus, dass SQL Server und die [AdventureWorks](http://go.microsoft.com/fwlink/?LinkID=67739) -Datenbank auf dem lokalen Computer installiert sind. Wenn das Beispiel über die Befehlszeile ausgeführt wird, werden alle Ausgaben in die Konsole geschrieben.  
  
```  
<?php  
/*Connect to the local server using Windows Authentication and specify  
the AdventureWorks database as the database in use. */  
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
                ReviewDate,  
                Rating,   
                Comments   
         FROM Production.ProductReview   
         WHERE ProductID = ?   
         ORDER BY ReviewDate DESC";  
  
/* Set the parameter value. */  
$productID = 709;  
$params = array( $productID);  
  
/* Execute the query. */  
$stmt = sqlsrv_query($conn, $tsql, $params);  
if( $stmt === false )  
{  
     echo "Error in statement execution.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Retrieve and display the data. The first and third fields are  
retrieved according to their default types, strings. The second field  
is retrieved as a string with 8-bit character encoding. The fourth  
field is retrieved as a stream with 8-bit character encoding.*/  
while ( sqlsrv_fetch( $stmt))  
{  
   echo "Name: ".sqlsrv_get_field( $stmt, 0 )."\n";  
   echo "Date: ".sqlsrv_get_field( $stmt, 1,   
                       SQLSRV_PHPTYPE_STRING( SQLSRV_ENC_CHAR))."\n";  
   echo "Rating: ".sqlsrv_get_field( $stmt, 2 )."\n";  
   echo "Comments: ";  
   $comments = sqlsrv_get_field( $stmt, 3,   
                            SQLSRV_PHPTYPE_STREAM(SQLSRV_ENC_CHAR));  
   fpassthru( $comments);  
   echo "\n";   
}  
  
/* Free statement and connection resources. */  
sqlsrv_free_stmt( $stmt);  
sqlsrv_close( $conn);  
?>  
```  
  
Im Beispiel sorgt der Abruf des zweiten Feldes \(*ReviewDate*\) als Zeichenfolge für die Millisekunden-Genauigkeit des SQL Server-Datentyps DATETIME. Standardmäßig wird der SQL Server-Datentyp DATETIME als PHP-DateTime-Objekt abgerufen, wobei die Millisekunden-Genauigkeit verloren geht.  
  
Das vierte Feld \(*Comments*\) wird zu Vorführungszwecken als Stream abgerufen. Standardmäßig wird der SQL Server-Datentyp „nvarchar\(3850\)“ als eine Zeichenfolge abgerufen. Dies ist für die meisten Situationen akzeptabel.  
  
> [!NOTE]  
> Die [sqlsrv_field_metadata](../content/sqlsrv_field_metadata.md)-Funktion bietet eine Möglichkeit, Feldinformationen inklusive Feldtypinformationen zu erhalten bevor eine Abfrage durchgeführt wird.  
  
## Siehe auch  
[Abrufen von Daten](../content/Retrieving-Data.md)  
[Informationen zu den Codebeispielen in der Dokumentation](../content/About-Code-Examples-in-the-Documentation.md)  
[Vorgehensweise: Abrufen von Eingabe-/Ausgabeparametern mit dem SQLSRV-Treiber](../Topic/How%20to:%20Retrieve%20Output%20Parameters%20Using%20the%20SQLSRV%20Driver.md)  
[How to: Retrieve Input and Output Parameters Using the SQLSRV Driver](../Topic/How%20to:%20Retrieve%20Input%20and%20Output%20Parameters%20Using%20the%20SQLSRV%20Driver.md)  
  
