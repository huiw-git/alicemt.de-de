---
title: "sqlsrv_query"
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
  - sqlsrv_query
apitype: NA
ms.assetid: 9fa7c4c8-4da8-4299-9893-f61815055aa3
caps.latest.revision: 46
caps.handback.revision: 45
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
# sqlsrv_query
Bereitet eine Anweisung vor und führt diese aus.  
  
## Syntax  
  
```  
  
sqlsrv_query( resource $conn, string $tsql [, array $params [, array $options]])  
```  
  
#### Parameter  
*$conn*: Die mit der vorbereiteten Anweisung verknüpfte Verbindungsressource.  
  
*$tsql*: Der Transact\-SQL-Ausdruck, der der vorbereiteten Anweisung entspricht.  
  
*$params* \[OPTIONAL\]: Ein **Array** von Werten, die Parametern in einer parametrisierten Abfrage entsprechen. Jedes Element des Arrays kann eines der folgenden sein:  
  
-   Ein Literalwert  
  
-   Eine PHP-Variable.  
  
-   Ein **Array** mit der folgenden Struktur:  
  
    ```  
    array($value [, $direction [, $phpType [, $sqlType]]])  
    ```  
  
    Die Beschreibung für jedes Element des Arrays finden Sie in der folgenden Tabelle:  
  
    |Element|Beschreibung|  
    |-----------|---------------|  
    |*$value*|Ein Literalwert, eine PHP-Variable oder eine PHP\-Variable als Verweis.|  
    |*$direction*\[OPTIONAL\]|Eine der folgenden verwendeten **SQLSRV\_PARAM\_\***-Konstanten, um die Parameterrichtung anzugeben: **SQLSRV\_PARAM\_IN**, **SQLSRV\_PARAM\_OUT**, **SQLSRV\_PARAM\_INOUT**. Der Standardwert ist **SQLSRV\_PARAM\_IN**.<br /><br />Weitere Informationen zu PHP-Konstanten finden Sie unter [Konstanten &#40;Microsoft-Treiber für PHP für SQL Server&#41;](../content/Constants--Microsoft-Drivers-for-PHP-for-SQL-Server-.md).|  
    |*$phpType*\[OPTIONAL\]|Eine **SQLSRV\_PHPTYPE\_\***-Konstante, die den PHP-Datentyp des zurückgegebenen Werts angibt.<br /><br />Weitere Informationen zu PHP-Konstanten finden Sie unter [Konstanten &#40;Microsoft-Treiber für PHP für SQL Server&#41;](../content/Constants--Microsoft-Drivers-for-PHP-for-SQL-Server-.md).|  
    |*$sqlType*\[OPTIONAL\]|Eine **SQLSRV\_SQLTYPE\_\***-Konstante, die den SQL Server-Datentyp des Eingabewerts angibt.<br /><br />Weitere Informationen zu PHP-Konstanten finden Sie unter [Konstanten &#40;Microsoft-Treiber für PHP für SQL Server&#41;](../content/Constants--Microsoft-Drivers-for-PHP-for-SQL-Server-.md).|  
  
*$options* \[OPTIONAL\]: Ein assoziatives Array, das Abfrageeigenschaften festlegt. Die folgenden Schlüssel werden unterstützt:  
  
|Key|Unterstützte Werte|Beschreibung|  
|-------|--------------------|---------------|  
|QueryTimeout|Ein positiver ganzzahliger Wert|Legt das Abfragetimeout in Sekunden fest. Standardmäßig wartet der Treiber unbegrenzt auf Ergebnisse.|  
|SendStreamParamsAtExec|**WAHR** oder **FALSCH**<br /><br />Der Standardwert ist **true**.|Konfiguriert den Treiber, um alle Streamdaten bei der Ausführung zu senden \(**true**\) oder Streamdaten in Blöcken \(**false**\) zu senden. In der Standardeinstellung ist dieser Wert mit **true**festgelegt. Weitere Informationen finden Sie unter [sqlsrv_send_stream_data](../content/sqlsrv_send_stream_data.md).|  
|Bildlauffähigkeit|SQLSRV\_CURSOR\_FORWARD<br /><br />SQLSRV\_CURSOR\_STATIC<br /><br />SQLSRV\_CURSOR\_DYNAMIC<br /><br />SQLSRV\_CURSOR\_KEYSET<br /><br />SQLSRV\_CURSOR\_CLIENT\_BUFFERED|Weitere Informationen zu diesen Werten finden Sie unter [Festlegen eines Cursortyps und Zeilenauswahl](../content/Specifying-a-Cursor-Type-and-Selecting-Rows.md).|  
  
## Rückgabewert  
Eine Anweisungsressource. Wenn die Anweisung nicht erstellt und\/oder ausgeführt werden kann, wird **false** zurückgegeben.  
  
## Hinweise  
Die **sqlsrv\_query**Funktion eignet sich ideal für einmalige Abfragen und sollte auch die Standardauswahl sein, um Abfragen auszuführen, es sei denn, es gelten besondere Umstände. Diese Funktion bietet eine optimierte Methode zum Ausführen einer Abfrage mit einem Minimum von Codes. Die **sqlsrv\_query**-Funktion führt jeweils eine Anweisungsvorbereitung und eine Anweisungsausführung durch und kann verwendet werden, um parametrisierte Abfragen auszuführen.  
  
Weitere Informationen finden Sie unter [How to: Retrieve Output Parameters Using the SQLSRV Driver](../Topic/How%20to:%20Retrieve%20Output%20Parameters%20Using%20the%20SQLSRV%20Driver.md).  
  
## Beispiel  
Im folgenden Beispiel wird eine einzelne Zeile in die *Sales.SalesOrderDetail* -Tabelle der AdventureWorks-Datenbank eingefügt. Das Beispiel setzt voraus, dass SQL Server und die [AdventureWorks](http://go.microsoft.com/fwlink/?LinkID=67739) -Datenbank auf dem lokalen Computer installiert sind. Wenn das Beispiel über die Befehlszeile ausgeführt wird, werden alle Ausgaben in die Konsole geschrieben.  
  
> [!NOTE]  
> Obwohl folgendes Beispiel eine INSERT-Anweisung verwendet, um die Verwendung des **sqlsrv\_query** für einmaliges Ausführen einer Anweisung zu demonstrieren, gilt das Konzept für jede Transact\-SQL\-Anweisung.  
  
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
  
/* Set up the parameterized query. */  
$tsql = "INSERT INTO Sales.SalesOrderDetail   
        (SalesOrderID,   
         OrderQty,   
         ProductID,   
         SpecialOfferID,   
         UnitPrice,   
         UnitPriceDiscount)  
        VALUES   
        (?, ?, ?, ?, ?, ?)";  
  
/* Set parameter values. */  
$params = array(75123, 5, 741, 1, 818.70, 0.00);  
  
/* Prepare and execute the query. */  
$stmt = sqlsrv_query( $conn, $tsql, $params);  
if( $stmt )  
{  
     echo "Row successfully inserted.\n";  
}  
else  
{  
     echo "Row insertion failed.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Free statement and connection resources. */  
sqlsrv_free_stmt( $stmt);  
sqlsrv_close( $conn);  
?>  
```  
  
## Beispiel  
Im folgenden Beispiel wird ein Feld in der *Sales.SalesOrderDetail* -Tabelle der AdventureWorks-Datenbank aktualisiert. Das Beispiel setzt voraus, dass SQL Server und die [AdventureWorks](http://go.microsoft.com/fwlink/?LinkID=67739) -Datenbank auf dem lokalen Computer installiert sind. Wenn das Beispiel über die Befehlszeile ausgeführt wird, werden alle Ausgaben in die Konsole geschrieben.  
  
```  
<?php  
/* Connect to the local server using Windows Authentication and  
specify the AdventureWorks database as the database in use. */  
$serverName = "(local)";  
$connectionInfo = array("Database"=>"AdventureWorks");  
$conn = sqlsrv_connect( $serverName, $connectionInfo);  
if( $conn === false )  
{  
     echo "Could not connect.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Set up the parameterized query. */  
$tsql = "UPDATE Sales.SalesOrderDetail   
         SET OrderQty = ( ?)   
         WHERE SalesOrderDetailID = ( ?)";  
  
/* Assign literal parameter values. */  
$params = array( 5, 10);  
  
/* Execute the query. */  
if( sqlsrv_query( $conn, $tsql, $params))  
{  
      echo "Statement executed.\n";  
}   
else  
{  
      echo "Error in statement execution.\n";  
      die( print_r( sqlsrv_errors(), true));  
}  
  
/* Free connection resources. */  
sqlsrv_close( $conn);  
?>  
```  
  
## Siehe auch  
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
[Vorgehensweise: Ausführen von parametrisierten Abfragen](../Topic/How%20to:%20Perform%20Parameterized%20Queries.md)  
[Informationen zu den Codebeispielen in der Dokumentation](../content/About-Code-Examples-in-the-Documentation.md)  
[Vorgehensweise: Streamen von Daten](../Topic/How%20to:%20Send%20Data%20as%20a%20Stream.md)  
[Verwenden direktionaler Parameter](../content/Using-Directional-Parameters.md)  
  
