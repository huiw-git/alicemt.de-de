---
title: "Vorgehensweise: Deaktivieren von Multiple Active Resultsets (MARS)"
ms.custom: na
ms.date: 06/16/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1912ad05-d0a4-40ff-8888-0d85bb36a807
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
# Vorgehensweise: Deaktivieren von Multiple Active Resultsets (MARS)
Wenn Sie eine Verbindung mit einer SQL Server-Datenquelle herstellen müssen, die Multiple Active Resultsets \(MARS\) nicht ermöglicht, können Sie die Verbindungsoption „MultipleActiveResultSets“ verwenden, um MARS zu deaktivieren oder zu aktivieren.  
  
## Verfahren  
  
#### Gehen Sie wie folgt vor, um die MARS-Unterstützung zu deaktivieren:  
  
-   Verwenden Sie die folgende Verbindungsoption:  
  
    ```  
    'MultipleActiveResultSets'=>false  
    ```  
  
    Wenn Ihre Anwendung versucht, eine Abfrage über eine Verbindung auszuführen, die ein geöffnetes aktives Resultset enthält, gibt der zweite Abfrageversuch die folgende Fehlerinformation zurück:  
  
    Die Verbindung kann diesen Vorgang nicht verarbeiten, da für eine Anweisung noch Ergebnisse ausstehen.  Rufen Sie entweder alle Ergebnisse auf, brechen Sie die Anweisung ab oder geben Sie sie frei, um die Verbindung anderen Abfragen zur Verfügung zu stellen. Weitere Informationen über die Verbindungsoption MultipleActiveResultSets finden Sie unter [Connection Options](../content/Connection-Options.md).  
  
## Beispiel  
Das folgende Beispiel zeigt die Vorgehensweise zum Deaktivieren der MARS-Unterstützung, unter Verwendung des SQLSRV-Treibers der [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)].  
  
```  
<?php  
/* Connect to the local server using Windows Authentication and  
specify the AdventureWorks database as the database in use. */  
$serverName = "MyServer";  
$connectionInfo = array( "Database"=>"AdventureWorks", 'MultipleActiveResultSets'=> false);  
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
Das folgende Beispiel zeigt die Vorgehensweise zum Deaktivieren der MARS-Unterstützung, unter Verwendung des PDO\_SQLSRV-Treibers von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)].  
  
```  
<?php  
// Connect to the local server using Windows Authentication and AdventureWorks database  
$serverName = "(local)";   
$database = "AdventureWorks";  
  
try {  
   $conn = new PDO(" sqlsrv:server=$serverName ; Database=$database ; MultipleActiveResultSets=false ", NULL, NULL);   
   $conn->setAttribute( PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION );   
}  
  
catch( PDOException $e ) {  
   die( "Error connecting to SQL Server" );   
}  
  
$conn = null;   
?>  
```  
  
## Siehe auch  
[Verbinden mit dem Server](../content/Connecting-to-the-Server.md)  
  
