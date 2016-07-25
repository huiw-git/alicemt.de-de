---
title: "getNString-Methode (java.lang.String)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b351e999-85bf-498b-915a-f91d89134bce
caps.latest.revision: 13
caps.handback.revision: 13
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
# getNString-Methode (java.lang.String)
  Ruft den Wert des angegebenen Parameters vom Typ **NCHAR**, **NVARCHAR** oder **LONGNVARCHAR** als String in der Programmiersprache Java ab.  
  
## Syntax  
  
```  
  
public final java.lang.String getNString(java.lang.String parameterName)  
```  
  
#### Parameter  
 *parameterName*  
  
 Ein **String** mit dem Parameternamen.  
  
## Rückgabewert  
 EinString\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getNString\-Methode wird von der getNString\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [getNString-Methode &#40;SQLServerCallableStatement&#41;](../content/getNString-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Methoden](../content/SQLServerCallableStatement-Methods.md)  
  
  