---
title: "PDO::query"
ms.custom: na
ms.date: 07/18/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f6f5e6d4-8ca9-4f06-89ed-de65ad3952a2
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
# PDO::query
Führt eine SQL-Abfrage aus und gibt ein Resultset als PDOStatement-Objekt zurück.  
  
## Syntax  
  
```  
  
PDOStatement PDO::query ($statement[, $fetch_style);  
```  
  
#### Parameter  
*$statement*: Die SQL-Anweisung, die Sie ausführen möchten.  
  
*$fetch\_style*: Die optionalen Anweisungen zum Ausführen der Abfrage. Weitere Details finden Sie im Abschnitt „Anmerkungen“. $*fetch\_style* in PDO::query kann mit $*fetch\_style* in PDO::fetch überschrieben werden.  
  
## Rückgabewert  
Wenn der Aufruf erfolgreich ist, gibt PDO::query ein PDOStatement-Objekt zurück. Wenn der Aufruf fehlschlägt, löst PDO::query ein PDOException-Objekt aus oder gibt „false“ zurück, abhängig von der Einstellung für PDO::ATTR\_ERRMODE.  
  
## Ausnahmen  
PDOException  
  
## Hinweise  
Bei einer mithilfe von PDO::query ausgeführten Abfrage wird entweder eine vorbereitete Anweisung ausgeführt oder die Abfrage wird direkt durchgeführt. Dies hängt von der Einstellung für PDO::SQLSRV\_ATTR\_DIRECT\_QUERY ab. Weitere Informationen finden Sie unter [Direkte Ausführung von Anweisungen und vorbereitete Ausführung von Anweisungen im PDO_SQLSRV-Treiber](../Topic/Direct%20Statement%20Execution%20and%20Prepared%20Statement%20Execution%20in%20the%20PDO_SQLSRV%20Driver.md) (Direct Statement Execution and Prepared Statement Execution in the PDO_SQLSRV Driver).  
  
PDO::SQLSRV\_ATTR\_QUERY\_TIMEOUT wirkt sich auf das Verhalten von PDO::exec aus. Weitere Informationen finden Sie unter [PDO::setAttribute](../Topic/PDO::setAttribute.md).  
  
Sie können die folgenden Optionen für $*fetch\_style* angeben.  
  
|Style|Beschreibung|  
|---------|---------------|  
|PDO::FETCH\_COLUMN, *Zahl*|Abfragen von Daten in der angegebenen Spalte. Die erste Spalte in der Tabelle ist die Spalte „0“.|  
|PDO::FETCH\_CLASS, '*Klassenname*', array\( *Argumentmliste* \)|Erstellt eine Instanz einer Klasse und weist Eigenschaften in der Klasse Spaltennamen zu. Wenn der Konstruktor der Klasse einen oder mehrere Parameter akzeptiert, können Sie auch eine *arglist*übergeben.|  
|PDO::FETCH\_CLASS, '*Klassenname*'|Weist Eigenschaften in einer vorhandenen Klasse Spaltennamen zu|  
  
Rufen Sie vor dem erneuten Aufrufen von PDO::query das PDOStatement::closeCursor auf, um zum PDOSTATEMENT-Objekt gehörende Datenbankressourcen freizugeben.  
  
Sie können ein PDOStatement-Objekt schließen, indem Sie dafür den Wert NULL festlegen.  
  
Wird für alle Daten in einem Resultset kein Abrufvorgang (FETCH) ausgeführt, wird der nächste Aufruf PDO::query nicht fehlschlagen.  
  
Unterstützung für PDO wurde in Version 2.0 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt.  
  
## Beispiel  
Dieses Beispiel zeigt mehrere Abfragen.  
  
```  
<?php  
$database = "AdventureWorks";  
$conn = new PDO( "sqlsrv:server=(local) ; Database = $database", "", "");  
$conn->setAttribute( PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION );  
$conn->setAttribute( PDO::SQLSRV_ATTR_QUERY_TIMEOUT, 1 );  
  
$query = 'select * from Person.ContactType';  
  
// simple query  
$stmt = $conn->query( $query );  
while ( $row = $stmt->fetch( PDO::FETCH_ASSOC ) ){  
   print_r( $row['Name'] ."\n" );  
}  
  
echo "\n........ query for a column ............\n";  
  
// query for one column  
$stmt = $conn->query( $query, PDO::FETCH_COLUMN, 1 );  
while ( $row = $stmt->fetch() ){  
   echo "$row\n";  
}  
  
echo "\n........ query with a new class ............\n";  
$query = 'select * from HumanResources.Department order by GroupName';  
// query with a class  
class cc {  
   function __construct( $arg ) {  
      echo "$arg";  
   }  
  
   function __toString() {  
      return $this->DepartmentID . "; " . $this->Name . "; " . $this->GroupName;  
   }  
}  
  
$stmt = $conn->query( $query, PDO::FETCH_CLASS, 'cc', array( "arg1 " ));  
  
while ( $row = $stmt->fetch() ){  
   echo "$row\n";  
}  
  
echo "\n........ query into an existing class ............\n";  
$c_obj = new cc( '' );  
$stmt = $conn->query( $query, PDO::FETCH_INTO, $c_obj );  
while ( $stmt->fetch() ){  
   echo "$c_obj\n";  
}  
  
$stmt = null;  
?>  
```  
  
## Siehe auch  
[PDO-Klasse](../content/PDO-Class.md)  
[PDO](http://go.microsoft.com/fwlink/?LinkID=187441)  
  
