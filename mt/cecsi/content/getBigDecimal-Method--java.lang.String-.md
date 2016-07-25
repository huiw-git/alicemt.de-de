---
title: "getBigDecimal-Methode (java.lang.String)"
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
  - SQLServerCallableStatement.getBigDecimal (java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: d0b29b48-9663-4de4-9fc2-82bc30e44aed
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
# getBigDecimal-Methode (java.lang.String)
    
## getBigDecimal\-Methode \(java.lang.String\)  
 Ruft den Wert des angegebenen Parameters unter Berücksichtigung des Parameternamens als java.math.BigDecimal\-Objekt mit vollständiger Genauigkeit ab.  
  
## Syntax  
  
```  
  
public java.math.BigDecimal getBigDecimal(java.lang.String sCol)  
```  
  
#### Parameter  
 *sCol*  
  
 Ein **String** mit dem Parameternamen.  
  
## Rückgabewert  
 Ein BigDecimal\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getBigDecimal\-Methode wird von der getBigDecimal\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [getBigDecimal-Methode &#40;SQLServerCallableStatement&#41;](../content/getBigDecimal-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  