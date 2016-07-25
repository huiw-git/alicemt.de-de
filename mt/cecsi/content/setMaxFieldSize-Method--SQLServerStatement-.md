---
title: "setMaxFieldSize-Methode (ISQLServerStatement)"
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
  - SQLServerStatement.setMaxFieldSize
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 38f7fc1d-acad-4d10-9fc8-3c0669d93b07
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
# setMaxFieldSize-Methode (ISQLServerStatement)
    
## setMaxFieldSize\-Methode \(ISQLServerStatement\)  
 Legt das Limit für die maximale Anzahl von Bytes in einer [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Spalte, in der Zeichen\- oder Binärwerte gespeichert werden, auf die angegebene Anzahl von Bytes fest.  
  
## Syntax  
  
```  
  
public final void setMaxFieldSize(int max)  
```  
  
#### Parameter  
 *max*  
  
 Ein Wert vom Typ **int** zum Angeben der maximalen Anzahl von Bytes.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setMaxFieldSize\-Methode wird von der setMaxFieldSize\-Methode in der java.sql.Statement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  