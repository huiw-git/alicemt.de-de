---
title: "setNClob-Methode (int, java.sql.NClob)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 48c8aa2a-4185-4837-b592-830e60f8ca0b
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
# setNClob-Methode (int, java.sql.NClob)
  Legt den angegebenen Parameter auf das angegebene NClob\-Objekt fest.  
  
## Syntax  
  
```  
  
public final void setNClob(int parameterIndex,  
              java.sql.NClob value)  
```  
  
#### Parameter  
 *parameterIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Parameterindex.  
  
 *value*  
  
 Ein NClob\-Objekt zum Angeben des Parameterwerts.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setNClob\-Methode wird von der setNClob\-Methode in der java.sql.PreparedStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [setNClob-Methode &#40;ISQLServerPreparedStatement&#41;](../content/setNClob-Method--SQLServerPreparedStatement-.md)   
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)  
  
  