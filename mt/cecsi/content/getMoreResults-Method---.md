---
title: "getMoreResults-Methode ()"
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
  - SQLServerStatement.getMoreResults ()
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: df89db50-0b2f-4094-820a-30be25ad72fe
caps.latest.revision: 8
caps.handback.revision: 8
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
# getMoreResults-Methode ()
    
## getMoreResults\-Methode \(\)  
 Wechselt zum nächsten Ergebnis dieses [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekts.  
  
## Syntax  
  
```  
  
public final boolean getMoreResults()  
```  
  
## Rückgabewert  
 **true**, wenn es sich beim zurückgegebenen Ergebnis um ein Resultset handelt. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getMoreResults\-Methode wird von der getMoreResults\-Methode in der java.sql.Statement\-Schnittstelle angegeben.  
  
 Durch den Aufruf der getMoreResults\-Methode werden alle momentan geöffneten Resultsetobjekte geschlossen, die mit der [getResultSet](../content/getResultSet-Method--SQLServerStatement-.md)\-Methode abgerufen werden.  
  
## Siehe auch  
 [getMoreResults-Methode &#40;ISQLServerStatement&#41;](../content/getMoreResults-Method--SQLServerStatement-.md)   
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  