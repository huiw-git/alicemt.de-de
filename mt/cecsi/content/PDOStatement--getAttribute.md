---
title: "PDOStatement::getAttribute"
ms.custom: na
ms.date: 07/18/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 41d0cca3-8556-4573-bb90-8e9402d9379f
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
# PDOStatement::getAttribute
Ruft den Wert eines vordefinierten PDOStatement-Attributs oder ein benutzerdefiniertes Treiber-Attributs ab.  
  
## Syntax  
  
```  
  
mixed PDOStatement::getAttribute( $attribute );  
```  
  
#### Parameter  
$*attribute*: Eine ganze Zahl, eine der Konstanten PDO::ATTR\_\* oder PDO::SQLSRV\_ATTR\_\*-Konstanten. Unterstützte Attribute sind die Attribute, die mithilfe von [PDOStatement::setAttribute](../Topic/PDOStatement::setAttribute.md) festgelegt werden können, PDO::SQLSRV\_ATTR\_DIRECT\_QUERY, \(in [Direkte Anweisungsausführung und vorbereitete Anweisungsausführung im PDO_SQLSRV-Treiber](../Topic/Direct%20Statement%20Execution%20and%20Prepared%20Statement%20Execution%20in%20the%20PDO_SQLSRV%20Driver.md) finden Sie weitere Informationen zu PDO::SQLSRV\_ATTR\_DIRECT\_QUERY\) und PDO::ATTR\_CURSOR.  
  
## Rückgabewert  
Bei Erfolg wird ein \(gemischter\) Wert für ein vordefiniertes PDO-Attribut oder ein benutzerdefiniertes Treiber-Attribut zurückgegeben. Gibt bei einem Fehler NULL zurück.  
  
## Hinweise  
Ein Beispiel hierzu finden Sie unter [PDOStatement::setAttribute](../Topic/PDOStatement::setAttribute.md) .  
  
Unterstützung für PDO wurde in Version 2.0 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt.  
  
## Siehe auch  
[PDOStatement-Klasse](../content/PDOStatement-Class.md)  
[PDO](http://go.microsoft.com/fwlink/?LinkID=187441)  
  
