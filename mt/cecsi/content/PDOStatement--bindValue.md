---
title: "PDOStatement::bindValue"
ms.custom: na
ms.date: 06/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 13bc4ece-420e-4887-8809-bf0705ddf126
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
# PDOStatement::bindValue
Bindet einen Wert an einen benannten Platzhalter oder Fragezeichenplatzhalter in der SQL-Anweisung.  
  
## Syntax  
  
```  
  
bool PDOStatement::bindValue( $parameter, $value [,$data_type] );  
```  
  
#### Parameter  
$*parameter*: Ein \(gemischter\) Parameterbezeichner. Ein Parametername \(:name\) für eine Anweisung, die benannte Platzhalter verwendet. Für eine vorbereitete Anweisung mit der Fragezeichensyntax stellt dieser den 1\-basierten Index des Parameters dar.  
  
$*value*: Der \(gemischte\) Wert, der an den Parameter gebunden wird.  
  
$*data\_type*: Der optionale Datentyp \(ganze Zahl\), der durch die Konstante PDO::PARAM\_\* dargestellt wird. Der Standardwert ist PDO::PARAM\_STR.  
  
## Rückgabewert  
„true“ bei Erfolg, andernfalls „false“.  
  
## Hinweise  
Unterstützung für PDO wurde in Version 2.0 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt.  
  
## Beispiel  
Dieses Beispiel zeigt, dass nachdem der Wert für $contact gebunden wurde, eine Änderung des Werts nicht den in der Abfrage übergebenen Wert ändert.  
  
```  
<?php  
$database = "AdventureWorks";  
$server = "(local)";  
$conn = new PDO( "sqlsrv:server=$server ; Database = $database", "", "");  
  
$contact = "Sales Agent";  
$stmt = $conn->prepare("select * from Person.ContactType where name = ?");  
$stmt->bindValue(1, $contact);  
$contact = "Owner";  
$stmt->execute();  
  
while ( $row = $stmt->fetch( PDO::FETCH_ASSOC ) ){  
   print "$row[Name]\n\n";  
}  
  
$stmt = null;  
$contact = "Sales Agent";  
$stmt = $conn->prepare("select * from Person.ContactType where name = :contact");  
$stmt->bindValue(':contact', $contact);  
$contact = "Owner";  
$stmt->execute();  
  
while ( $row = $stmt->fetch( PDO::FETCH_ASSOC ) ){  
   print "$row[Name]\n\n";  
}  
?>  
```  
  
## Siehe auch  
[PDOStatement-Klasse](../content/PDOStatement-Class.md)  
[PDO](http://go.microsoft.com/fwlink/?LinkID=187441)  
  
