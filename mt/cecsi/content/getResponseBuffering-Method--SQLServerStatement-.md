---
title: "getResponseBuffering-Methode (ISQLServerStatement)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLServerStatement.getResponseBuffering()
apilocation: 
  - SQLServerStatement.getResponseBuffering()
apitype: Assembly
ms.assetid: a9a9ffdd-7ce3-4e0a-907c-34d6a54e6865
caps.latest.revision: 23
caps.handback.revision: 22
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
# getResponseBuffering-Methode (ISQLServerStatement)
    
## getResponseBuffering\-Methode \(ISQLServerStatement\)  
 Ruft den Antwortpuffermodus für dieses [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt ab.  
  
## Syntax  
  
```  
  
public final java.lang.String getResponseBuffering()  
```  
  
## Rückgabewert  
 Ein **String** mit **full** oder **adaptive** in Kleinbuchstaben.  
  
## Hinweise  
 **adaptive** gibt an, dass im Bedarfsfall die geringstmögliche Menge an Daten gepuffert wird.  
  
 **full** gibt an, dass zur Laufzeit das gesamte Ergebnis vom Server gelesen wird.  
  
 **adaptive** ist der Standardwert in JDBC Driver, Version 2.0 und 3.0. **full** war der Standardwert in Versionen vor JDBC Driver, Version 2.0.  
  
 Weitere Informationen zum Verwenden des Antwortpuffermodus finden Sie unter [Verwenden der adaptiven Pufferung](../content/Using-Adaptive-Buffering.md).  
  
## Siehe auch  
 [setResponseBuffering-Methode &#40;ISQLServerStatement&#41;](../content/setResponseBuffering-Method--SQLServerStatement-.md)   
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  