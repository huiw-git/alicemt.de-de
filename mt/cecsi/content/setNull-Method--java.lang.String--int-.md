---
title: "setNull-Methode (java.lang.String, int)"
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
  - SQLServerCallableStatement.setNull (java.lang.String, int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: e1d7e267-d9de-407a-b1a9-abdc2623478d
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
# setNull-Methode (java.lang.String, int)
    
## setNull\-Methode \(java.lang.String, int\)  
 Legt den angegebenen Parameter unter Berücksichtigung des festzulegenden Parametertyps auf einen NULL\-Wert fest.  
  
## Syntax  
  
```  
  
public void setNull(java.lang.String sCol,  
                    int nType)  
```  
  
#### Parameter  
 *sCol*  
  
 Ein **String** mit dem Parameternamen.  
  
 *nType*  
  
 Ein JDBC\-Typcode, der durch ein java.sql.Types\-Element definiert wird.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setNull\-Methode wird von der setNull\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [setNull-Methode &#40;SQLServerCallableStatement&#41;](../content/setNull-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  