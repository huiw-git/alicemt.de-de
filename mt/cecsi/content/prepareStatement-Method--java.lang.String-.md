---
title: "prepareStatement-Methode (java.lang.String)"
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
  - SQLServerConnection.prepareStatement (java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: e825765c-eb55-4800-951b-f3495da36641
caps.latest.revision: 9
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
# prepareStatement-Methode (java.lang.String)
    
## prepareStatement\-Methode \(java.lang.String\)  
 Erstellt ein [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\-Objekt zum Senden von parametrisierten SQL\-Anweisungen an die Datenbank.  
  
## Syntax  
  
```  
  
public java.sql.PreparedStatement prepareStatement(java.lang.String sql)  
```  
  
#### Parameter  
 *sql*  
  
 Ein **String** mit einer SQL\-Anweisung.  
  
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
  
  