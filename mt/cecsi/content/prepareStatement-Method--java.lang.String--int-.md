---
title: "prepareStatement-Methode (java.lang.String, int)"
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
  - SQLServerConnection.prepareStatement (java.lang.String, int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 4504cd55-81fd-4783-bcb0-1efb1938fdd5
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
    
## prepareStatement\-Methode \(java.lang.String, int\)  
 Erstellt ein [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\-Objekt zum Senden parametrisierter SQL\-Anweisungen an die Datenbank und bietet die Möglichkeit zum Abrufen automatisch erstellter Schlüssel.  
  
## Syntax  
  
```  
  
public java.sql.PreparedStatement prepareStatement(java.lang.String sql,  
                                                   int flag)  
```  
  
#### Parameter  
 *sql*  
  
 Ein **String** mit einer SQL\-Anweisung.  
  
 *flag*  
  
 Ein Wert vom Typ **int** zum Angeben, ob automatisch generierte Schlüssel verfügbar sind.  
  
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
  
  