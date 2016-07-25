---
title: "PDO::prepare"
ms.custom: na
ms.date: 07/18/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a8b16fdc-c748-49be-acf2-a6ac7432d16b
caps.latest.revision: 28
caps.handback.revision: 27
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
# PDO::prepare
Bereitet eine Anweisung für die Ausführung vor.  
  
## Syntax  
  
```  
  
PDOStatement PDO::prepare ( $statement [, array(key_pair)] )  
```  
  
#### Parameter  
$*statement*: Eine Zeichenfolge, die die SQL-Anweisung enthält.  
  
*key\_pair*: Ein Array, das einen Attributnamen und einen Wert enthält. Weitere Informationen finden Sie im Abschnitt zu den Hinweisen.  
  
## Rückgabewert  
Bei Erfolg wird ein PDOStatement-Objekt zurückgegeben. Bei einem Fehler wird entweder ein PDOException-Objekt oder „false“ zurückgegeben, abhängig vom Wert für PDO::ATTR\_ERRMODE.  
  
## Hinweise  
[!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] wertet keine vorbereiteten Anweisungen vor der Ausführung aus.  
  
In der folgenden Tabelle sind die möglichen Werte für *key\_pair* aufgelistet.  
  
|Key|Beschreibung|  
|-------|---------------|  
|PDO::ATTR\_CURSOR|Definiert das Cursorverhalten. Der Standardwert ist PDO::CURSOR\_FWDONLY. PDO::CURSOR\_SCROLL ist ein statischer Cursor.<br /><br />Beispiel: `array( PDO::ATTR_CURSOR => PDO::CURSOR_FWDONLY )`.<br /><br />Wenn Sie PDO::CURSOR\_SCROLL verwenden, können Sie auch PDO::SQLSRV\_ATTR\_CURSOR\_SCROLL\_TYPE verwenden, wie nachstehend beschrieben.<br /><br />Weitere Informationen zu Ergebnismengen und Cursorn im PDO\_SQLSRV-Treiber finden Sie unter [Cursortypen &#40;PDO_SQLSRV-Treiber&#41;](../Topic/Cursor%20Types%20(PDO_SQLSRV%20Driver).md).|  
|PDO::ATTR\_EMULATE\_PREPARES|Der Zweck von PDO::ATTR\_EMULATE\_PREPARES ist im [PHP-Handbuch](http://us3.php.net/pdo) beschrieben.<br /><br />[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] unterstützt in einigen [!INCLUDE[tsql](../content/includes/tsql_md.md)] -Klauseln keine benannten oder positionellen Parameter.<br /><br />Wenn Sie Parameter in einer [!INCLUDE[tsql](../content/includes/tsql_md.md)]-Klausel Ihrer PHP-Anwendung verwenden müssen, die einen Fehler auf dem Server generieren, können Sie für das Attribut PDO::ATTR\_EMULATE\_PREPARES den Wert „true“ festlegen. Beispiel:<br /><br />`PDO::ATTR_EMULATE_PREPARES => true`<br /><br />Standardmäßig ist dieses Attribut auf "false" festgelegt.<br /><br />**Hinweis:** Bei der Verwendung von `PDO::ATTR_EMULATE_PREPARES => true` kommt der Sicherheitsgewinn durch parametrisierte Anfragen nicht zum Tragen. Ihre Anwendung sollte sicherstellen, dass die an den/die Parameter gebunden Daten keinen bösartigen [!INCLUDE[tsql](../content/includes/tsql_md.md)]-Code enthalten.|  
|PDO::SQLSRV\_ATTR\_ENCODING|PDO::SQLSRV\_ENCODING\_UTF8 \(Standardwert\)<br /><br />PDO::SQLSRV\_ENCODING\_SYSTEM<br /><br />PDO::SQLSRV\_ENCODING\_BINARY|  
|PDO::SQLSRV\_ATTR\_DIRECT\_QUERY|Wird hierfür der Wert „true“ festgelegt, werden Abfragen direkt ausgeführt. Der Wert „false“ sorgt dafür, dass vorbereitete Anweisungen ausgeführt werden. Weitere Informationen zu PDO::SQLSRV\_ATTR\_DIRECT\_QUERY finden Sie unter [Direkte Anweisungsausführung und vorbereitete Anweisungsausführung im PDO_SQLSRV-Treiber](../Topic/Direct%20Statement%20Execution%20and%20Prepared%20Statement%20Execution%20in%20the%20PDO_SQLSRV%20Driver.md).|  
|PDO::SQLSRV\_ATTR\_QUERY\_TIMEOUT|Weitere Informationen finden Sie unter [PDO::setAttribute](../Topic/PDO::setAttribute.md).|  
  
Wenn Sie PDO::ATTR\_CURSOR \=> PDO::CURSOR\_SCROLL verwenden, können Sie PDO::SQLSRV\_ATTR\_CURSOR\_SCROLL\_TYPE verwenden. Beispiel:  
  
```  
array(PDO::ATTR_CURSOR => PDO::CURSOR_SCROLL, PDO::SQLSRV_ATTR_CURSOR_SCROLL_TYPE => PDO::SQLSRV_CURSOR_DYNAMIC));  
```  
  
Die folgende Tabelle enthält die möglichen Werte für PDO::SQLSRV\_ATTR\_CURSOR\_SCROLL\_TYPE.  
  
|Wert|Beschreibung|  
|---------|---------------|  
|PDO::SQLSRV\_CURSOR\_BUFFERED|Erstellt einen clientseitigen statischen Cursor \(gepuffert\). Weitere Informationen zu clientseitigen Cursorn finden Sie unter [Cursortypen &#40;PDO_SQLSRV-Treiber&#41;](../Topic/Cursor%20Types%20(PDO_SQLSRV%20Driver).md).|  
|PDO::SQLSRV\_CURSOR\_DYNAMIC|Erstellt einen serverseitigen \(ungepufferten\) dynamischen Cursor, der es Ihnen erlaubt, auf Zeilen in beliebiger Reihenfolge zuzugreifen und Änderungen in der Datenbank widerspiegelt.|  
|PDO::SQLSRV\_CURSOR\_KEYSET\_DRIVEN|Erstellt einen serverseitigen Keysetcursor. Ein Keysetcursor aktualisiert nach dem Löschen einer Zeile aus einer Tabelle nicht die Zeilenanzahl \(eine gelöschte Zeile wird ohne Werte zurückgegeben\).|  
|PDO::SQLSRV\_CURSOR\_STATIC|Erstellt einen serverseitigen statischen Cursor, der es Ihnen zwar erlaubt, auf Zeilen in beliebiger Reihenfolge zuzugreifen, aber die Änderungen in der Datenbank nicht widerspiegelt.<br /><br />PDO::ATTR\_CURSOR \=> PDO::CURSOR\_SCROLL impliziert PDO::SQLSRV\_ATTR\_CURSOR\_SCROLL\_TYPE \=> PDO::SQLSRV\_CURSOR\_STATIC.|  
  
Sie können ein PDOStatement-Objekt schließen, indem Sie dafür den Wert NULL festlegen.  
  
## Beispiel  
In diesem Beispiel wird erläutert, wie Sie die Methode „PDO::prepare“ mit Parametermarkern und einem Vorwärtscursor verwenden.  
  
```  
<?php  
$database = "Test";  
$server = "(local)";  
$conn = new PDO( "sqlsrv:server=$server ; Database = $database", "", "");  
  
$col1 = 'a';  
$col2 = 'b';  
  
$query = "insert into Table1(col1, col2) values(?, ?)";  
$stmt = $conn->prepare( $query, array( PDO::ATTR_CURSOR => PDO::CURSOR_FWDONLY, PDO::SQLSRV_ATTR_QUERY_TIMEOUT => 1  ) );  
$stmt->execute( array( $col1, $col2 ) );  
print $stmt->rowCount();  
echo "\n";  
  
$query = "insert into Table1(col1, col2) values(:col1, :col2)";  
$stmt = $conn->prepare( $query, array( PDO::ATTR_CURSOR => PDO::CURSOR_FWDONLY, PDO::SQLSRV_ATTR_QUERY_TIMEOUT => 1  ) );  
$stmt->execute( array( ':col1' => $col1, ':col2' => $col2 ) );  
print $stmt->rowCount();  
  
$stmt = null  
?>  
```  
  
## Beispiel  
In diesem Beispiel wird veranschaulicht, wie Sie die PDO::prepare-Methode mit einem clientseitigen Cursor verwenden. Ein Beispiel für einen serverseitigen Cursor finden Sie unter [Cursortypen &#40;PDO_SQLSRV-Treiber&#41;](../Topic/Cursor%20Types%20(PDO_SQLSRV%20Driver).md).  
  
```  
<?php  
$database = "AdventureWorks";  
$server = "(local)";  
$conn = new PDO( "sqlsrv:server=$server ; Database = $database", "", "");  
  
$query = "select * from Person.ContactType";  
$stmt = $conn->prepare( $query, array(PDO::ATTR_CURSOR => PDO::CURSOR_SCROLL));  
$stmt->execute();  
  
echo "\n";  
  
while ( $row = $stmt->fetch( PDO::FETCH_ASSOC ) ){  
   print "$row[Name]\n";  
}  
echo "\n..\n";  
  
$row = $stmt->fetch( PDO::FETCH_BOTH, PDO::FETCH_ORI_FIRST );  
print_r($row);  
  
$row = $stmt->fetch( PDO::FETCH_ASSOC, PDO::FETCH_ORI_REL, 1 );  
print "$row[Name]\n";  
  
$row = $stmt->fetch( PDO::FETCH_NUM, PDO::FETCH_ORI_NEXT );  
print "$row[1]\n";  
  
$row = $stmt->fetch( PDO::FETCH_NUM, PDO::FETCH_ORI_PRIOR );  
print "$row[1]..\n";  
  
$row = $stmt->fetch( PDO::FETCH_NUM, PDO::FETCH_ORI_ABS, 0 );  
print_r($row);  
  
$row = $stmt->fetch( PDO::FETCH_NUM, PDO::FETCH_ORI_LAST );  
print_r($row);  
?>  
```  
  
## Siehe auch  
[PDO-Klasse](../content/PDO-Class.md)  
[PDO](http://go.microsoft.com/fwlink/?LinkID=187441)  
  
