---
title: "setNClob-Methode (java.lang.String, java.io.Reader)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a595679a-89b7-4b18-9ad2-d9cb13af2a28
caps.latest.revision: 15
caps.handback.revision: 15
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
# setNClob-Methode (java.lang.String, java.io.Reader)
  Legt den angegebenen Parameter auf das angegebene Reader\-Objekt fest.  
  
## Syntax  
  
```  
  
public final void setNClob(java.lang.String parameterName,  
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
 Diese Methode sollte für die Parameterdatentypen **NCHAR**, **NVARCHAR**, **NTEXT** und **XML** verwendet werden.  
  
 Diese setNClob\-Methode wird von der setNClob\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [setNClob-Methode &#40;SQLServerCallableStatement&#41;](../content/setNClob-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)  
  
  