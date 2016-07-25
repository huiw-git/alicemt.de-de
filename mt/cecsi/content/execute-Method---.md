---
title: "execute-Methode ()"
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
  - SQLServerPreparedStatement.execute ()
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: fa96d0f8-101b-422f-a767-405be9a5f74f
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
# execute-Methode ()
    
## execute\-Methode \(\)  
 Führt die SQL\-Anweisung in diesem [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\-Objekt aus. Hierbei kann es sich um eine beliebige Art von SQL\-Anweisung handeln.  
  
## Syntax  
  
```  
  
public boolean execute()  
```  
  
## Rückgabewert  
 **true**, wenn von der Anweisung ein Resultset zurückgegeben wird. **false**, wenn eine Updatezählung oder kein Ergebnis zurückgegeben wird.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Die execute\-Methode wird von der execute\-Methode in der java.sql.PreparedStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [execute-Methode &#40;ISQLServerPreparedStatement&#41;](../content/execute-Method--SQLServerPreparedStatement-.md)   
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)   
 [SQLServerPreparedStatement-Klasse](../content/SQLServerPreparedStatement-Class.md)  
  
  