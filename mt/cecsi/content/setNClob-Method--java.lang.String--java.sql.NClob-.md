---
title: "setNClob-Methode (java.lang.String, java.sql.NClob)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4e30d242-0c1b-45db-b75f-41b041692f31
caps.latest.revision: 16
caps.handback.revision: 16
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
# setNClob-Methode (java.lang.String, java.sql.NClob)
  Legt den angegebenen Parameter auf das angegebene NClob\-Objekt fest.  
  
## Syntax  
  
```  
  
public final void setNClob(java.lang.String parameterName,  
              java.sql.NClob value)  
```  
  
#### Parameter  
 *parameterName*  
  
 Ein **String** mit dem Parameternamen.  
  
 *value*  
  
 Ein NClob\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese Methode sollte für die Parameterdatentypen **NCHAR**, **NVARCHAR**, **NTEXT** und **XML** verwendet werden.  
  
 Diese setNClob\-Methode wird von der setNClob\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [setNClob-Methode &#40;SQLServerCallableStatement&#41;](../content/setNClob-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)  
  
  