---
title: "sqlsrv_execute"
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
  - sqlsrv_execute
apitype: NA
ms.assetid: 38331bc2-4391-4f9f-aa83-9873dad605a0
caps.latest.revision: 24
caps.handback.revision: 24
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
# sqlsrv_execute
Führt eine zuvor vorbereitete Anweisung aus. Weitere Informationen zum Vorbereiten einer Anweisung für die Ausführung finden Sie unter [sqlsrv_prepare](../content/sqlsrv_prepare.md) .  
  
> [!NOTE]  
> Diese Funktion ist ideal  zum mehrfachen Ausführen einer vorbereiteten Anweisung mit verschiedenen Parameterwerten.  
  
## Syntax  
  
```  
  
sqlsrv_execute( resource $stmt)  
```  
  
#### Parameter  
*$stmt*: Eine Ressource, die die auszuführende Anweisung angibt. Weitere Informationen zum Erstellen einer Anweisungsressource finden Sie unter [sqlsrv_prepare](../content/sqlsrv_prepare.md).  
  
## Rückgabewert  
Ein boolescher Wert: **true** wenn die Anweisung erfolgreich ausgeführt wurde. Andernfalls lautet der Wert **false**.  
  
## Beispiel  
Das folgende Beispiel führt eine Anweisung durch, die ein Feld in der *Sales.SalesOrderDetail*-Tabelle in der [AdventureWorks](http://go.microsoft.com/fwlink/?LinkID=67739)-Datenbank aktualisiert. Das Beispiel setzt voraus, dass SQL Server und die AdventureWorks-Datenbank auf dem lokalen Computer installiert sind. Wenn das Beispiel über die Befehlszeile ausgeführt wird, werden alle Ausgaben in die Konsole geschrieben.  
  
```  
<?php  
/*Connect to the local server using Windows Authentication and  
specify the AdventureWorks database as the database in use. */  
$serverName = "(local)";  
$connectionInfo = array( "Database"=>"AdventureWorks");  
$conn = sqlsrv_connect( $serverName, $connectionInfo);  
if( $conn === false)  
{  
     echo "Could not connect.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Set up the Transact-SQL query. */  
$tsql = "UPDATE Sales.SalesOrderDetail   
         SET OrderQty = ( ?)   
         WHERE SalesOrderDetailID = ( ?)";  
  
/* Set up the parameters array. Parameters correspond, in order, to  
question marks in $tsql. */  
$params = array( 5, 10);  
  
/* Create the statement. */  
$stmt = sqlsrv_prepare( $conn, $tsql, $params);  
if( $stmt )  
{  
     echo "Statement prepared.\n";  
}  
else  
{  
     echo "Error in preparing statement.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Execute the statement. Display any errors that occur. */  
if( sqlsrv_execute( $stmt))  
{  
      echo "Statement executed.\n";  
}  
else  
{  
     echo "Error in executing statement.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Free the statement and connection resources. */  
sqlsrv_free_stmt( $stmt);  
sqlsrv_close( $conn);  
?>  
```  
  
## Siehe auch  
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
[Informationen zu den Codebeispielen in der Dokumentation](../content/About-Code-Examples-in-the-Documentation.md)  
[sqlsrv_query](../content/sqlsrv_query.md)  
  
