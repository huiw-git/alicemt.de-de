---
title: "setCharacterStream-Methode (SQLServerNClob)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 09042ee9-dfb1-4d0b-82bd-d1224b0aea80
caps.latest.revision: 8
caps.handback.revision: 8
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
# setCharacterStream-Methode (SQLServerNClob)
  Ruft einen Datenstrom ab, der verwendet wird, um ab der angegebenen Position einen Unicode\-Zeichendatenstrom in den **NCLOB**\-Wert zu schreiben, der von diesem **java.sql.NClob**\-Objekt dargestellt wird.  
  
## Syntax  
  
```  
  
public java.io.Writer setCharacterStream(long pos)  
```  
  
#### Parameter  
 *pos*  
  
 Die Position, ab der in den **NCLOB**\-Wert geschrieben wird. Die erste Position ist "1".  
  
## Rückgabewert  
 Ein Writer\-Objekt, das für den Datenstrom steht, in den Unicode\-codierte Zeichen geschrieben werden können.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setCharacterStream\-Methode wird von der setCharacterStream\-Methode in der java.sql.NClob\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerNClob-Methoden](../content/SQLServerNClob-Methods.md)   
 [SQLServerNClob-Elemente](../content/SQLServerNClob-Members.md)   
 [SQLServerNClob-Klasse](../content/SQLServerNClob-Class.md)  
  
  