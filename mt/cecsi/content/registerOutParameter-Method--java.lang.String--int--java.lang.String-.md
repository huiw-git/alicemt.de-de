---
title: "registerOutParameter-Methode (java.lang.String, int, java.lang.String)"
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
  - SQLServerCallableStatement.registerOutParameter
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: f962c912-2475-4e1f-a384-579be2d17f37
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
# registerOutParameter-Methode (java.lang.String, int, java.lang.String)
    
## registerOutParameter\-Methode \(java.lang.String, int, java.lang.String\)  
 Registriert den OUT\-Parameter mit dem angegebenen Namen für den angegebenen JDBC\-Typ und den Typnamen.  
  
## Syntax  
  
```  
  
public void registerOutParameter(java.lang.String s,  
                                 int n,  
                                 java.lang.String s1)  
```  
  
#### Parameter  
 *s*  
  
 Ein **String** mit dem Parameternamen.  
  
 *n*  
  
 Ein JDBC\-Typcode gemäß der Definition in "java.sql.Types".  
  
 *s1*  
  
 Ein **String** , der den vollqualifizierten SQL\-Typnamen enthält.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese registerOutParameter\-Methode wird von der registerOutParameter\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [registerOutParameter-Methode &#40;SQLServerCallableStatement&#41;](../content/registerOutParameter-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  