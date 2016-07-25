---
title: "PDO::commit"
ms.custom: na
ms.date: 06/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a0db4a00-9700-4f49-ab16-6522dd1101d3
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
# PDO::commit
Sendet Befehle an die Datenbank, die nach dem Aufruf von [PDO::beginTransaction](../Topic/PDO::beginTransaction.md) ausgegeben wurden und setzt die Verbindung in den Autocommit-Modus zurück.  
  
## Syntax  
  
```  
  
bool PDO::commit();  
```  
  
## Rückgabewert  
„true“, bei erfolgreichem Aufruf der Methode; andernfalls „false“.  
  
## Hinweise  
PDO::commit ist nicht betroffen von dem Wert des PDO::ATTR\_AUTOCOMMIT \(und hat keinen Einfluss auf diesen\).  
  
Ein Beispiel, das PDO::commit verwendet, finden Sie unter [PDO::beginTransaction](../Topic/PDO::beginTransaction.md) .  
  
Unterstützung für PDO wurde in Version 2.0 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt.  
  
## Siehe auch  
[PDO-Klasse](../content/PDO-Class.md)  
[PDO](http://go.microsoft.com/fwlink/?LinkID=187441)  
  
