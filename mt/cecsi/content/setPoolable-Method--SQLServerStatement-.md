---
title: "setPoolable-Methode (ISQLServerStatement)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f0f798c8-cafb-4acc-b85d-2e0059c91d92
caps.latest.revision: 5
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
# setPoolable-Methode (ISQLServerStatement)
    
## setPoolable\-Methode \(ISQLServerStatement\)  
 Sendet eine Anforderung, dass dem Pool eine Anweisung hinzugefügt bzw. nicht hinzugefügt werden soll.  
  
## Syntax  
  
```  
  
public void setPoolable(boolean poolable) throws SQLException  
```  
  
#### Parameter  
 *poolable*  
  
 Wenn **true**, wird angefordert, dass dem Pool die Anweisung hinzugefügt werden soll. Wenn **false**, wird angefordert, dass dem Pool die Anweisung nicht hinzugefügt werden soll.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Der im *poolable*\-Parameter angegebene Wert zeigt an, ob die Anweisung dem Pool hinzugefügt werden soll. Vom Anweisungspoolmanager wird entschieden, ob dieser Hinweis verwendet wird.  
  
 Der Poolwert einer Anwendung gilt für vom Treiber implementierte interne Anweisungscaches und externe von Anwendungsservern oder anderen Anwendungen implementierte Anweisungscaches.  
  
 Ein SQLServerStatement\-Objekt kann nach der Erstellung dem Pool standardmäßig nicht hinzugefügt werden. SQLServerPreparedStatement\- und SQLServerCallableStatement\-Objekte können nach der Erstellung dem Pool hinzugefügt werden.  
  
 [SQLServerException](../content/SQLServerException-Class.md) wird ausgelöst, wenn diese Methode für eine geschlossene Anweisung aufgerufen wird.  
  
 Von [isPoolable](../content/isPoolable-Method--SQLServerStatement-.md) wird ein Wert zurückgegeben, der anzeigt, ob das Objekt dem Pool hinzugefügt werden kann.  
  
## Siehe auch  
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  