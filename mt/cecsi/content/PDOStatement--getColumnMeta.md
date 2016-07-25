---
title: "PDOStatement::getColumnMeta"
ms.custom: na
ms.date: 06/16/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c92a21cc-8e53-43d0-a4bf-542c77c100c9
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
# PDOStatement::getColumnMeta
Ruft die Metadaten für eine Spalte ab.  
  
## Syntax  
  
```  
  
array PDOStatement::getColumnMeta ( $column );  
```  
  
#### Parameter  
*$conn*: \(Ganze Zahl\) Die nullbasierte Nummer der Spalte, deren Metadaten Sie abrufen wollen.  
  
## Rückgabewert  
Ein assoziatives Array \(Schlüssel und Wert\), das die Metadaten für die Spalte enthält. Im Abschnitt „Anmerkungen“ finden Sie eine Beschreibung für die Felder im Array.  
  
## Hinweise  
Die folgende Tabelle beschreibt die Felder im durch „getColumnMeta“ zurückgegebenen Array.  
  
|NAME|VALUES|  
|--------|----------|  
|native\_type|Gibt den PHP-Typ der Spalte an Immer Zeichenfolge.|  
|driver:decl\_type|Gibt den SQL-Typ an, der verwendet wird, um den Spaltenwert in der Datenbank darzustellen Falls die Spalte im Resultset das Ergebnis einer Funktion ist, wird dieser Wert nicht von PDOStatement::getColumnMeta zurückgegeben.|  
|flags|Gibt die Flags (Kennzeichnungen), die für diese Spalte eingerichtet wurden, an Immer 0.|  
|name|Gibt den Namen der Spalte in der Datenbank an|  
|table|Gibt den Namen derjenigen Tabelle in der Datenbank an, welche die Spalte enthält Immer leer.|  
|Länge|Gibt die Länge der Spalte an|  
|precision|Gibt die numerische Genauigkeit dieser Spalte an|  
|pdo\_type|Gibt den Typ dieser Spalte an, wie durch die PDO::PARAM\_\*-Konstanten widergespiegelt. Immer PDO::PARAM\_STR \(2\).|  
  
Unterstützung für PDO wurde in Version 2.0 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt.  
  
## Beispiel  
  
```  
<?php  
$database = "AdventureWorks";  
$server = "(local)";  
$conn = new PDO( "sqlsrv:server=$server ; Database = $database", "", "");  
  
$stmt = $conn->query("select * from Person.ContactType");  
$metadata = $stmt->getColumnMeta(2);  
var_dump($metadata);  
  
print $metadata['sqlsrv:decl_type'] . "\n";  
print $metadata['native_type'] . "\n";  
print $metadata['name'];  
?>  
```  
  
## Siehe auch  
[PDOStatement-Klasse](../content/PDOStatement-Class.md)  
[PDO](http://go.microsoft.com/fwlink/?LinkID=187441)  
  
