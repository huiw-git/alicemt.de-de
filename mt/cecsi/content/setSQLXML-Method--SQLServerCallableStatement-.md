---
title: "setSQLXML-Methode (SQLServerCallableStatement)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: de095cb3-1111-4154-8996-3c2e529e3000
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
# setSQLXML-Methode (SQLServerCallableStatement)
  Legt den angegebenen Parameter auf das angegebene SQLXML\-Objekt fest.  
  
## Syntax  
  
```  
  
public final void setSQLXML(java.lang.String parameterName,  
                            java.sql.SQLXML xmlObject)  
```  
  
#### Parameter  
 *parameterName*  
  
 Ein **String** zum Angeben des Parameternamens.  
  
 *xmlObject*  
  
 Ein SQLXML\-Objekt, das den Parameterwert enthält.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setSQLXML\-Methode wird von der setSQLXML\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)  
  
  