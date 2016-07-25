---
title: "setNClob-Methode (int, java.io.Reader)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9fc9938c-b821-41c7-8df7-e21cb83a46d4
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
# setNClob-Methode (int, java.io.Reader)
  Legt den angegebenen Parameter auf das angegebene Reader\-Objekt fest.  
  
## Syntax  
  
```  
  
public final void setNClob(int parameterIndex,  
                    java.io.Reader reader)  
```  
  
#### Parameter  
 *parameterIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Parameterindex.  
  
 *reader*  
  
 Ein Reader\-Objekt zum Angeben des Parameterwerts.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setNClob\-Methode wird von der setNClob\-Methode in der java.sql.PreparedStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [setNClob-Methode &#40;ISQLServerPreparedStatement&#41;](../content/setNClob-Method--SQLServerPreparedStatement-.md)   
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)  
  
  