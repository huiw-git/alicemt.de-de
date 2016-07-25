---
title: "setCharacterStream-Methode (java.lang.String, java.io.Reader)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 43acac5b-5a8a-4685-bee6-7194d2d03a52
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
# setCharacterStream-Methode (java.lang.String, java.io.Reader)
  Legt den angegebenen Parameter auf das angegebene Reader\-Objekt fest.  
  
## Syntax  
  
```  
  
public final void setCharacterStream(java.lang.String parameterName,  
                                             java.io.Reader reader)  
```  
  
#### Parameter  
 *parameterName*  
  
 Ein **String** mit dem Parameternamen.  
  
 *reader*  
  
 Ein Reader\-Objekt, das die Unicode\-Daten enthält.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setCharacterStream\-Methode wird von der setCharacterStream\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [setCharacterStream-Methode &#40;SQLServerCallableStatement&#41;](../content/setCharacterStream-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)  
  
  