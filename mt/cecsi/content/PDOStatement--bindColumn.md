---
title: "PDOStatement::bindColumn"
ms.custom: na
ms.date: 06/16/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bbdcea53-d23d-4769-89a0-95c7cf4d5390
caps.latest.revision: 14
caps.handback.revision: 13
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
# PDOStatement::bindColumn
Bindet eine Variable an eine Spalte im Resultset.  
  
## Syntax  
  
```  
  
bool PDOStatement::bindColumn($column, &$param[, $type[, $maxLen[, $driverdata ]]] );  
```  
  
#### Parameter  
$*column*: Die \(gemischte\) Nummer der Spalte \(laut einem auf 1 basierenden Index\) oder der Name der Spalte im Resultset.  
  
&$*param*: Der \(gemischte\) Name der PHP-Variable, an die die Spalte gebunden werden soll.  
  
$*type*: Der optionale Datentyp des Parameters, durch eine PDO::PARAM\_\*-Konstante dargestellt  
  
$*maxLen*: Optionale ganze Zahl, die von den Microsoft-Treibern für PHP für SQL Server nicht verwendet wird.  
  
$$*driverdata*: Optionale\(r\) gemischte(r) Parameter für den Treiber. Beispielsweise können Sie PDO::SQLSRV\_ENCODING\_\-UTF8 angeben, um die Spalte an eine Variable als UTF-8codierte Zeichenfolge zu binden.  
  
## Rückgabewert  
TRUE bei Erfolg, andernfalls FALSE.  
  
## Hinweise  
Unterstützung für PDO wurde in Version 2.0 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt.  
  
## Beispiel  
Dieses Beispiel zeigt, wie eine Variable an eine Spalte im Resultset gebunden werden kann.  
  
```  
<?php  
$database = "AdventureWorks";  
$server = "(local)";  
$conn = new PDO( "sqlsrv:server=$server ; Database = $database", "", "");  
  
$query = "SELECT Title, FirstName, EmailAddress FROM Person.Contact where LastName = 'Estes'";  
$stmt = $conn->prepare($query);  
$stmt->execute();  
  
$stmt->bindColumn('EmailAddress', $email);  
while ( $row = $stmt->fetch( PDO::FETCH_BOUND ) ){  
   echo "$email\n";  
}  
?>  
```  
  
## Siehe auch  
[PDOStatement-Klasse](../content/PDOStatement-Class.md)  
[PDO](http://go.microsoft.com/fwlink/?LinkID=187441)  
  
