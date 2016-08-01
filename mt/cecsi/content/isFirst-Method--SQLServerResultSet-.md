---
title: "isFirst-Methode (ISQLServerResultSet)"
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
  - SQLServerResultSet.isFirst
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 2ff94b95-32ad-4378-8bb1-970030527bb2
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
# isFirst-Methode (ISQLServerResultSet)
    
## isFirst\-Methode \(ISQLServerResultSet\)  
 Ruft ab, ob sich der Cursor in der ersten Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts befindet.  
  
## Syntax  
  
```  
  
public boolean isFirst()  
```  
  
## Rückgabewert  
 **true**, wenn sich der Cursor in der ersten Zeile befindet. **false**, wenn sich der Cursor an einer beliebigen anderen Position befindet oder wenn das Resultset keine Zeilen enthält.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese isFirst\-Methode wird von der isFirst\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Wird diese Methode mit Vorwärtscursors und dynamischen Cursors verwendet, wird eine Ausnahme ausgelöst.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  