---
title: "getResponseBuffering-Methode (SQLServerDataSource)"
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
  - SQLServerDataSource.getResponseBuffering()
apilocation: 
  - SQLServerDataSource.getResponseBuffering()
apitype: Assembly
ms.assetid: 19585a93-88a4-415e-a20e-12ba58cddeaa
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
# getResponseBuffering-Methode (SQLServerDataSource)
    
## getResponseBuffering\-Methode \(SQLServerDataSource\)  
 Gibt den Antwortpuffermodus für dieses [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Objekt zurück.  
  
## Syntax  
  
```  
  
public java.lang.String getResponseBuffering()  
```  
  
## Rückgabewert  
 Ein **String** mit **full** oder **adaptive** in Kleinbuchstaben.  
  
## Hinweise  
 Der Wert **full** gibt an, dass zur Laufzeit das gesamte Ergebnis vom Server gelesen wird.  
  
 Der Wert **adaptive** gibt an, dass im Bedarfsfall die geringstmögliche Menge an Daten gepuffert wird. Der **adaptive**\-Wert ist der Standardpuffermodus.  
  
 Weitere Informationen zum Verwenden des Antwortpuffermodus finden Sie unter [Verwenden der adaptiven Pufferung](../content/Using-Adaptive-Buffering.md).  
  
## Siehe auch  
 [setResponseBuffering-Methode &#40;SQLServerDataSource&#41;](../content/setResponseBuffering-Method--SQLServerDataSource-.md)   
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  