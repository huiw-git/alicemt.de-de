---
title: "PDO::quote"
ms.custom: na
ms.date: 06/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ab9ddc48-42f8-4edf-aa8b-b0fc66706161
caps.latest.revision: 9
caps.handback.revision: 8
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
# PDO::quote
Verarbeitet eine Zeichenfolge für die Verwendung in einer Abfrage, indem die Eingabezeichenfolge gemäß der zugrunde liegenden SQL Server-Datenbank in Anführungszeichen gesetzt wird. PDO::quote umgeht Sonderzeichen in der Eingabezeichenfolge unter Verwendung eines für den SQL Server geeigneten Zitierstils.  
  
## Syntax  
  
```  
  
string PDO::quote( $string[, $parameter_type ] )  
```  
  
#### Parameter  
$*string*: Die zu zitierende Zeichenfolge.  
  
$*parameter\_type*: Ein optionales \(Ganzzahl\)symbol, das den Datentyp angibt.  Der Standardwert ist PDO::PARAM\_STR.  
  
## Rückgabewert  
Eine Zeichenfolge in Anführungszeichen, die an eine SQL-Anweisung oder bei einem Fehler an false übergeben werden kann.  
  
## Hinweise  
Unterstützung für PDO wurde in Version 2.0 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt.  
  
## Beispiel  
  
```  
<?php  
$database = "test";  
$server = "(local)";  
$conn = new PDO( "sqlsrv:server=$server ; Database = $database", "", "");  
  
$param = 'a \' g';  
$param2 = $conn->quote( $param );  
  
$query = "INSERT INTO Table1 VALUES( ?, '1' )";  
$stmt = $conn->prepare( $query );  
$stmt->execute(array($param));  
  
$query = "INSERT INTO Table1 VALUES( ?, ? )";  
$stmt = $conn->prepare( $query );  
$stmt->execute(array($param, $param2));  
?>  
```  
  
## Siehe auch  
[PDO-Klasse](../content/PDO-Class.md)  
[PDO](http://go.microsoft.com/fwlink/?LinkID=187441)  
  
