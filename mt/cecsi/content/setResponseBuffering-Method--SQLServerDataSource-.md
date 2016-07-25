---
title: "setResponseBuffering-Methode (SQLServerDataSource)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLServerDataSource.setResponseBuffering(String responseBufferingValue)
apilocation: 
  - SQLServerDataSource.setResponseBuffering(String responseBufferingValue)
apitype: Assembly
ms.assetid: c9e43ff2-8117-4dca-982d-83c863d0c8e1
caps.latest.revision: 27
caps.handback.revision: 26
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
# setResponseBuffering-Methode (SQLServerDataSource)
  Legt den Antwortpuffermodus für Verbindungen fest, die unter Verwendung dieses [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Objekts erstellt werden.  
  
## Syntax  
  
```  
  
public void setResponseBuffering(java.lang.String value)  
```  
  
#### Parameter  
 *value*  
  
 Ein **String** mit dem Puffer\- und Streamingmodus. Gültige Modi \(jeweils ohne Berücksichtigung der Groß\-\/Kleinschreibung\): **full** oder **adaptive**.  
  
## Hinweise  
 Der Wert **full** gibt an, dass zur Laufzeit das gesamte Ergebnis vom Server gelesen wird.  
  
 Der Wert **adaptive** gibt an, dass im Bedarfsfall die geringstmögliche Menge an Daten gepuffert wird. Der **adaptive**\-Wert ist der Standardpuffermodus.  
  
 Weitere Informationen zum Verwenden des Antwortpuffermodus finden Sie unter [Verwenden der adaptiven Pufferung](../content/Using-Adaptive-Buffering.md).  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  