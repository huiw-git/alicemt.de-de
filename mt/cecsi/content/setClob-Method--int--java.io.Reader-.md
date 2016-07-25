---
title: "setClob-Methode (int, java.io.Reader)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2b3727da-0480-4cea-b8b1-abda90699b84
caps.latest.revision: 25
caps.handback.revision: 25
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
# setClob-Methode (int, java.io.Reader)
  Legt den angegebenen Parameter auf das angegebene Reader\-Objekt fest.  
  
## Syntax  
  
```  
  
public final void setClob(int parameterIndex,  
                          java.io.Reader reader)  
```  
  
#### Parameter  
 *parameterIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Parameterindex.  
  
 *reader*  
  
 Ein Reader\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setClob\-Methode wird von der setClob\-Methode in der java.sql.PreparedStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [setClob-Methode &#40;ISQLServerPreparedStatement&#41;](../content/setClob-Method--SQLServerPreparedStatement-.md)   
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)  
  
  