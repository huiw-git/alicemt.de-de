---
title: "setTimestamp-Methode (java.lang.String, java.sql.Timestamp, java.util.Calendar)"
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
  - SQLServerCallableStatement.setTimestamp (java.lang.String, java.sql.Timestamp, java.util.Calendar))
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 09dca1f9-225a-4acb-9857-9a947e0829be
caps.latest.revision: 10
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
# setTimestamp-Methode (java.lang.String, java.sql.Timestamp, java.util.Calendar)
    
## setTimestamp\-Methode \(java.lang.String, java.sql.Timestamp, java.util.Calendar\)  
 Legt den angegebenen Parameter auf die angegebenen Zeitstempel\- und Kalenderwerte fest.  
  
## Syntax  
  
```  
  
public void setTimestamp(java.lang.String sCol,  
                         java.sql.Timestamp x,  
                         java.util.Calendar c)  
```  
  
#### Parameter  
 *sCol*  
  
 Ein **String** mit dem Parameternamen.  
  
 *x*  
  
 Ein Timestamp\-Objekt.  
  
 *c*  
  
 Ein Calendar\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setTimestamp\-Methode wird von der setTimestamp\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [setTimestamp-Methode &#40;SQLServerCallableStatement&#41;](../content/setTimestamp-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  