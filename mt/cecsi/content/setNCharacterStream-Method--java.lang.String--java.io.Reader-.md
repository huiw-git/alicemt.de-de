---
title: "setNCharacterStream-Methode (java.lang.String, java.io.Reader)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fd19fbb8-a878-4d98-a584-e4969d649844
caps.latest.revision: 20
caps.handback.revision: 20
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
# setNCharacterStream-Methode (java.lang.String, java.io.Reader)
  Legt den angegebenen Parameter auf das angegebene Reader\-Objekt fest.  
  
## Syntax  
  
```  
  
public final void setNCharacterStream(java.lang.String parameterName,  
                       java.io.Reader value)  
```  
  
#### Parameter  
 *parameterName*  
  
 Ein **String** zum Angeben des Parameternamens.  
  
 *value*  
  
 Ein Reader\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setNCharacterStream\-Methode wird von der setNCharacterStream\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
 Diese Methode sollte für die Datentypen **NCHAR**, **NVARCHAR**, **NTEXT** und **XML** verwendet werden.  
  
## Siehe auch  
 [setNCharacterStream-Methode &#40;SQLServerCallableStatement&#41;](../content/setNCharacterStream-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)  
  
  