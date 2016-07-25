---
title: "Vorgehensweise: Herstellen einer Verbindung mithilfe der Windows-Authentifizierung"
ms.custom: na
ms.date: 06/28/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f403a4e0-b0a8-4939-9dc1-e1209626367e
caps.latest.revision: 35
caps.handback.revision: 34
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
# Vorgehensweise: Herstellen einer Verbindung mithilfe der Windows-Authentifizierung
Standardmäßig verwenden die [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] für die Verbindung zu SQL Server die Windows-Authentifizierung. Es ist wichtig zu beachten, dass dies in den meisten Szenarien bedeutet, dass die Prozess\- oder Threadidentität des Servers \(falls der Webserver Identitätswechsel verwendet\) dazu verwendet wird, sich mit dem Server und nicht mit der Identität des Endbenutzers zu verbinden.  
  
Bitte beachten Sie die folgenden Punkte, wenn Sie die Windows-Authentifizierung verwenden, um eine Verbindung mit einem SQL Server herzustellen:  
  
-   Die Anmeldeinformationen, unter denen der Webserverprozess \(oder Thread\) läuft, müssen einer gültigen SQL Server-Anmeldung zugeordnet sein, um eine Verbindung herstellen zu können.  
  
-   Wenn sich SQL Server und der Webserver auf unterschiedlichen Computern befinden, müssen für SQL Server Remoteverbindungen aktiviert sein.  
  
> [!NOTE]  
> Sie können Verbindungsattribute wie z. B. *Database* und *ConnectionPooling* festlegen, wenn Sie eine Verbindung herstellen. Eine vollständige Liste der unterstützten Verbindungsattribute finden Sie unter [Connection Options](../content/Connection-Options.md).  
  
Aus folgenden Gründen sollte, wann immer möglich, die Windows-Authentifizierung für die Verbindung zu SQL Server verwendet werden:  
  
-   Während der Authentifizierung werden keine Anmeldeinformationen über das Netzwerk übergeben. Benutzernamen und Kennwörter werden nicht in die Verbindungszeichenfolge der Datenbank eingebettet. Dies bedeutet, dass böswillige Benutzer oder Angreifer die Anmeldeinformationen nicht durch Überwachen des Netzwerks oder durch Einsehen der Verbindungszeichenfolgen in Konfigurationsdateien erhalten können.  
  
-   Die Benutzer werden über ein zentrales Kontenmanagement verwaltet. Sicherheitsrichtlinien wie z. B. Gültigkeitszeiträume für Passwörter, Vorgaben zur Mindestlänge von Passwörtern und die Sperrung von Konten nach mehreren ungültigen Anmeldeanfragen werden umgesetzt.  
  
Wenn die Windows-Authentifizierung für Sie nicht praktikabel ist, lesen Sie [How to: Connect Using SQL Server Authentication](../Topic/How%20to:%20Connect%20Using%20SQL%20Server%20Authentication.md).  
  
## Beispiel  
Im folgenden Beispiel wird bei Verwendung des SQLSRV-Treibers von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]die Windows-Authentifizierung verwendet, um eine Verbindung mit einer lokalen SQL Server-Instanz herzustellen. Nach dem Aufbau der Verbindung wird eine Anfrage an den Benutzer gestellt, den Benutzer anzumelden, der auf die Datenbank zugreifen möchte.  
  
Das Beispiel setzt voraus, dass SQL Server und die [AdventureWorks](http://go.microsoft.com/fwlink/?LinkID=67739) -Datenbank auf dem lokalen Computer installiert sind. Wenn das Beispiel über den Browser ausgeführt wird, werden alle Ausgaben im Browser geschrieben.  
  
```  
<?php  
/* Specify the server and connection string attributes. */  
$serverName = "(local)";  
$connectionInfo = array( "Database"=>"AdventureWorks");  
  
/* Connect using Windows Authentication. */  
$conn = sqlsrv_connect( $serverName, $connectionInfo);  
if( $conn === false )  
{  
     echo "Unable to connect.</br>";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Query SQL Server for the login of the user accessing the  
database. */  
$tsql = "SELECT CONVERT(varchar(32), SUSER_SNAME())";  
$stmt = sqlsrv_query( $conn, $tsql);  
if( $stmt === false )  
{  
     echo "Error in executing query.</br>";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Retrieve and display the results of the query. */  
$row = sqlsrv_fetch_array($stmt);  
echo "User login: ".$row[0]."</br>";  
  
/* Free statement and connection resources. */  
sqlsrv_free_stmt( $stmt);  
sqlsrv_close( $conn);  
?>  
```  
  
## Beispiel  
Das folgende Beispiel verwendet den PDO\_SQLSRV-Treiber, um dasselbe Ergebnis zu erreichen wie das vorherige Beispiel.  
  
```  
<?php  
try {  
   $conn = new PDO( "sqlsrv:Server=(local);Database=AdventureWorks", NULL, NULL);   
   $conn->setAttribute( PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION );  
}  
  
catch( PDOException $e ) {  
   die( "Error connecting to SQL Server" );   
}  
  
echo "Connected to SQL Server\n";  
  
$query = 'select * from Person.ContactType';   
$stmt = $conn->query( $query );   
while ( $row = $stmt->fetch( PDO::FETCH_ASSOC ) ){   
   print_r( $row );   
}  
?>  
```  
  
## Siehe auch  
[Vorgehensweise: Herstellen einer Verbindung mithilfe der SQL Server-Authentifizierung](../Topic/How%20to:%20Connect%20Using%20SQL%20Server%20Authentication.md)  
[Programmierhandbuch für den PHP-SQL-Treiber](../content/Programming-Guide-for-PHP-SQL-Driver.md)
[Informationen zu den Codebeispielen in der Dokumentation](../content/About-Code-Examples-in-the-Documentation.md)  
[Vorgehensweise: Erstellen einer SQL Server-Anmeldung](http://go.microsoft.com/fwlink/?LinkId=106325)  
[Vorgehensweise: Erstellen eines Datenbankbenutzers](http://go.microsoft.com/fwlink/?LinkId=106327)  
[Verwalten von Benutzern, Rollen und Anmeldungen](http://go.microsoft.com/fwlink/?LinkId=106329)  
[Trennung von Benutzer und Schema](http://go.microsoft.com/fwlink/?LinkId=106330)  
[Erteilen von Objektberechtigungen \(Transact-SQL\-\)](http://go.microsoft.com/fwlink/?LinkId=106332)  
  
