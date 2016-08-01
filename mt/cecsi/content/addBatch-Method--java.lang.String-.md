---
title: "addBatch-Methode (java.lang.String)"
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
  - SQLServerPreparedStatement.addBatch (java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 093f6c3b-49a6-4043-9993-bd0482de04dd
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
# addBatch-Methode (java.lang.String)
    
## addBatch\-Methode \(java.lang.String\)  
 Fügt den angegebenen SQL\-Befehl der aktuellen Liste mit Befehlen für dieses [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\-Objekt hinzu.  
  
## Syntax  
  
```  
  
public void addBatch(java.lang.String sql)  
```  
  
#### Parameter  
 *sql*  
  
 Ein **String** mit einer SQL\-Anweisung.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese addBatch\-Methode wird von der addBatch\-Methode in der java.sql.Statement\-Schnittstelle angegeben.  
  
 Durch den Aufruf dieser Methode wird eine Ausnahme ausgelöst, da die SQL\-Anweisung für das SQLServerPreparedStatement\-Objekt bei der Erstellung des Objekts angegeben wird.  
  
## Siehe auch  
 [addBatch-Methode &#40;ISQLServerPreparedStatement&#41;](../content/addBatch-Method--SQLServerPreparedStatement-.md)   
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)   
 [SQLServerPreparedStatement-Klasse](../content/SQLServerPreparedStatement-Class.md)  
  
  