---
title: "isPoolable-Methode (ISQLServerStatement)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b8a12ac5-57cb-4288-9973-c7d5cebd197c
caps.latest.revision: 6
caps.handback.revision: 5
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
  - sv-se
  - zh-cn
  - zh-tw
---
# isPoolable-Methode (ISQLServerStatement)
    
## isPoolable\-Methode \(ISQLServerStatement\)  
 Gibt einen Wert zurück, durch den angegeben wird, ob dem vom Benutzer bereitgestellten Anwendungspool eine Anweisung hinzugefügt werden kann.  
  
## Syntax  
  
```  
  
public boolean isPoolable() throws SQLException  
```  
  
## Rückgabewert  
 **true**, wenn die Anweisung dem vom Benutzer bereitgestellten Anwendungspool hinzugefügt werden kann. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Mit [setPoolable](../content/setPoolable-Method--SQLServerStatement-.md) wird für ein Objekt das Verhalten beim Hinzufügen zu Pools geändert.  
  
## Siehe auch  
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  