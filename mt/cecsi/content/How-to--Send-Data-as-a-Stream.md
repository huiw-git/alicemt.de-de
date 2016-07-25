---
title: "Vorgehensweise: Streamen von Daten"
ms.custom: na
ms.date: 06/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ab6b95d6-b6e6-4bd7-a18c-50f2918f7532
caps.latest.revision: 30
caps.handback.revision: 29
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
# Vorgehensweise: Streamen von Daten
Die [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] nutzt PHP-Datenströme, um große Objekte an den Server zu senden. In diesem Thema wird erklärt, wie Sie Daten in Strömen senden können. Im ersten Beispiel wird mithilfe des SQLSRV-Treibers die Standardvorgehensweise veranschaulicht, bei der alle Datenstromdaten direkt bei der Abfrageausführung gesendet werden. Im zweiten Beispiel wird mithilfe des SQLSRV-Treibers veranschaulicht, wie Sie bis zu 8 Kilobyte \(KB\) an Datenstromdaten gleichzeitig an den Server senden.  
  
Im dritten Beispiel wird veranschaulicht, wie Sie mithilfe des PDO\_SQLSRV-Treibers Datenstromdaten an den Server senden.  
  
## Beispiel  
Im folgenden Beispiel wird eine einzelne Zeile in die *Production.ProductReview* Tabelle der AdventureWorks-Datenbank eingefügt. Die Kundenkommentare \(*$comments*\) werden mithilfe der PHP-Funktion [fopen](http://php.net/manual/en/function.fopen.php) als Datenstrom geöffnet und bei der Ausführung der Abfrage dann an den Server gestreamt.  
  
Das Beispiel setzt voraus, dass SQL Server und die [AdventureWorks](http://go.microsoft.com/fwlink/?LinkID=67739) -Datenbank auf dem lokalen Computer installiert sind. Die Ausgabe wird in die Konsole geschrieben.  
  
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
$tsql = "INSERT INTO Production.ProductReview (ProductID,   
                                               ReviewerName,  
                                               ReviewDate,  
                                               EmailAddress,  
                                               Rating,  
                                               Comments)  
         VALUES (?, ?, ?, ?, ?, ?)";  
  
/* Set the parameter values and put them in an array.  
Note that $comments is opened as a stream. */  
$productID = '709';  
$name = 'Customer Name';  
$date = date("Y-m-d");  
$email = 'customer@name.com';  
$rating = 3;  
$comments = fopen( "data://text/plain,[ Insert lengthy comment here.]",  
                  "r");  
$params = array($productID, $name, $date, $email, $rating, $comments);  
  
/* Execute the query. All stream data is sent upon execution.*/  
$stmt = sqlsrv_query($conn, $tsql, $params);  
if( $stmt === false )  
{  
     echo "Error in statement execution.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
else  
{  
     echo "The query was successfully executed.";  
}  
  
/* Free statement and connection resources. */  
sqlsrv_free_stmt( $stmt);  
sqlsrv_close( $conn);  
?>  
```  
  
## Beispiel  
Das nächste Beispiel ähnelt dem vorherigen Beispiel, jedoch wurde hier die Standardvorgehensweise zum Senden von Datenstromdaten bei Ausführung der Abfrage deaktiviert. Im Beispiel wird [sqlsrv_send_stream_data](../content/sqlsrv_send_stream_data.md) verwendet, um Datenstromdaten an den Server zu senden. Mit jedem Aufruf werden bis zu acht Kilobyte \(8 KB\) Daten an **sqlsrv\_send\_stream\_data** gesendet. Das Skript zählt die Anzahl der Aufrufe durch **sqlsrv\_send\_stream\_data** und zeigt sie in der Konsole an.  
  
Das Beispiel setzt voraus, dass SQL Server und die [AdventureWorks](http://go.microsoft.com/fwlink/?LinkID=67739) -Datenbank auf dem lokalen Computer installiert sind. Die Ausgabe wird in die Konsole geschrieben.  
  
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
$tsql = "INSERT INTO Production.ProductReview (ProductID,   
                                               ReviewerName,  
                                               ReviewDate,  
                                               EmailAddress,  
                                               Rating,  
                                               Comments)  
         VALUES (?, ?, ?, ?, ?, ?)";  
  
/* Set the parameter values and put them in an array.  
Note that $comments is opened as a stream. */  
$productID = '709';  
$name = 'Customer Name';  
$date = date("Y-m-d");  
$email = 'customer@name.com';  
$rating = 3;  
$comments = fopen( "data://text/plain,[ Insert lengthy comment here.]",  
                  "r");  
$params = array($productID, $name, $date, $email, $rating, $comments);  
  
/* Turn off the default behavior of sending all stream data at  
execution. */  
$options = array("SendStreamParamsAtExec" => 0);  
  
/* Execute the query. */  
$stmt = sqlsrv_query($conn, $tsql, $params, $options);  
if( $stmt === false )  
{  
     echo "Error in statement execution.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Send up to 8K of parameter data to the server with each call to  
sqlsrv_send_stream_data. Count the calls. */  
$i = 1;  
while( sqlsrv_send_stream_data( $stmt))   
{  
     echo "$i call(s) made.\n";  
     $i++;  
}  
  
/* Free statement and connection resources. */  
sqlsrv_free_stmt( $stmt);  
sqlsrv_close( $conn);  
?>  
```  
  
Obwohl in den Beispielen in diesem Thema nur Zeichendaten an den Server gesendet werden, können Daten aller Formate als Strom gesendet werden. Sie können die in diesem Thema erläuterten Techniken beispielsweise nutzen, um Bilder im Binärformat als Ströme zu senden.  
  
## Beispiel  
  
```  
<?php  
   $server = "(local)";   
   $database = "Test";  
   $conn = new PDO( "sqlsrv:server=$server;Database = $database", "", "");  
  
   $binary_source = fopen( "data://text/plain,", "r");  
  
   $stmt = $conn->prepare("insert into binaries (imagedata) values (?)");  
   $stmt->bindParam(1, $binary_source, PDO::PARAM_LOB);   
  
   $conn->beginTransaction();  
   $stmt->execute();  
   $conn->commit();  
?>  
```  
  
## Siehe auch  
[Aktualisieren von Daten &#40;Microsoft-Treiber für PHP für SQL Server&#41;](../content/Updating-Data--Microsoft-Drivers-for-PHP-for-SQL-Server-.md)  
[Abrufen von Daten als Stream mit dem SQLSRV-Treiber](../content/Retrieving-Data-as-a-Stream-Using-the-SQLSRV-Driver.md)  
[Informationen zu den Codebeispielen in der Dokumentation](../content/About-Code-Examples-in-the-Documentation.md)  
  
