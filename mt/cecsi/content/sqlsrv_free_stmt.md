---
title: "sqlsrv_free_stmt"
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
  - sqlsrv_free_stmt
apitype: NA
ms.assetid: 3c71f432-36ad-41e1-8ac7-587c82539448
caps.latest.revision: 21
caps.handback.revision: 20
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
# sqlsrv_free_stmt
Gibt alle der angegebenen Anweisung zugeordneten Ressourcen frei. Die Anweisung kann nicht erneut verwendet werden, nachdem diese Funktion aufgerufen wurde.  
  
## Syntax  
  
```  
  
sqlsrv_free_stmt( resource $stmt)  
```  
  
#### Parameter  
*$stmt*: Die Anweisung, die geschlossen werden soll.  
  
## Rückgabewert  
Der boolesche Wert **true** , außer die Funktion wird mit einem ungültigen Parameter aufgerufen. Wenn die Funktion mit einem ungültigen Parameter aufgerufen wird, wird **false** zurückgegeben.  
  
> [!NOTE]  
> **NULL** ist ein gültiger Parameter für diese Funktion. Dadurch kann die Funktion mehrmals in einem Skript aufgerufen werden. Wenn Sie z. B. eine Verbindung in einem Fehlerzustand freigeben und sie erneut am Ende des Skripts freigeben, wird der zweite Aufruf von **sqlsrv\_free\_stmt** den Wert **true** zurückgeben, da der erste Aufruf von **sqlsrv\_free\_stmt** \(im Fehlerzustand\) die Verbindungsressource auf **NULL** setzt.  
  
## Beispiel  
Das folgende Beispiel erstellt eine Anwendungsressource, führt eine einfache Abfrage durch und ruft **sqlsrv\_free\_stmt** auf, um alle der Anweisung zugeordneten Ressourcen freizugeben. Das Beispiel setzt voraus, dass SQL Server und die [AdventureWorks](http://go.microsoft.com/fwlink/?LinkID=67739) -Datenbank auf dem lokalen Computer installiert sind. Wenn das Beispiel über die Befehlszeile ausgeführt wird, werden alle Ausgaben in die Konsole geschrieben.  
  
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
  
$stmt = sqlsrv_query( $conn, "SELECT * FROM Person.Contact");  
if( $stmt )  
{  
     echo "Statement executed.\n";  
}  
else  
{  
     echo "Query could not be executed.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/*-------------------------------  
     Process query results here.  
-------------------------------*/  
  
/* Free the statement and connection resources. */  
sqlsrv_free_stmt( $stmt);  
sqlsrv_close( $conn);  
?>  
```  
  
## Siehe auch  
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
[Informationen zu den Codebeispielen in der Dokumentation](../content/About-Code-Examples-in-the-Documentation.md)  
[sqlsrv_cancel](../content/sqlsrv_cancel.md)  
  
