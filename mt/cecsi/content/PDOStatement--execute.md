---
title: "PDOStatement::execute"
ms.custom: na
ms.date: 07/18/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c2e80566-fa41-4918-8521-cf2e05374cbd
caps.latest.revision: 12
caps.handback.revision: 11
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
# PDOStatement::execute
Führt eine Anweisung aus.  
  
## Syntax  
  
```  
  
bool PDOStatement::execute ([ $input ] );  
```  
  
#### Parameter  
*$input*: \(Optional\) Ein assoziatives Array das die Werte für Parametermarker enthält.  
  
## Rückgabewert  
„true“ bei Erfolg, andernfalls „false“.  
  
## Hinweise  
Anweisungen, die mit PDOStatement::execute ausgeführt werden, müssen erst mit [PDO::prepare](../Topic/PDO::prepare.md)vorbereitet werden. Informationen zum Angeben der direkten oder vorbereiteten Ausführung von Anweisungen finden Sie unter [Direkte Anweisungsausführung und vorbereitete Anweisungsausführung im PDO_SQLSRV-Treiber](../Topic/Direct%20Statement%20Execution%20and%20Prepared%20Statement%20Execution%20in%20the%20PDO_SQLSRV%20Driver.md).  
  
Alle Werte de Eingabeparameterarrays werden als PDO::PARAM\_STR-Werte behandelt.  
  
Falls die vorbereitete Anweisung Parametermarker enthält, müssen Sie entweder PDOStatement::bindParam aufrufen, um die PHP-Variablen an die Parametermarker zu binden, oder ein Array, das nur aus Eingabeparameterwerten besteht, weitergeben.  
  
Unterstützung für PDO wurde in Version 2.0 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt.  
  
## Beispiel  
  
```  
<?php  
$database = "AdventureWorks";  
$server = "(local)";  
$conn = new PDO( "sqlsrv:server=$server ; Database = $database", "", "");  
  
$query = "select * from Person.ContactType";  
$stmt = $conn->prepare( $query );  
$stmt->execute();  
  
while ( $row = $stmt->fetch( PDO::FETCH_ASSOC ) ){  
   print "$row[Name]\n";  
}  
  
echo "\n";  
$param = "Owner";  
$query = "select * from Person.ContactType where name = ?";  
$stmt = $conn->prepare( $query );  
$stmt->execute(array($param));  
  
while ( $row = $stmt->fetch( PDO::FETCH_ASSOC ) ){  
   print "$row[Name]\n";  
}  
?>  
```  
  
## Siehe auch  
[PDOStatement-Klasse](../content/PDOStatement-Class.md)  
[PDO](http://go.microsoft.com/fwlink/?LinkID=187441)  
  
