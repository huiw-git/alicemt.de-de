---
title: "sqlsrv_fetch_array"
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
  - sqlsrv_fetch_array
apitype: NA
ms.assetid: 69270b9e-0791-42f4-856d-412da39dea63
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
# sqlsrv_fetch_array
Gibt die nächste Datenzeile als numerisch indiziertes Array, assoziatives Array oder beides zurück.  
  
## Syntax  
  
```  
  
sqlsrv_fetch_array( resource $stmt[, int $fetchType [, row[, ]offset]])  
```  
  
#### Parameter  
*$stmt*: Eine Anweisungsressource, die einer ausgeführten Anweisung entspricht.  
  
*$fetchType* \[OPTIONAL\]: Eine vordefinierte Konstante. Dieser Parameter kann einen der in der folgenden Tabelle aufgeführten Werte annehmen:  
  
|Wert|Beschreibung|  
|---------|---------------|  
|SQLSRV\_FETCH\_NUMERIC|Die nächste Datenzeile wird als numerisches Array zurückgegeben.|  
|SQLSRV\_FETCH\_ASSOC|Die nächste Datenzeile wird als assoziatives Array zurückgegeben. Die Array-Schlüssel sind die Spaltennamen im Resultset.|  
|SQLSRV\_FETCH\_BOTH|Die nächste Datenzeile wird als numerisches und assoziatives Array zurückgegeben. Dies ist der Standardwert.|  
  
*row* \[OPTIONAL\]: In Version 1.1 hinzugefügt. Einer der folgenden Werte, der spezifiziert, auf welche Zeile in einem Resultset zuzugreifen ist, welches einen bildlauffähigen Cursor verwendet: \(Wenn *row* angegeben wird, muss *fetchtype* explizit angegeben werden, auch wenn Sie den Standardwert angeben.\)  
  
-   SQLSRV\_SCROLL\_NEXT  
-   SQLSRV\_SCROLL\_PRIOR  
-   SQLSRV\_SCROLL\_FIRST  
-   SQLSRV\_SCROLL\_LAST  
-   SQLSRV\_SCROLL\_ABSOLUTE  
-   SQLSRV\_SCROLL\_RELATIVE  
  
Weitere Informationen zu diesen Werten finden Sie unter [Festlegen eines Cursortyps und Zeilenauswahl](../content/Specifying-a-Cursor-Type-and-Selecting-Rows.md). Unterstützung für einen bildlauffähigen Cursor wurde in Version 1.1 der [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt.  
  
*offset* \[OPTIONAL\]: In Verbindung mit SQLSRV\_SCROLL\_ABSOLUTE und SQLSRV\_SCROLL\_RELATIVE verwendet, um die abzurufende Zeile anzugeben. Der erste Datensatz im Resultset ist „0“.  
  
## Rückgabewert  
Wenn eine Datenzeile abgerufen wird, wird ein **Array** zurückgegeben. Wenn keine weiteren Zeilen mehr abgerufen werden können, wird **NULL** zurückgegeben. Wenn ein Fehler auftritt, wird **false** zurückgegeben.  
  
Basierend auf dem Wert des *$fetchType* -Parameters, kann das zurückgegebene **Array** ein numerisch indiziertes **Array**, ein assoziatives **Array**oder beides sein. In der Standardeinstellung wird ein **Array** mit numerischen und assoziativen Schlüsseln zurückgegeben. Der Datentyp eines Werts im zurückgegebenen Array wird der PHP-Standarddatentyp sein. Informationen zu PHP-Datentypen finden Sie unter [Default PHP Data Types](../content/Default-PHP-Data-Types.md).  
  
## Hinweise  
Wenn eine Spalte ohne Namen zurückgegeben wird, ist der assoziative Schlüssel für das Arrayelement eine leere Zeichenfolge \(""\). Betrachten Sie beispielsweise diese Transact\-SQL\-Anweisung, die einen Wert in eine Datenbanktabelle einfügt und den vom Server generierten Primärschlüssel abruft:  
  
```
INSERT INTO Production.ProductPhoto (LargePhoto) VALUES (?);  
SELECT SCOPE_IDENTITY()
```
  
Wenn das Resultset, das vom `SELECT SCOPE_IDENTITY()`-Teil dieser Anweisung zurückgegeben wird, als assoziatives Array abgerufen wird, so wird der Schlüssel des zurückgegebenen Werts eine leere Zeichenfolge \(""\) sein, da die zurückgegebene Spalte keinen Namen hat. Um dies zu vermeiden, können Sie das Ergebnis als numerisches Array abrufen oder Sie können einen Namen für die zurückgegebene Spalte in der Transact\-SQL-Anweisung angeben. Im Folgenden finden Sie eine Möglichkeit, einen Spaltennamen in Transact\-SQL anzugeben:  
  
```
SELECT SCOPE_IDENTITY() AS PictureID
```
  
Wenn ein Resultset mehrere Spalten ohne Namen enthält, wird der Wert der letzten unbenannten Spalte dem Schlüssel einer leeren Zeichenfolge \(""\) zugewiesen.  
  
## Beispiel  
Das folgende Beispiel ruft jede Zeile eines Resultsets als assoziatives **Array**auf. Das Beispiel setzt voraus, dass SQL Server und die [AdventureWorks](http://go.microsoft.com/fwlink/?LinkID=67739) -Datenbank auf dem lokalen Computer installiert sind. Wenn das Beispiel über die Befehlszeile ausgeführt wird, werden alle Ausgaben in die Konsole geschrieben.  
  
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
  
/* Set up and execute the query. */  
$tsql = "SELECT FirstName, LastName  
         FROM Person.Contact  
         WHERE LastName='Alan'";  
$stmt = sqlsrv_query( $conn, $tsql);  
if( $stmt === false)  
{  
     echo "Error in query preparation/execution.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Retrieve each row as an associative array and display the results.*/  
while( $row = sqlsrv_fetch_array( $stmt, SQLSRV_FETCH_ASSOC))  
{  
      echo $row['LastName'].", ".$row['FirstName']."\n";  
}  
  
/* Free statement and connection resources. */  
sqlsrv_free_stmt( $stmt);  
sqlsrv_close( $conn);  
?>  
```  
  
## Beispiel  
Das folgende Beispiel ruft jede Zeile eines Resultsets als numerisch indiziertes Array auf.  
  
Im Beispiel wird die Produktinformation aus der *Purchasing.PurchaseOrderDetail*-Tabelle der AdventureWorks-Datenbank für Produkte mit einem angegebenen Datum und einer gelagerten Menge \(*StockQty*\), die kleiner ist als ein angegebener Wert, abgerufen.  
  
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
  
/* Define the query. */  
$tsql = "SELECT ProductID,  
                UnitPrice,  
                StockedQty   
         FROM Purchasing.PurchaseOrderDetail  
         WHERE StockedQty < 3   
         AND DueDate='2002-01-29'";  
  
/* Execute the query. */  
$stmt = sqlsrv_query( $conn, $tsql);  
if ( $stmt )  
{  
     echo "Statement executed.\n";  
}   
else   
{  
     echo "Error in statement execution.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Iterate through the result set printing a row of data upon each  
iteration.*/  
while( $row = sqlsrv_fetch_array( $stmt, SQLSRV_FETCH_NUMERIC))  
{  
     echo "ProdID: ".$row[0]."\n";  
     echo "UnitPrice: ".$row[1]."\n";  
     echo "StockedQty: ".$row[2]."\n";  
     echo "-----------------\n";  
}  
  
/* Free statement and connection resources. */  
sqlsrv_free_stmt( $stmt);  
sqlsrv_close( $conn);  
?>  
```  
  
Die **sqlsrv\_fetch\_array** Funktion gibt immer die Daten gemäß der [PHP-Standarddatentypen](../content/Default-PHP-Data-Types.md) zurück. Weitere Informationen zur Angabe des PHP-Datentyps finden Sie unter [How to: Specify PHP Data Types](../Topic/How%20to:%20Specify%20PHP%20Data%20Types.md).  
  
Wenn ein Feld ohne Namen abgerufen wird, ist der assoziative Schlüssel für das Arrayelement eine leere Zeichenfolge \(""\). Weitere Informationen finden Sie unter [sqlsrv_fetch_array](../content/sqlsrv_fetch_array.md).  
  
## Siehe auch  
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
[Abrufen von Daten](../content/Retrieving-Data.md)  
[Informationen zu den Codebeispielen in der Dokumentation](../content/About-Code-Examples-in-the-Documentation.md)  
[Programmierhandbuch für den PHP-SQL-Treiber](../content/Programming-Guide-for-PHP-SQL-Driver.md)
  
