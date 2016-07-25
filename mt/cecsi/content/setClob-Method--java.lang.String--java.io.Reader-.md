---
title: "setClob-Methode (java.lang.String, java.io.Reader)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f7457b8a-df31-4999-883e-8cc386a48ceb
caps.latest.revision: 14
caps.handback.revision: 14
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
# setClob-Methode (java.lang.String, java.io.Reader)
  Legt den angegebenen Parameter auf das angegebene Reader\-Objekt fest.  
  
## Syntax  
  
```  
  
public final void setClob(java.lang.String parameterName,  
            java.io.Reader reader)  
```  
  
#### Parameter  
 *parameterName*  
  
 Ein **String** mit dem Parameternamen.  
  
 *reader*  
  
 Ein Reader\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setClob\-Methode wird von der setClob\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [setClob-Methode &#40;SQLServerCallableStatement&#41;](../content/setClob-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)  
  
  