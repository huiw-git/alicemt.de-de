---
title: "getFetchDirection-Methode (ISQLServerResultSet)"
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
  - SQLServerResultSet.getFetchDirection
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 5ab385c2-e18c-4b75-ac2d-2402af5c52a5
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
  - sv-se
  - zh-cn
  - zh-tw
---
# getFetchDirection-Methode (ISQLServerResultSet)
    
## getFetchDirection\-Methode \(ISQLServerResultSet\)  
 Ruft die Abrufrichtung für dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt ab.  
  
## Syntax  
  
```  
  
public int getFetchDirection()  
```  
  
## Rückgabewert  
 Ein Wert vom Typ **int** zum Angeben der aktuellen Abrufrichtung.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getFetchDirection\-Methode wird von der getFetchDirection\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Von dieser Methode wird FETCH\_FORWARD für schreibgeschützte Vorwärtscursor zurückgegeben, die letzte Einstellung, die durch einen Aufruf der [setFetchDirection](../content/setFetchDirection-Method--SQLServerResultSet-.md)\-Methode für andere Cursortypen vorgenommen wurde. Wenn die setFetchDirection\-Methode niemals aufgerufen wurde, wird für diese Cursortypen FETCH\_UNKNOWN zurückgegeben.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  