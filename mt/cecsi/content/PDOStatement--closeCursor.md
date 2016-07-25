---
title: "PDOStatement::closeCursor"
ms.custom: na
ms.date: 06/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8997ab61-e948-4d54-8d32-fc080d55525c
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
# PDOStatement::closeCursor
Schließt den Cursor und erlaubt erneute Ausführung der Anwendung.  
  
## Syntax  
  
```  
  
bool PDOStatement::closeCursor();  
```  
  
## Rückgabewert  
„true“ bei Erfolg, andernfalls „false“.  
  
## Hinweise  
„closeCursor“ ist wirksam, wenn die Verbindungsoption MultipleActiveResultSets auf „false“ gesetzt ist.  Weitere Informationen über die Option MultipleActiveResultSets finden Sie unter [Gewusst wie: Deaktivieren von mehreren aktiven Resultsets \(MARS\)](../Topic/How%20to:%20Disable%20Multiple%20Active%20Resultsets%20(MARS).md).  
  
Statt „closeCursor“ aufzurufen, können Sie auch einfach das Anweisungshandle auf NULL setzen.  
  
Unterstützung für PDO wurde in Version 2.0 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt.  
  
## Beispiel  
  
```  
<?php  
$database = "AdventureWorks";  
$server = "(local)";  
$conn = new PDO( "sqlsrv:server=$server ; Database = $database", "", "", array('MultipleActiveResultSets' => false ) );  
  
$stmt = $conn->prepare('SELECT * FROM Person.ContactType');  
  
$stmt2 = $conn->prepare('SELECT * FROM HumanResources.Department');  
  
$stmt->execute();  
  
$result = $stmt->fetch();  
print_r($result);  
  
$stmt->closeCursor();  
  
$stmt2->execute();  
$result = $stmt2->fetch();  
print_r($result);  
?>  
```  
  
## Siehe auch  
[PDOStatement-Klasse](../content/PDOStatement-Class.md)  
[PDO](http://go.microsoft.com/fwlink/?LinkID=187441)  
  
