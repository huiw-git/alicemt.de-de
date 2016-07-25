---
title: "setResponseBuffering-Methode (ISQLServerStatement)"
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
  - SQLServerStatement.setResponseBuffering(String responseBufferingValue)
apilocation: 
  - SQLServerStatement.setResponseBuffering(String responseBufferingValue)
apitype: Assembly
ms.assetid: 9f489835-6cda-4c8c-b139-079639a169cf
caps.latest.revision: 24
caps.handback.revision: 23
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
# setResponseBuffering-Methode (ISQLServerStatement)
    
## setResponseBuffering\-Methode \(ISQLServerStatement\)  
 Legt den Antwortpuffermodus für dieses [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt auf **String full** oder auf **adaptive** \(jeweils ohne Berücksichtigung der Groß\-\/Kleinschreibung\) fest.  
  
## Syntax  
  
```  
  
public final void setResponseBuffering(java.lang.String value)  
```  
  
#### Parameter  
 *value*  
  
 Ein **String** mit dem Antwortpuffermodus. Gültige Modi \(jeweils ohne Berücksichtigung der Groß\-\/Kleinschreibung\): **full** oder **adaptive**.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 **adaptive** gibt an, dass im Bedarfsfall die geringstmögliche Menge an Daten gepuffert wird.  
  
 **full** gibt an, dass zur Laufzeit das gesamte Ergebnis vom Server gelesen wird.  
  
 "adaptive" ist der Standardwert in JDBC Driver, Version 2.0 und 3.0. "full" war der Standardwert in Versionen vor JDBC Driver, Version 2.0.  
  
 Mithilfe der [setResponseBuffering](../content/setResponseBuffering-Method--SQLServerStatement-.md)\-Methode kann die **responseBuffering**\-Verbindungseigenschaft vom Typ **String** für das aktuelle [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt überschrieben werden. Weitere Informationen zum Verwenden des Antwortpuffermodus finden Sie unter [Verwenden der adaptiven Pufferung](../content/Using-Adaptive-Buffering.md).  
  
 Wird von der Anwendung ein ungültiger Parameterwert für die [setResponseBuffering](../content/setResponseBuffering-Method--SQLServerStatement-.md)\-Methode angegeben, wird ein Fehler vom Typ [SQLServerException](../content/SQLServerException-Class.md) ausgelöst.  
  
## Siehe auch  
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)   
 [Verwenden der adaptiven Pufferung](../content/Using-Adaptive-Buffering.md)  
  
  