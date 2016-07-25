---
title: "PDOStatement::errorCode"
ms.custom: na
ms.date: 06/16/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4161abec-c12b-444e-9de5-f1dac7b3e0e4
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
# PDOStatement::errorCode
Ruft den SQLSTATE des letzten Vorgangs auf dem Statementobjekt der Datenbank auf.  
  
## Syntax  
  
```  
  
string PDOStatement::errorCode();  
```  
  
## Rückgabewert  
Gibt ein SQLSTATE mit fünf Zeichen als Zeichenfolge oder NULL zurück, wenn kein Vorgang über das Anweisungshandle erfolgte.  
  
## Hinweise  
Unterstützung für PDO wurde in Version 2.0 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt.  
  
## Beispiel  
Dieses Beispiel zeigt eine SQL-Abfrage, die einen Fehler aufweist.  Der Fehlercode wird angezeigt.  
  
```  
<?php  
$conn = new PDO( "sqlsrv:server=(local) ; Database = AdventureWorks", "", "");  
$stmt = $conn->prepare('SELECT * FROM Person.Addressx');  
  
$stmt->execute();  
print $stmt->errorCode();  
?>  
```  
  
## Siehe auch  
[PDOStatement-Klasse](../content/PDOStatement-Class.md)  
[PDO](http://go.microsoft.com/fwlink/?LinkID=187441)  
  
