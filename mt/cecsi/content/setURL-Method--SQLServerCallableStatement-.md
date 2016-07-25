---
title: "setURL-Methode (SQLServerCallableStatement)"
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
  - SQLServerCallableStatement.setURL
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 3d83675e-74ca-49d9-8461-6326773c5c8c
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
# setURL-Methode (SQLServerCallableStatement)
    
## setURL\-Methode \(SQLServerCallableStatement\)  
 Legt den angegebenen Parameter auf den angegebenen URL\-Wert fest.  
  
## Syntax  
  
```  
  
public void setURL(java.lang.String sCol,  
                   java.net.URL u)  
```  
  
#### Parameter  
 *sCol*  
  
 Ein **String** mit dem Namen des Parameters.  
  
 *u*  
  
 Ein URL\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setURL\-Methode wird von der setURL\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  