---
title: "Vorgehensweise: Datums- und Uhrzeittypen mittels des SQLSRV-Treibers als Zeichenfolgen abrufen "
ms.custom: na
ms.date: 06/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 58a974ea-4daf-4e3b-98ed-9731b9c9250f
caps.latest.revision: 20
caps.handback.revision: 19
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
# Vorgehensweise: Datums- und Uhrzeittypen mittels des SQLSRV-Treibers als Zeichenfolgen abrufen 
Diese Funktion wurde der Version 1.1 der [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] hinzugefügt und ist nur zulässig, wenn der SQLSRV-Treiber für die [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]verwendet wird. Es ist ein Fehler die Verbindungsoption „ReturnDatesAsStrings“ mit dem PDO\_SQLSRV-Treiber zu verwenden.  
  
Sie können Datums- und Uhrzeittypen \(**datetime**, **date**, **time**, **datetime2** und **datetimeoffset**\) als Zeichenfolgen abrufen, indem Sie eine Option in der Verbindungszeichenfolge festlegen.  
  
### Datums- und Uhrzeittypen als Zeichenfolgen abrufen  
  
-   Verwenden Sie die folgende Verbindungsoption:  
  
    ```  
    'ReturnDatesAsStrings'=>true  
    ```  
  
    Der Standardwert ist **false**, d. h. dass **datetime**, **Date**, **Time**, **DateTime2**und **DateTimeOffset** -Typen als PHP- **Datetime** -Typen ausgegeben werden.  
  
## Beispiel  
Das folgende Beispiel zeigt die Syntax, welche festlegt, dass die Datums- und Uhrzeittypen als Zeichenfolgen abgerufen werden.  
  
```  
<?php  
$serverName = "MyServer";  
$connectionInfo = array( "Database"=>"AdventureWorks", 'ReturnDatesAsStrings '=> true);  
$conn = sqlsrv_connect( $serverName, $connectionInfo);  
if( $conn === false )  
{  
   echo "Could not connect.\n";  
   die( print_r( sqlsrv_errors(), true));  
}  
  
sqlsrv_close( $conn);  
?>  
```  
  
## Beispiel  
Das folgende Beispiel zeigt, dass Sie verschiedene Datumsangaben als Zeichenfolge abrufen können, sofern Sie beim Abruf UTF\-8 angeben. Dies gilt auch, wenn die Verbindung mittels `"ReturnDatesAsStrings" => false` erstellt wurde.  
  
```  
<?php  
$serverName = "MyServer";  
$connectionInfo = array( "Database"=>"AdventureWorks", "ReturnDatesAsStrings" => false);  
$conn = sqlsrv_connect( $serverName, $connectionInfo);  
if( $conn === false ) {  
   echo "Could not connect.\n";  
   die( print_r( sqlsrv_errors(), true));  
}  
  
$tsql = "SELECT VersionDate FROM AWBuildVersion";  
  
$stmt = sqlsrv_query( $conn, $tsql);  
  
if ( $stmt === false ) {  
   echo "Error in statement preparation/execution.\n";  
   die( print_r( sqlsrv_errors(), true));  
}  
  
sqlsrv_fetch( $stmt );  
  
// retrieve date as string  
$date = sqlsrv_get_field( $stmt, 0, SQLSRV_PHPTYPE_STRING("UTF-8"));  
  
if( $date === false ) {  
   die( print_r( sqlsrv_errors(), true ));  
}  
  
echo $date;  
  
sqlsrv_close( $conn);  
?>  
```  
  
## Beispiel  
Das folgende Beispiel zeigt, wie Datumsangaben als Zeichenfolgen abgerufen werden können, indem UTF\-8 und `"ReturnDatesAsStrings" => true` in der Verbindungszeichenfolge spezifiziert werden.  
  
```  
<?php  
$serverName = "MyServer";  
$connectionInfo = array( "Database"=>"AdventureWorks", 'ReturnDatesAsStrings'=> true, "CharacterSet" => 'utf-8' );  
$conn = sqlsrv_connect( $serverName, $connectionInfo);  
if( $conn === false ) {  
   echo "Could not connect.\n";  
   die( print_r( sqlsrv_errors(), true));  
}  
  
$tsql = "SELECT VersionDate FROM AWBuildVersion";  
  
$stmt = sqlsrv_query( $conn, $tsql);  
  
if ( $stmt === false ) {  
   echo "Error in statement preparation/execution.\n";  
   die( print_r( sqlsrv_errors(), true));  
}  
  
sqlsrv_fetch( $stmt );  
  
// retrieve date as string  
$date = sqlsrv_get_field( $stmt, 0 );  
  
if ( $date === false ) {  
   die( print_r( sqlsrv_errors(), true ));  
}  
  
echo $date;  
sqlsrv_close( $conn);  
?>  
```  
  
## Beispiel  
Das folgende Beispiel zeigt, wie das Datum als PHP-Typ abgerufen wird. `'ReturnDatesAsStrings'=> false` ist standardmäßig aktiviert.  
  
```  
<?php  
$serverName = "MyServer";  
$connectionInfo = array( "Database"=>"AdventureWorks");  
$conn = sqlsrv_connect( $serverName, $connectionInfo);  
if( $conn === false ) {  
   echo "Could not connect.\n";  
   die( print_r( sqlsrv_errors(), true));  
}  
  
$tsql = "SELECT VersionDate FROM AWBuildVersion";  
  
$stmt = sqlsrv_query( $conn, $tsql);  
  
if ( $stmt === false ) {  
   echo "Error in statement preparation/execution.\n";  
   die( print_r( sqlsrv_errors(), true));  
}  
  
sqlsrv_fetch( $stmt );  
  
// retrieve date as string  
$date = sqlsrv_get_field( $stmt, 0 );  
  
if ( $date === false ) {  
   die( print_r( sqlsrv_errors(), true ));  
}  
  
$date_string = date_format( $date, 'jS, F Y' );  
echo "Date = $date_string\n";  
  
sqlsrv_close( $conn);  
?>  
```  
  
## Siehe auch  
[Abrufen von Daten](../content/Retrieving-Data.md)  
  
