---
title: "PDO::rollback"
ms.custom: na
ms.date: 06/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d918c1e3-1be0-4001-b3b0-000db6d9e8b8
caps.latest.revision: 8
caps.handback.revision: 7
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
# PDO::rollback
Verwirft Datenbankbefehle, die nach dem Aufrufen von [PDO::beginTransaction](../Topic/PDO::beginTransaction.md) ausgegeben wurden, und setzt die Verbindung in den Autocommit-Modus zurück.  
  
## Syntax  
  
```  
  
bool PDO::rollBack ();  
```  
  
## Rückgabewert  
„true“, bei erfolgreichem Aufruf der Methode; andernfalls „false“.  
  
## Hinweise  
PDO::rollback ist nicht betroffen von \(und hat keinen Einfluss auf\) den Wert von PDO::ATTR\_AUTOCOMMIT.  
  
Unter [PDO::beginTransaction](../Topic/PDO::beginTransaction.md) finden Sie ein Beispiel, das PDO::rollback verwendet.  
  
Unterstützung für PDO wurde in Version 2.0 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt.  
  
## Siehe auch  
[PDO-Klasse](../content/PDO-Class.md)  
[PDO](http://go.microsoft.com/fwlink/?LinkID=187441)  
  
