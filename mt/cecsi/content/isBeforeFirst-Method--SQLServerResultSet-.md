---
title: "isBeforeFirst-Methode (ISQLServerResultSet)"
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
  - SQLServerResultSet.isBeforeFirst
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: e0e2bd28-6949-47dc-b9dd-145ffb337069
caps.latest.revision: 11
caps.handback.revision: 10
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
# isBeforeFirst-Methode (ISQLServerResultSet)
    
## isBeforeFirst\-Methode \(ISQLServerResultSet\)  
 Ruft ab, ob sich der Cursor an einer Position vor der ersten Zeile in diesem [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt befindet.  
  
## Syntax  
  
```  
  
public boolean isBeforeFirst()  
```  
  
## Rückgabewert  
 **true**, wenn sich der Cursor vor der ersten Zeile befindet. **false**, wenn sich der Cursor an einer beliebigen anderen Position befindet oder wenn das Resultset keine Zeilen enthält.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese isBeforeFirst\-Methode wird von der isBeforeFirst\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Wird diese Methode mit dynamischen Cursors verwendet, einschließlich schreibgeschützten Vorwärtscursors und die selectMethod\-Verbindungseigenschaft auf "cursor" festgelegt, wird eine Ausnahme ausgelöst.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  