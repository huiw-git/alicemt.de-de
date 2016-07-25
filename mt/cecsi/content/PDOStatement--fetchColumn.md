---
title: "PDOStatement::fetchColumn"
ms.custom: na
ms.date: 06/16/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6ebf385c-ddb0-4c53-9dc6-7df0d3740b04
caps.latest.revision: 8
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
# PDOStatement::fetchColumn
Gibt eine Spalte in einer Zeile zurück.  
  
## Syntax  
  
```  
  
string PDOStatement::fetchColumn ([ $column_number ] );  
```  
  
#### Parameter  
$*column\_number*: Eine optionale ganze Zahl, die die nullbasierte Spaltennummer angibt. Der Standardwert ist 0 \(die erste Spalte in der Zeile\).  
  
## Rückgabewert  
Eine Spalte oder „false“, wenn keine weiteren Zeilen vorhanden sind.  
  
## Hinweise  
Unterstützung für PDO wurde in Version 2.0 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt.  
  
## Beispiel  
  
```  
<?php  
   $server = "(local)";  
   $database = "AdventureWorks";  
   $conn = new PDO( "sqlsrv:server=$server ; Database = $database", "", "");  
  
   $stmt = $conn->query( "select * from Person.ContactType where ContactTypeID < 5 " );  
   while ( $result = $stmt->fetchColumn(1)) {   
      print($result . "\n");   
   }  
?>  
```  
  
## Siehe auch  
[PDOStatement-Klasse](../content/PDOStatement-Class.md)  
[PDO](http://go.microsoft.com/fwlink/?LinkID=187441)  
  
