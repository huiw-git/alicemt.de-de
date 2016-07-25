---
title: "registerOutParameter-Methode (java.lang.String, int)"
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
  - SQLServerCallableStatement.registerOutParameter (java.lang.String, int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 5d00242c-4d9c-42cc-86bb-b76f5ef876b8
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
# registerOutParameter-Methode (java.lang.String, int)
    
## registerOutParameter\-Methode \(java.lang.String, int\)  
 Registriert den OUT\-Parameter mit dem angegebenen Namen für den angegebenen JDBC\-Typ.  
  
## Syntax  
  
```  
  
public void registerOutParameter(java.lang.String s,  
                                 int n)  
```  
  
#### Parameter  
 *s*  
  
 Ein **String** mit dem Parameternamen.  
  
 *n*  
  
 Ein JDBC\-Typcode gemäß Definition in "java.sql.Types".  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese registerOutParameter\-Methode wird von der registerOutParameter\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [registerOutParameter-Methode &#40;SQLServerCallableStatement&#41;](../content/registerOutParameter-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  