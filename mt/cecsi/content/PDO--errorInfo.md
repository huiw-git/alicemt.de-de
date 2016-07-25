---
title: "PDO::errorInfo"
ms.custom: na
ms.date: 06/16/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9d5481d5-13bc-4388-b3aa-78676c0fc709
caps.latest.revision: 11
caps.handback.revision: 10
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
# PDO::errorInfo
Ruft erweiterte Fehlerinformationen des zuletzt ausgeführten Vorgangs des Datenbankhandles ab.  
  
## Syntax  
  
```  
  
array PDO::errorInfo();  
```  
  
## Rückgabewert  
Ein Array mit Fehlerinformationen über den zuletzt ausgeführten Vorgang des Datenbankhandles. Dieses Array besteht aus den folgenden Feldern:  
  
-   Der SQLSTATE-Fehlercode  
  
-   Der treiberspezifische Fehlercode  
  
-   Die treiberspezifische Fehlermeldung  
  
Wenn kein Fehler vorliegt oder wenn der SQLSTATE nicht festgelegt ist, sind die treiberspezifischen Felder NULL.  
  
## Hinweise  
PDO::errorInfo ruft nur die Fehlerinformationen für Vorgänge ab, die direkt in der Datenbank ausgeführt werden. Verwenden Sie PDOStatement::errorInfo, wenn eine PDOStatement-Instanz mit PDO::prepare oder PDO::query erstellt wird.  
  
Unterstützung für PDO wurde in Version 2.0 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt.  
  
## Beispiel  
In diesem Beispiel ist der Name der Spalte falsch geschrieben \(`Cityx` anstelle von `City`\) und verursacht einen Fehler, der dann gemeldet wird.  
  
```  
<?php  
$conn = new PDO( "sqlsrv:server=(local) ; Database = AdventureWorks ", "");  
$query = "SELECT * FROM Person.Address where Cityx = 'Essen'";  
  
$conn->query($query);  
print $conn->errorCode();  
echo "\n";  
print_r ($conn->errorInfo());  
?>  
```  
  
## Siehe auch  
[PDO-Klasse](../content/PDO-Class.md)  
[PDO](http://go.microsoft.com/fwlink/?LinkID=187441)  
  
