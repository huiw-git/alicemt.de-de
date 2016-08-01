---
title: "setNClob-Methode (java.lang.String, java.io.Reader, long)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c1b95ee7-7e82-418f-8f30-948589086f63
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
# setNClob-Methode (java.lang.String, java.io.Reader, long)
  Legt den angegebenen Parameter auf das angegebene Reader\-Objekt fest, dessen Länge der angegebenen Zeichenanzahl entspricht.  
  
## Syntax  
  
```  
  
public final void setNClob(java.lang.String parameterName,  
              java.io.Reader reader,  
              long length)  
```  
  
#### Parameter  
 *parameterName*  
  
 Ein **String** mit dem Parameternamen.  
  
 *reader*  
  
 Ein Reader\-Objekt.  
  
 *length*  
  
 Ein **long**\-Wert zum Angeben der Anzahl von Zeichen im Datenstrom.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese Methode sollte für die Parameterdatentypen **NCHAR**, **NVARCHAR**, **NTEXT** und **XML** verwendet werden.  
  
 Diese setNClob\-Methode wird von der setNClob\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [setNClob-Methode &#40;SQLServerCallableStatement&#41;](../content/setNClob-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)  
  
  