---
title: "setNull-Methode (java.lang.String, int, java.lang.String)"
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
  - SQLServerCallableStatement.setNull (java.lang.String, int, java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 16ff77f9-7928-415c-abf6-97ed59e3e396
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
# setNull-Methode (java.lang.String, int, java.lang.String)
    
## setNull\-Methode \(java.lang.String, int, java.lang.String\)  
 Legt den angegebenen Parameter unter Berücksichtigung des festzulegenden Parametertyps und \-namens auf einen NULL\-Wert fest.  
  
## Syntax  
  
```  
  
public void setNull(java.lang.String sCol,  
                    int nType,  
                    java.lang.String sTypeName)  
```  
  
#### Parameter  
 *sCol*  
  
 Ein **String** , mit dem Parameternamen.  
  
 *nType*  
  
 Ein JDBC\-Typcode, der durch ein java.sql.Types\-Element definiert wird.  
  
 *sTypeName*  
  
 Ein **String** , der den voll qualifizierten Namen des Parameters anzeigt, der festgelegt wird.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setNull\-Methode wird von der setNull\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [setNull-Methode &#40;SQLServerCallableStatement&#41;](../content/setNull-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  