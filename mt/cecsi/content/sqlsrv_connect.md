---
title: "sqlsrv_connect"
ms.custom: na
ms.date: 07/18/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - sqlsrv_connect
apitype: NA
ms.assetid: 37836b49-258e-45ce-9549-b8bd85d6952d
caps.latest.revision: 67
caps.handback.revision: 66
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
# sqlsrv_connect
Erstellt eine Verbindungsressource und öffnet eine Verbindung. Standardmäßig wird versucht, die Verbindung unter Verwendung der Windows-Authentifizierung herzustellen.  
  
## Syntax  
  
```  
  
sqlsrv_connect( string $serverName [, array $connectionInfo])  
```  
  
#### Parameter  
*$serverName*: Eine Zeichenfolge, die den Namen des Servers angibt, zu dem eine Verbindung erstellt werden soll. Ein Instanzname \(z. B. „MeinServer\\InstanzName“\) oder Port \(z. B. „MeinServer, 1521“\) kann als Teil dieser Zeichenfolge enthalten sein. Eine vollständige Beschreibung der Optionen für diesen Parameter finden Sie im Abschnitt „Server-Schlüsselwort in den Kennwörtern der Verbindungszeichenfolgen des ODCB-Treibers“. Diesen finden Sie unter [Verwenden von Schlüsselwörtern für Verbindungszeichenfolgen mit SQL Native Client](http://go.microsoft.com/fwlink/?LinkId=105504).  
  
Ab Version 3.0 der [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]können Sie auch eine LocalDB-Instanz mit `"(localdb)\instancename"`angeben. Weitere Informationen finden Sie unter [PHP Driver for SQL Server Support for LocalDB](../Topic/PHP%20Driver%20for%20SQL%20Server%20Support%20for%20LocalDB.md).  
  
Zusätzlich können Sie ab der Version 3.0 der [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]einen virtuellen Netzwerknamen angeben, um sich mit einer AlwaysOn-Verfügbarkeitsgruppe zu verbinden. Weitere Informationen zur [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]-Untertützung für [!INCLUDE[ssHADR](../content/includes/ssHADR_md.md)] finden Sie unter [PHP Driver for SQL Server Support for High Availability, Disaster Recovery (Unterstützung für hohe Verfügbarkeit im PHP-Treiber für SQL Server, Notfallwiederherstellung)](../Topic/PHP%20Driver%20for%20SQL%20Server%20Support%20for%20High%20Availability,%20Disaster%20Recovery.md).  
  
*$connectionInfo* \[OPTIONAL\]: ein assoziatives **Array**, das Verbindungsattribute enthält \(z. B. **Array**\(„Database“ \= > „AdventureWorks“\)\). Unter [Connection Options](../content/Connection-Options.md) finden Sie eine Liste der unterstützten Schlüssel für das Array.  
  
## Rückgabewert  
Eine PHP-Verbindungsressource. Wenn eine Verbindung nicht erfolgreich erstellt und geöffnet werden kann, wird **false** zurückgegeben.  
  
## Hinweise  
Wenn im optionalen *$connectionInfo* -Parameter keine Werte für die Schlüssel *UID* und *PWD* angegeben sind, wird versucht, die Verbindung mithilfe der Windows-Authentifizierung herzustellen. Weitere Informationen zur Herstellung einer Verbindung mit dem Server finden Sie unter [How to: Connect Using Windows Authentication](../Topic/How%20to:%20Connect%20Using%20Windows%20Authentication.md) und [How to: Connect Using SQL Server Authentication](../Topic/How%20to:%20Connect%20Using%20SQL%20Server%20Authentication.md).  
  
## Beispiel  
Das folgende Beispiel erstellt und öffnet eine Verbindung mit Windows-Authentifizierung. Das Beispiel setzt voraus, dass SQL Server und die [AdventureWorks-Datenbank](http://www.codeplex.com/SqlServerSamples) auf dem lokalen Computer installiert sind. Wenn das Beispiel über die Befehlszeile ausgeführt wird, werden alle Ausgaben in die Konsole geschrieben.  
  
```  
<?php  
/*  
Connect to the local server using Windows Authentication and specify  
the AdventureWorks database as the database in use. To connect using  
SQL Server Authentication, set values for the "UID" and "PWD"  
 attributes in the $connectionInfo parameter. For example:  
$connectionInfo = array("UID" => $uid, "PWD" => $pwd, "Database"=>"AdventureWorks");  
*/  
$serverName = "(local)";  
$connectionInfo = array( "Database"=>"AdventureWorks");  
$conn = sqlsrv_connect( $serverName, $connectionInfo);  
  
if( $conn )  
{  
     echo "Connection established.\n";  
}  
else  
{  
     echo "Connection could not be established.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
//-----------------------------------------------  
// Perform operations with connection.  
//-----------------------------------------------  
  
/* Close the connection. */  
sqlsrv_close( $conn);  
?>  
```  
  
## Siehe auch  
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
[Verbinden mit dem Server](../content/Connecting-to-the-Server.md)  
[Informationen zu den Codebeispielen in der Dokumentation](../content/About-Code-Examples-in-the-Documentation.md)  
  
