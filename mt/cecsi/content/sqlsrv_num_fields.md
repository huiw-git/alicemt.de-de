---
title: "sqlsrv_num_fields"
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
  - sqlsrv_num_fields
apitype: NA
ms.assetid: 03ca1860-01ed-408c-862a-57a7355de4bf
caps.latest.revision: 17
caps.handback.revision: 16
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
# sqlsrv_num_fields
Ruft die Anzahl der Felder in einem aktiven Resultset ab. Beachten Sie, dass **sqlsrv\_num\_fields** für jede vorbereitete Anweisung vor oder nach der Ausführung aufgerufen werden kann.  
  
## Syntax  
  
```  
  
sqlsrv_num_fields( resource $stmt)  
```  
  
#### Parameter  
*$stmt*: Die Anweisung, zu der das Zielresultset aktiv ist.  
  
## Rückgabewert  
Ein ganzzahliger Wert, der die Anzahl der Felder im aktiven Resultset darstellt. Falls ein Fehler auftritt, wird der boolesche Wert **false** zurückgegeben.  
  
## Beispiel  
Das folgende Beispiel führt eine Abfrage zum Abrufen aller Felder für die ersten drei Zeilen in der *HumanResources.Department* -Tabelle der Adventureworks-Datenbank durch. Die Funktion **sqlsrv\_num\_fields** bestimmt die Anzahl der Felder im Resultset. Dies erlaubt die Darstellung der Daten indem in einem Iterationsverfahren durch jede ausgegebenen Zeile durchgegangen wird.  
  
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
  
/* Define and execute the query. */  
$tsql = "SELECT TOP (3) * FROM HumanResources.Department";  
$stmt = sqlsrv_query($conn, $tsql);  
if( $stmt === false)  
{  
     echo "Error in executing query.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Retrieve the number of fields. */  
$numFields = sqlsrv_num_fields( $stmt );  
  
/* Iterate through each row of the result set. */  
while( sqlsrv_fetch( $stmt ))  
{  
     /* Iterate through the fields of each row. */  
     for($i = 0; $i < $numFields; $i++)  
     {  
          echo sqlsrv_get_field($stmt, $i,   
                   SQLSRV_PHPTYPE_STRING(SQLSRV_ENC_CHAR))." ";  
     }  
     echo "\n";  
}  
  
/* Free statement and connection resources. */  
sqlsrv_free_stmt( $stmt );  
sqlsrv_close( $conn );  
?>  
```  
  
## Siehe auch  
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
[sqlsrv_field_metadata](../content/sqlsrv_field_metadata.md)  
[Informationen zu den Codebeispielen in der Dokumentation](../content/About-Code-Examples-in-the-Documentation.md)  
  
