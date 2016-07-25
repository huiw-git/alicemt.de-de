---
title: "PDOStatement::rowCount"
ms.custom: na
ms.date: 06/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0569f26a-2376-4c20-8813-bd3c87d0ae9f
caps.latest.revision: 10
caps.handback.revision: 9
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
# PDOStatement::rowCount
Gibt die Anzahl der Zeilen zurück, die durch die letzte Anweisung hinzugefügt, gelöscht oder geändert wurden  
  
## Syntax  
  
```  
  
int PDOStatement::rowCount ();  
```  
  
## Rückgabewert  
Die Anzahl der hinzugefügten, gelöschten oder geänderten Zeilen.  
  
## Hinweise  
Falls die letzte SQL-Anweisung, die durch die zugeordnete PDO-Anweisung ausgeführt wurde, eine SELECT-Anweisung war, gibt ein PDO::CURSOR\_FWDONLY-Cursor den Wert \-1 zurück. A PDO::CURSOR\_SCROLLABLE -Cursor gibt die Anzahl der Zeilen in dem Resultset zurück.  
  
Unterstützung für PDO wurde in Version 2.0 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt.  
  
## Beispiel  
Dieses Beispiel zeigt zwei Verwendungen von „rowCount“. Die erste gibt die Anzahl der Zeilen zurück, die der Tabelle hinzugefügt wurden. Die zweite Verwendung zeigt, dass „rowCount“ die Anzahl der Zeilen in einem Resultset ausgeben kann, wenn Sie einen bildlauffähigen Cursor spezifizieren.  
  
```  
<?php  
$database = "Test";  
$server = "(local)";  
$conn = new PDO( "sqlsrv:server=$server ; Database = $database", "", "");  
  
$col1 = 'a';  
$col2 = 'b';  
  
$query = "insert into Table2(col1, col2) values(?, ?)";  
$stmt = $conn->prepare( $query );  
$stmt->execute( array( $col1, $col2 ) );  
print $stmt->rowCount();  
  
echo "\n\n";  
  
$con = null;  
$database = "AdventureWorks";  
$conn = new PDO( "sqlsrv:server=$server ; Database = $database", "", "");  
  
$query = "select * from Person.ContactType";  
$stmt = $conn->prepare( $query, array(PDO::ATTR_CURSOR => PDO::CURSOR_SCROLL));  
$stmt->execute();  
print $stmt->rowCount();  
?>  
```  
  
## Siehe auch  
[PDOStatement-Klasse](../content/PDOStatement-Class.md)  
[PDO](http://go.microsoft.com/fwlink/?LinkID=187441)  
  
