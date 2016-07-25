---
title: "Vorgehensweise: Senden und Abrufen von UTF-8-Daten mithilfe der eingebauten UTF-8-Unterst&#252;tzung."
ms.custom: na
ms.date: 06/28/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 366c57cf-352f-4202-8074-6ddce44880d1
caps.latest.revision: 33
caps.handback.revision: 32
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
# Vorgehensweise: Senden und Abrufen von UTF-8-Daten mithilfe der eingebauten UTF-8-Unterst&#252;tzung.
Wenn Sie den PDO\_SQLSRV-Treiber verwenden, können Sie die Codierung mit dem Attribut PDO::SQLSRV\_ATTR\_ENCODING festlegen. Weitere Informationen finden Sie unter [Konstanten &#40;Microsoft-Treiber für PHP für SQL Server&#41;](../content/Constants--Microsoft-Drivers-for-PHP-for-SQL-Server-.md).  
  
Im weiteren Verlauf dieses Themas wird die Codierung mit dem SQLSRV-Treiber erläutert.  
  
Gehen Sie zum Senden/Abrufen von UTF\-8-codierten Daten an den/vom Server wie folgt vor:  
  
1.  Stellen Sie sicher, dass die Quell- oder Ziel-Spalte den Typ **nchar** oder **nvarchar**aufweist.  
  
2.  Geben Sie im Parameterarray `SQLSRV_PHPTYPE_STRING('UTF-8')` als PHP-Typ an. Oder legen Sie `"CharacterSet" => "UTF-8"` als eine Verbindungsoption fest.  
  
    Wenn Sie einen Zeichensatz als Teil der Verbindungsoptionen angeben, geht der Treiber davon aus, dass auch die anderen Optionszeichenfolgen der Verbindung den gleichen Zeichensatz verwenden. Auch beim Servernamen und den Abfragezeichenfolgen geht er vom selben Zeichensatz aus.  
  
Beachten Sie, dass Sie UTF\-8 oder SQLSRV\_ENC\_CHAR an **CharacterSet** übergeben können \(aber nicht SQLSRV\_ENC\_BINARY\). Die Standardcodierung ist SQLSRV\_ENC\_CHAR.  
  
## Beispiel  
Im folgenden Beispiel wird veranschaulicht, wie Sie bei der Herstellung der Verbindung, durch die Festlegung auf den UTF\-8-Zeichensatz, das Senden und Empfangen von UTF\-8-codierten Daten ermöglichen. Das Beispiel aktualisiert die Spalte „Kommentare“ der Tabelle „Produktion.ProduktReview“ auf eine angegebene Review-ID. Das Beispiel ruft auch die neuen, aktualisierten Daten auf und zeigt sie an. Beachten Sie, dass die Spalte „Comments“ den Typ **nvarchar\(3850\)** aufweist. Beachten Sie, dass Daten vor dem Senden an den Server mit der PHP-Funktion **utf8\_encode** in UTF\-8-Codierung konvertiert werden. Dies erfolgt nur zu Demonstrationszwecken. In einem realen Anwendungsszenario würden Sie mit UTF\-8-codierten Daten beginnen.  
  
Das Beispiel setzt voraus, dass [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] und die [AdventureWorks](http://go.microsoft.com/fwlink/?LinkID=67739) -Datenbank auf dem lokalen Computer installiert sind. Wenn das Beispiel über den Browser ausgeführt wird, werden alle Ausgaben im Browser geschrieben.  
  
```  
<?php  
  
// Connect to the local server using Windows Authentication and  
// specify the AdventureWorks database as the database in use.   
//   
$serverName = "MyServer";  
$connectionInfo = array( "Database"=>"AdventureWorks", "CharacterSet" => "UTF-8");  
$conn = sqlsrv_connect( $serverName, $connectionInfo);  
  
if ( $conn === false ) {  
   echo "Could not connect.<br>";  
   die( print_r( sqlsrv_errors(), true));  
}  
  
// Set up the Transact-SQL query.  
//   
$tsql1 = "UPDATE Production.ProductReview  
          SET Comments = ?  
          WHERE ProductReviewID = ?";  
  
// Set the parameter values and put them in an array. Note that  
// $comments is converted to UTF-8 encoding with the PHP function  
// utf8_encode to simulate an application that uses UTF-8 encoded data.   
//   
$reviewID = 3;  
$comments = utf8_encode("testing 1, 2, 3, 4.  Testing.");  
$params1 = array(  
                  array( $comments, null ),  
                  array( $reviewID, null )  
                );  
  
// Execute the query.  
//   
$stmt1 = sqlsrv_query($conn, $tsql1, $params1);  
  
if ( $stmt1 === false ) {  
   echo "Error in statement execution.<br>";  
   die( print_r( sqlsrv_errors(), true));  
}  
else {  
   echo "The update was successfully executed.<br>";  
}  
  
// Retrieve the newly updated data.  
//   
$tsql2 = "SELECT Comments   
          FROM Production.ProductReview   
          WHERE ProductReviewID = ?";  
  
// Set up the parameter array.  
//   
$params2 = array($reviewID);  
  
// Execute the query.  
//   
$stmt2 = sqlsrv_query($conn, $tsql2, $params2);  
if ( $stmt2 === false ) {  
   echo "Error in statement execution.<br>";  
   die( print_r( sqlsrv_errors(), true));  
}  
  
// Retrieve and display the data.   
//   
if ( sqlsrv_fetch($stmt2) ) {  
   echo "Comments: ";  
   $data = sqlsrv_get_field( $stmt2, 0 );  
   echo $data."<br>";  
}  
else {  
   echo "Error in fetching data.<br>";  
   die( print_r( sqlsrv_errors(), true));  
}  
  
// Free statement and connection resources.  
//   
sqlsrv_free_stmt( $stmt1 );  
sqlsrv_free_stmt( $stmt2 );  
sqlsrv_close( $conn);  
?>  
```  
  
Informationen zum Speichern von Unicode-Daten finden Sie unter [Arbeiten mit Unicode-Daten](http://go.microsoft.com/fwlink/?LinkId=128236).  
  
## Beispiel  
Das folgende Beispiel ähnelt dem ersten Beispiel, aber statt der Festlegung des UTF\-8-Zeichensatzes für die Verbindung, veranschaulicht dieses Beispiel die Festlegung des UTF\-8-Zeichensatzes für die Spalte.  
  
```  
<?php  
  
// Connect to the local server using Windows Authentication and  
// specify the AdventureWorks database as the database in use.   
//   
$serverName = "MyServer";  
$connectionInfo = array( "Database"=>"AdventureWorks");  
$conn = sqlsrv_connect( $serverName, $connectionInfo);  
  
if ( $conn === false ) {  
   echo "Could not connect.<br>";  
   die( print_r( sqlsrv_errors(), true));  
}  
  
// Set up the Transact-SQL query.  
//   
$tsql1 = "UPDATE Production.ProductReview  
          SET Comments = ?  
          WHERE ProductReviewID = ?";  
  
// Set the parameter values and put them in an array. Note that  
// $comments is converted to UTF-8 encoding with the PHP function  
// utf8_encode to simulate an application that uses UTF-8 encoded data.   
//   
$reviewID = 3;  
$comments = utf8_encode("testing");  
$params1 = array(  
                  array($comments,  
                        SQLSRV_PARAM_IN,  
                        SQLSRV_PHPTYPE_STRING('UTF-8')  
                  ),  
                  array($reviewID)  
                );  
  
// Execute the query.  
//   
$stmt1 = sqlsrv_query($conn, $tsql1, $params1);  
  
if ( $stmt1 === false ) {  
   echo "Error in statement execution.<br>";  
   die( print_r( sqlsrv_errors(), true));  
}  
else {  
   echo "The update was successfully executed.<br>";  
}  
  
// Retrieve the newly updated data.  
//   
$tsql2 = "SELECT Comments   
          FROM Production.ProductReview   
          WHERE ProductReviewID = ?";  
  
// Set up the parameter array.  
//   
$params2 = array($reviewID);  
  
// Execute the query.  
//   
$stmt2 = sqlsrv_query($conn, $tsql2, $params2);  
if ( $stmt2 === false ) {  
   echo "Error in statement execution.<br>";  
   die( print_r( sqlsrv_errors(), true));  
}  
  
// Retrieve and display the data.   
//   
if ( sqlsrv_fetch($stmt2) ) {  
   echo "Comments: ";  
   $data = sqlsrv_get_field($stmt2,   
                            0,   
                            SQLSRV_PHPTYPE_STRING('UTF-8')  
                           );  
   echo $data."<br>";  
}  
else {  
   echo "Error in fetching data.<br>";  
   die( print_r( sqlsrv_errors(), true));  
}  
  
// Free statement and connection resources.  
//   
sqlsrv_free_stmt( $stmt1 );  
sqlsrv_free_stmt( $stmt2 );  
sqlsrv_close( $conn);  
?>  
```  
  
## Siehe auch  
[Abrufen von Daten](../content/Retrieving-Data.md)  
[Aktualisieren von Daten &#40;Microsoft-Treiber für PHP für SQL Server&#41;](../content/Updating-Data--Microsoft-Drivers-for-PHP-for-SQL-Server-.md)  
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
[Konstanten &#40;Microsoft-Treiber für PHP für SQL Server&#41;](../content/Constants--Microsoft-Drivers-for-PHP-for-SQL-Server-.md)  
[Beispielanwendung &#40;SQLSRV-Treiber&#41;](../content/Example-Application--SQLSRV-Driver-.md)  
  
