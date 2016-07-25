---
title: "PDOStatement::columnCount"
ms.custom: na
ms.date: 06/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8d89a568-0c7c-40dd-9f54-db7313600df3
caps.latest.revision: 7
caps.handback.revision: 7
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
# PDOStatement::columnCount
Gibt die Anzahl der Spalten in einem Resultset zurück.  
  
## Syntax  
  
```  
  
int PDOStatement::columnCount ();  
```  
  
## Rückgabewert  
Gibt die Anzahl der Spalten in einem Resultset zurück. Gibt „0“ zurück, wenn das Resultset leer ist.  
  
## Hinweise  
Unterstützung für PDO wurde in Version 2.0 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt.  
  
## Beispiel  
  
```  
<?php  
$database = "AdventureWorks";  
$server = "(local)";  
$conn = new PDO( "sqlsrv:server=$server ; Database = $database", "", "");  
  
$query = "select * from Person.ContactType";  
$stmt = $conn->prepare( $query );  
print $stmt->columnCount();   // 0  
  
echo "\n";  
$stmt->execute();  
print $stmt->columnCount();  
  
echo "\n";  
$stmt = $conn->query("select * from HumanResources.Department");  
print $stmt->columnCount();  
?>  
```  
  
## Siehe auch  
[PDOStatement-Klasse](../content/PDOStatement-Class.md)  
[PDO](http://go.microsoft.com/fwlink/?LinkID=187441)  
  
