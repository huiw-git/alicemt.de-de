---
title: "PDOStatement::bindParam"
ms.custom: na
ms.date: 06/16/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 65212058-2632-47a4-ba7d-2206883abf09
caps.latest.revision: 17
caps.handback.revision: 16
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
# PDOStatement::bindParam
Bindet einen Parameter an einen benannten Platzhalter oder Fragezeichenplatzhalter in der SQL-Anweisung.  
  
## Syntax  
  
```  
  
bool PDOStatement::bindParam( $parameter, &$variable [,$data_type[, $length[, $driver_options]]] );  
```  
  
#### Parameter  
$*parameter*: Ein \(gemischter\) Parameterbezeichner. Ein Parametername \(:name\) für eine Anweisung, die benannte Platzhalter verwendet. Für eine vorbereitete Anweisung mit der Fragezeichensyntax stellt dieser den 1\-basierten Index des Parameters dar.  
  
&$*variable*: Der \(gemischte\) Name der PHP-Variablen, die an den SQL-Anweisungsparameter gebunden werden soll.  
  
$*data\_type*: Eine optionale \(Integer\) PDO::PARAM\_\*-Konstante. Der Standardwert ist PDO::PARAM\_STR.  
  
$*length*: Eine optionale \(Integer\) Länge des Datentyps. Sie können PDO::SQLSRV\_PARAM\_OUT\_DEFAULT\_SIZE bestimmen, um die Standardgröße anzugeben, wenn Sie PDO::PARAM\_INT oder PDO::PARAM\_BOOL in $*data\_type* verwenden.  
  
$*driver\_options*: Die optionalen \(gemischten\) treiberspezifischen Optionen. Beispielsweise können Sie PDO::SQLSRV\_ENCODING\_UTF8 angeben, um die Spalte an eine Variable als UTF\-8-codierte Zeichenfolge zu binden.  
  
## Rückgabewert  
„true“ bei Erfolg, andernfalls „false“.  
  
## Hinweise  
Beim Binden von NULL-Daten an Serverspalten vom Typ varbinary, binary oder varbinary\(max\) sollten Sie die binäre Codierung \(PDO::SQLSRV\_ENCODING\_BINARY\) unter Verwendung der $*driver\_options* angeben. Weitere Informationen über Codierungskonstanten finden Sie unter [Konstanten](../content/Constants--Microsoft-Drivers-for-PHP-for-SQL-Server-.md).  
  
Unterstützung für PDO wurde in Version 2.0 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt.  
  
## Beispiel  
Dieses Codebeispiel zeigt, dass, nachdem $contact an den Parameter gebunden wurde, das Ändern des Werts nicht den in der Abfrage übergebenen Wert ändert.  
  
```  
<?php  
$database = "AdventureWorks";  
$server = "(local)";  
$conn = new PDO( "sqlsrv:server=$server ; Database = $database", "", "");  
  
$contact = "Sales Agent";  
$stmt = $conn->prepare("select * from Person.ContactType where name = ?");  
$stmt->bindParam(1, $contact);  
$contact = "Owner";  
$stmt->execute();  
  
while ( $row = $stmt->fetch( PDO::FETCH_ASSOC ) ){  
   print "$row[Name]\n\n";  
}  
  
$stmt = null;  
$contact = "Sales Agent";  
$stmt = $conn->prepare("select * from Person.ContactType where name = :contact");  
$stmt->bindParam(':contact', $contact);  
$contact = "Owner";  
$stmt->execute();  
  
while ( $row = $stmt->fetch( PDO::FETCH_ASSOC ) ){  
   print "$row[Name]\n\n";  
}  
?>  
```  
  
## Beispiel  
In diesem Codebeispiel wird veranschaulicht, wie auf einen Output-Parameter zugegriffen wird.  
  
```  
<?php  
$database = "Test";  
$server = "(local)";  
$conn = new PDO( "sqlsrv:server=$server ; Database = $database", "", "");  
  
$input1 = 'bb';  
  
$stmt = $conn->prepare("select ? = count(* ) from Sys.tables");  
$stmt->bindParam( 1, $input1, PDO::PARAM_STR, 10 );  
$stmt->execute();  
echo $input1;  
?>  
```  
  
## Beispiel  
In diesem Codebeispiel wird veranschaulicht, wie ein Input\/Output-Parameter verwendet wird.  
  
```  
<?php  
   $database = "AdventureWorks";  
   $server = "(local)";  
   $dbh = new PDO( "sqlsrv:server=$server ; Database = $database", "", "");  
  
   $dbh->query("IF OBJECT_ID('dbo.sp_ReverseString', 'P') IS NOT NULL DROP PROCEDURE dbo.sp_ReverseString");  
   $dbh->query("CREATE PROCEDURE dbo.sp_ReverseString @String as VARCHAR(2048) OUTPUT as SELECT @String = REVERSE(@String)");  
   $stmt = $dbh->prepare("EXEC dbo.sp_ReverseString ?");  
   $string = "123456789";  
   $stmt->bindParam(1, $string, PDO::PARAM_STR | PDO::PARAM_INPUT_OUTPUT, 2048);  
   $stmt->execute();  
   print $string;   // Expect 987654321  
?>  
```  
  
## Siehe auch  
[PDOStatement-Klasse](../content/PDOStatement-Class.md)  
[PDO](http://go.microsoft.com/fwlink/?LinkID=187441)  
  
