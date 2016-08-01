---
title: "prepareStatement-Methode (java.lang.String, int)"
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
  - SQLServerConnection.prepareStatement (java.lang.String, int[])
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 72b5c4a5-1382-4b2c-80a0-47c97c5f52d3
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
# prepareStatement-Methode (java.lang.String, int)
    
## prepareStatement\-Methode \(java.lang.String, int\[\]\)  
 Erstellt ein [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\-Objekt zum Senden parametrisierter SQL\-Anweisungen an die Datenbank und bietet die Möglichkeit zum Abrufen automatisch erstellter Schlüssel, die vom angegebenen Array festgelegt werden.  
  
## Syntax  
  
```  
  
public java.sql.PreparedStatement prepareStatement(java.lang.String sql,  
                                                   int[] columnIndexes)  
```  
  
#### Parameter  
 *sql*  
  
 Ein **String** mit einer SQL\-Anweisung.  
  
 *columnIndexes*  
  
 Ein Array von int\-Elementen.  
  
## Rückgabewert  
 Ein PreparedStatement\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese prepareStatement\-Methode wird von der prepareStatement\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
## Siehe auch  
 [prepareStatement-Methode &#40;ISQLServerConnection&#41;](../content/prepareStatement-Method--SQLServerConnection-.md)   
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  