---
title: "setString-Methode (long, java.lang.String) (SQLServerNClob)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 698073b2-3f0c-449c-ad68-48144698fe8f
caps.latest.revision: 11
caps.handback.revision: 11
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
# setString-Methode (long, java.lang.String) (SQLServerNClob)
  Schreibt den angegebenen **String** ab der angegebenen Position in das **NCLOB**.  
  
## Syntax  
  
```  
  
public int setString(long pos,  
              java.lang.String str)  
```  
  
#### Parameter  
 *pos*  
  
 Die Position, ab der in das **NCLOB** geschrieben wird. Die erste Position ist "1".  
  
 *str*  
  
 Der String, der in das **NCLOB** geschrieben werden soll.  
  
## Rückgabewert  
 Die Anzahl der geschriebenen Zeichen.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setString\-Methode wird von der setString\-Methode in der java.sql.NClob\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerNClob-Methoden](../content/SQLServerNClob-Methods.md)   
 [SQLServerNClob-Elemente](../content/SQLServerNClob-Members.md)   
 [SQLServerNClob-Klasse](../content/SQLServerNClob-Class.md)  
  
  