---
title: "getSQLXML-Methode (java.lang.String)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f56b192a-3255-4215-b552-8e494fbca083
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
# getSQLXML-Methode (java.lang.String)
  Ruft den Wert des angegebenen Parameters unter Berücksichtigung des Parameternamens als SQLXML\-Objekt ab.  
  
## Syntax  
  
```  
  
public final java.sql.SQLXML getSQLXML(java.lang.String parameterName)  
```  
  
#### Parameter  
 *parameterName*  
  
 Ein **String** zum Angeben des Parameternamens.  
  
## Rückgabewert  
 EinSQLXML\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getSQLXML\-Methode wird von der getSQLXML\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [getSQLXML-Methode &#40;SQLServerCallableStatement&#41;](../content/getSQLXML-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)  
  
  