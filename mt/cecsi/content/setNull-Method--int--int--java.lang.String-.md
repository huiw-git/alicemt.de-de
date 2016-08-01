---
title: "setNull-Methode (int, int, java.lang.String)"
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
  - SQLServerPreparedStatement.setNull (int, int, java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 43c74e06-2858-49ba-bae7-b88808e5fff4
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
# setNull-Methode (int, int, java.lang.String)
    
## setNull\-Methode \(int, int, java.lang.String\)  
 Legt den angegebenen Parameter unter Berücksichtigung des festzulegenden Parametertyps und \-namens auf einen NULL\-Wert fest.  
  
## Syntax  
  
```  
  
public final void setNull(int paramIndex,  
                          int sqlType,  
                          java.lang.String typeName)  
```  
  
#### Parameter  
 *paramIndex*  
  
 Ein Wert vom Typ **int** zum Angeben der Parameternummer.  
  
 *sqlType*  
  
 Ein JDBC\-Typcode gemäß der Definition von "java.sql.Types".  
  
 *typeName*  
  
 Ein **String** , der den voll qualifizierten Namen des Parameters anzeigt, der festgelegt wird.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Die setNull\-Methode wird von der setNull\-Methode in der java.sql.PreparedStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [setNull-Methode &#40;ISQLServerPreparedStatement&#41;](../content/setNull-Method--SQLServerPreparedStatement-.md)   
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)   
 [SQLServerPreparedStatement-Klasse](../content/SQLServerPreparedStatement-Class.md)  
  
  