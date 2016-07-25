---
title: "PDOStatement::fetch"
ms.custom: na
ms.date: 06/16/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4368e362-5bda-4da1-8462-33714683c39f
caps.latest.revision: 19
caps.handback.revision: 18
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
# PDOStatement::fetch
Ruft eine Zeile aus einem Resultset ab.  
  
## Syntax  
  
```  
  
mixed PDOStatement::fetch ([ $fetch_style[, $cursor_orientation[, $cursor_offset]]] );  
```  
  
#### Parameter  
$*fetch\_style*: Ein optionales \(Ganzzahl\)symbol, das das Format der Zeilendaten angibt. Eine Liste der möglichen Werte für $*fetch\_style* finden Sie im Abschnitt „Anmerkungen“. Der Standardwert ist PDO::FETCH\_BOTH. $*fetch\_style* in der Abrufmethode überschreibt die Angabe von $*fetch\_style* in der PDO::query-Methode.  
  
$*cursor\_orientation*: Ein optionales Symbol \(ganze Zahl\), welches die Zeile angibt, die abgerufen werden soll, wenn die prepare-Anweisung `PDO::ATTR_CURSOR => PDO::CURSOR_SCROLL` angibt. Eine Liste der möglichen Werte für $*cursor\_orientation* finden Sie im Abschnitt „Anmerkungen“. Ein Beispiel mit einem bildlauffähigen Cursor finden Sie unter [PDO::prepare](../Topic/PDO::prepare.md) .  
  
$*cursor\_offset*: Ein optionales Symbol \(ganze Zahl\), das die abzurufende Zeile anbigt, wenn $*cursor\_orientation* einen der Werte PDO::FETCH\_ORI\_ABS oder PDO::FETCH\_ORI\_REL aufweist und PDO::ATTR\_CURSOR gleich PDO::CURSOR\_SCROLL ist.  
  
## Rückgabewert  
Ein gemischter Wert, der eine Zeile oder „false“ zurückgibt.  
  
## Hinweise  
Der Cursor wird automatisch vorgerückt, wenn FETCH aufgerufen wird. Die folgende Tabelle enthält die Liste der möglichen Werte für $*fetch\_style*.  
  
|$*fetch\_style*|Beschreibung|  
|-------------------|---------------|  
|PDO::FETCH\_ASSOC|Gibt ein Array an, das von einem Spaltennamen indiziert ist.|  
|PDO::FETCH\_BOTH|Gibt ein Array an, das von einem Spaltennamen und einer 0\-basierten Reihenfolge indiziert ist. Dies ist die Standardeinstellung.|  
|PDO::FETCH\_BOUND|Gibt „true“ zurück und weist die Werte gemäß [PDOStatement::bindColumn](../Topic/PDOStatement::bindColumn.md)zu.|  
|PDO::FETCH\_CLASS|Erstellt eine Instanz und ordnet Spalten den benannten Eigenschaften zu.<br /><br />Rufen Sie [PDOStatement::setFetchMode](../Topic/PDOStatement::setFetchMode.md) auf, bevor Sie FETCH aufrufen.|  
|PDO::FETCH\_INTO|Aktualisiert eine Instanz der angeforderten Klasse.<br /><br />Rufen Sie [PDOStatement::setFetchMode](../Topic/PDOStatement::setFetchMode.md) auf, bevor Sie FETCH aufrufen.|  
|PDO::FETCH\_LAZY|Erstellt Namen von Variablen während des Zugriffs sowie ein unbenanntes Objekt.|  
|PDO::FETCH\_NUM|Gibt ein Array an, das von einer nullbasierten Spaltenreihenfolge indiziert ist.|  
|PDO::FETCH\_OBJ|Gibt ein unbenanntes Objekt mit Eigenschaftennamen an, die Spaltennamen zugeordnet sind.|  
  
Wenn sich der Cursor am Ende des Resultsets befindet \(die letzte Zeile wurde abgerufen und der Cursor befindet sich außerhalb der Begrenzung des Resultsets\) und es sich um einen Vorwärtscursor handelt \(PDO::ATTR\_CURSOR \= PDO::CURSOR\_FWDONLY\), schlagen nachfolgende FETCH\-Aufrufe fehl.  
  
Wenn der Cursor scrollfähig ist \(PDO::ATTR\_CURSOR \= PDO::CURSOR\_SCROLL\), wird FETCH den Cursor innerhalb der Begrenzung des Resultsets bewegen. Die folgende Tabelle enthält die Liste der möglichen Werte für $*cursor\_orientation*.  
  
|$*cursor\_orientation*|Beschreibung|  
|--------------------------|---------------|  
|PDO::FETCH\_ORI\_NEXT|Ruft die nächste Zeile ab. Dies ist die Standardeinstellung.|  
|PDO::FETCH\_ORI\_PRIOR|Ruft die vorherige Zeile ab.|  
|PDO::FETCH\_ORI\_FIRST|Ruft die erste Zeile ab.|  
|PDO::FETCH\_ORI\_LAST|Ruft die letzte Zeile ab.|  
|PDO::FETCH\_ORI\_ABS, *num*|Ruft die in $*cursor\_offset* angeforderte Zeile über die Zeilennummer ab.|  
|PDO::FETCH\_ORI\_REL, *num*|Ruft die in $*cursor\_offset* angeforderte Zeile über die relative Position von der aktuellen Position ab.|  
  
Wenn der für $*cursor\_offset* oder $*cursor\_orientation* angegebene Wert eine Position außerhalb der Grenzen des Resultsets ergibt, tritt ein Fehler beim Abruf auf.  
  
Unterstützung für PDO wurde in Version 2.0 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt.  
  
## Beispiel  
  
```  
<?php  
   $server = "(local)";  
   $database = "AdventureWorks";  
   $conn = new PDO( "sqlsrv:server=$server ; Database = $database", "", "");  
  
   print( "\n---------- PDO::FETCH_CLASS -------------\n" );  
   $stmt = $conn->query( "select * from HumanResources.Department order by GroupName" );  
  
   class cc {  
      function __construct( $arg ) {  
         echo "$arg";  
      }  
  
      function __toString() {  
         return $this->DepartmentID . "; " . $this->Name . "; " . $this->GroupName;  
      }  
   }  
  
   $stmt->setFetchMode(PDO::FETCH_CLASS, 'cc', array( "arg1 " ));  
   while ( $row = $stmt->fetch(PDO::FETCH_CLASS)) {   
      print($row . "\n");   
   }  
  
   print( "\n---------- PDO::FETCH_INTO -------------\n" );  
   $stmt = $conn->query( "select * from HumanResources.Department order by GroupName" );  
   $c_obj = new cc( '' );  
  
   $stmt->setFetchMode(PDO::FETCH_INTO, $c_obj);  
   while ( $row = $stmt->fetch(PDO::FETCH_INTO)) {   
      echo "$c_obj\n";  
   }  
  
   print( "\n---------- PDO::FETCH_ASSOC -------------\n" );  
   $stmt = $conn->query( "select * from Person.ContactType where ContactTypeID < 5 " );  
   $result = $stmt->fetch( PDO::FETCH_ASSOC );  
   print_r( $result );  
  
   print( "\n---------- PDO::FETCH_NUM -------------\n" );  
   $stmt = $conn->query( "select * from Person.ContactType where ContactTypeID < 5 " );  
   $result = $stmt->fetch( PDO::FETCH_NUM );  
   print_r ($result );  
  
   print( "\n---------- PDO::FETCH_BOTH -------------\n" );  
   $stmt = $conn->query( "select * from Person.ContactType where ContactTypeID < 5 " );  
   $result = $stmt->fetch( PDO::FETCH_BOTH );  
   print_r( $result );  
  
   print( "\n---------- PDO::FETCH_LAZY -------------\n" );  
   $stmt = $conn->query( "select * from Person.ContactType where ContactTypeID < 5 " );  
   $result = $stmt->fetch( PDO::FETCH_LAZY );  
   print_r( $result );  
  
   print( "\n---------- PDO::FETCH_OBJ -------------\n" );  
   $stmt = $conn->query( "select * from Person.ContactType where ContactTypeID < 5 " );  
   $result = $stmt->fetch( PDO::FETCH_OBJ );  
   print $result->Name;  
   print( "\n \n" );  
  
   print( "\n---------- PDO::FETCH_BOUND -------------\n" );  
   $stmt = $conn->query( "select * from Person.ContactType where ContactTypeID < 5 " );  
   $stmt->bindColumn('Name', $name);  
   $result = $stmt->fetch( PDO::FETCH_BOUND );  
   print $name;  
   print( "\n \n" );  
?>  
```  
  
## Siehe auch  
[PDOStatement-Klasse](../content/PDOStatement-Class.md)  
[PDO](http://go.microsoft.com/fwlink/?LinkID=187441)  
  
