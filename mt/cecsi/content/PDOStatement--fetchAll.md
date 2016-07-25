---
title: "PDOStatement::fetchAll"
ms.custom: na
ms.date: 06/16/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: be74188a-77cd-4d19-b16e-77278373c979
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
# PDOStatement::fetchAll
Gibt die Zeilen in einem Resultset in einem Array zurück.  
  
## Syntax  
  
```  
  
array PDOStatement::fetchAll([ $fetch_style[, $column_index ][, ctor_args]] );  
```  
  
#### Parameter  
$*fetch\_style*: Ein Symbol \(ganze Zahl\), welches das Format der Daten aus der Zeile angibt. Unter [PDOStatement::fetch](../Topic/PDOStatement::fetch.md) finden Sie eine Liste der Werte. PDO::FETCH\_COLUMN ist ebenfalls zulässig. PDO::FETCH\_BOTH ist der Standardwert.  
  
$*column\_index*: Ein Integerwert, der die zurückzugebende Spalte darstellt, falls für $*fetch\_style* PDO::FETCH\_COLUMN festgelegt ist. Der Standardwert ist 0.  
  
$*ctor\_args*: Ein Array der Parameter für einen Klassenkonstruktor, wenn für $*fetch\_style* PDO::FETCH\_CLASS oder PDO::FETCH\_OBJ festgelegt ist.  
  
## Rückgabewert  
Ein Array der verbleibenden Zeilen im Resultset oder „false“ falls der Methodenaufruf fehlschlägt.  
  
## Hinweise  
Unterstützung für PDO wurde in Version 2.0 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt.  
  
## Beispiel  
  
```  
<?php  
   $server = "(local)";  
   $database = "AdventureWorks";  
   $conn = new PDO( "sqlsrv:server=$server ; Database = $database", "", "");  
  
   print "-----------\n";  
   $stmt = $conn->query( "select * from Person.ContactType where ContactTypeID < 5 " );  
   $result = $stmt->fetchall(PDO::FETCH_BOTH);  
   print_r( $result );  
   print "\n-----------\n";  
  
   print "-----------\n";  
   $stmt = $conn->query( "select * from Person.ContactType where ContactTypeID < 5 " );  
   $result = $stmt->fetchall(PDO::FETCH_NUM);  
   print_r( $result );  
   print "\n-----------\n";  
  
   $stmt = $conn->query( "select * from Person.ContactType where ContactTypeID < 5 " );  
   $result = $stmt->fetchall(PDO::FETCH_COLUMN, 1);  
   print_r( $result );  
   print "\n-----------\n";  
  
   class cc {  
      function __construct( $arg ) {  
         echo "$arg\n";  
      }  
  
      function __toString() {  
         echo "To string\n";  
      }  
   };  
  
   $stmt = $conn->query( 'SELECT TOP(2) * FROM Person.ContactType' );  
   $all = $stmt->fetchAll( PDO::FETCH_CLASS, 'cc', array( 'Hi!' ));  
   var_dump( $all );  
?>  
```  
  
## Siehe auch  
[PDOStatement-Klasse](../content/PDOStatement-Class.md)  
[PDO](http://go.microsoft.com/fwlink/?LinkID=187441)  
  
