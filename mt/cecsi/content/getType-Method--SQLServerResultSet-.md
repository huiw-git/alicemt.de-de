---
title: "getType-Methode (ISQLServerResultSet)"
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
  - SQLServerResultSet.getType
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: ffbc4a02-e851-431c-bc1a-7ab381d982bb
caps.latest.revision: 9
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
# getType-Methode (ISQLServerResultSet)
    
## getType\-Methode \(ISQLServerResultSet\)  
 Ruft den Cursortyp dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts ab.  
  
## Syntax  
  
```  
  
public int getType()  
```  
  
## Rückgabewert  
 Ein Wert vom Typ **int**  zum Angeben des aktuellen Cursortyps. Mögliche Werte:  
  
 ResultSet.TYPE\_FORWARD\_ONLY  
  
 ResultSet.TYPE\_SCROLL\_INSENSITIVE  
  
 ResultSet.TYPE\_SCROLL\_SENSITIVE  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getType\-Methode wird von der getType\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Diese Methode kann zur Bestimmung des eigentlichen Cursortyps verwendet werden. Wurde von der Anwendung "TYPE\_FORWARD\_ONLY" ausgewählt oder ein standardmäßiger Cursortyp verwendet, wird "TYPE\_FORWARD\_ONLY" zurückgegeben.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  