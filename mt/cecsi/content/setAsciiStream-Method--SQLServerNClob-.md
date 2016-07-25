---
title: "setAsciiStream-Methode (SQLServerNClob)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 617ece92-0fb1-4f95-b32d-29b5b56eb3fb
caps.latest.revision: 9
caps.handback.revision: 9
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
# setAsciiStream-Methode (SQLServerNClob)
  Ruft einen Datenstrom ab, der verwendet wird, um ab der angegebenen Position ASCII\-Zeichen in den **NCLOB**\-Wert zu schreiben, der von diesem **java.sql.NClob**\-Objekt dargestellt wird.  
  
## Syntax  
  
```  
  
public java.io.OutputStream setAsciiStream(long pos)  
```  
  
#### Parameter  
 *pos*  
  
 Die Position, ab der in das **NCLOB** geschrieben wird. Die erste Position ist "1".  
  
## Rückgabewert  
 Ein OutputStream\-Objekt, das für den Datenstrom steht, in den ASCII\-codierte Zeichen geschrieben werden können.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setAsciiStream\-Methode wird von der setAsciiStream\-Methode in der java.sql.NClob\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerNClob-Methoden](../content/SQLServerNClob-Methods.md)   
 [SQLServerNClob-Elemente](../content/SQLServerNClob-Members.md)   
 [SQLServerNClob-Klasse](../content/SQLServerNClob-Class.md)  
  
  