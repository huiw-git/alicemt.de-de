---
title: "setQueryTimeout-Methode (ISQLServerStatement)"
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
  - SQLServerStatement.setQueryTimeout
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 0c513265-cd0c-4b38-9494-94458c17a16d
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
# setQueryTimeout-Methode (ISQLServerStatement)
    
## setQueryTimeout\-Methode \(ISQLServerStatement\)  
 Legt die Anzahl von Sekunden, die vom Treiber auf die Ausführung eines [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekts gewartet wird, auf die angegebene Anzahl von Sekunden fest.  
  
## Syntax  
  
```  
  
public final void setQueryTimeout(int seconds)  
```  
  
#### Parameter  
 *seconds*  
  
 Ein Wert vom Typ **int** zum Angeben der Anzahl der Sekunden, die gewartet werden soll, bzw. 0, wenn keine Beschränkung festgelegt wurde.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setQueryTimeout\-Methode wird von der setQueryTimeout\-Methode in der java.sql.Statement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  