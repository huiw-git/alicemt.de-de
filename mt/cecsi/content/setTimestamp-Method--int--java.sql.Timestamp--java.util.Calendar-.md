---
title: "setTimestamp-Methode (int, java.sql.Timestamp, java.util.Calendar)"
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
  - SQLServerPreparedStatement.setTimestamp (int, java.sql.Timestamp, java.util.Calendar))
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 10c93cbf-f831-4e00-8e37-ea728bf34b1e
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
# setTimestamp-Methode (int, java.sql.Timestamp, java.util.Calendar)
    
## setTimestamp\-Methode \(int, java.sql.Timestamp, java.util.Calendar\)  
 Legt den angegebenen Parameter auf die angegebenen Zeitstempel\- und Kalenderwerte fest.  
  
## Syntax  
  
```  
  
public final void setTimestamp(int n,  
                               java.sql.Timestamp x,  
                               java.util.Calendar cal)  
```  
  
#### Parameter  
 *n*  
  
 Ein Wert vom Typ **int** zum Angeben der Parameternummer.  
  
 *x*  
  
 Ein Timestamp\-Objekt.  
  
 *cal*  
  
 Ein Calendar\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setTimestamp\-Methode wird von der setTimestamp\-Methode in der java.sql.PreparedStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [setTimestamp-Methode &#40;ISQLServerPreparedStatement&#41;](../content/setTimestamp-Method--SQLServerPreparedStatement-.md)   
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)   
 [SQLServerPreparedStatement-Klasse](../content/SQLServerPreparedStatement-Class.md)  
  
  