---
title: "setNClob-Methode (int, java.io.Reader, long)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 11071f8f-0e9b-45f0-b600-aaef7e2815d8
caps.latest.revision: 22
caps.handback.revision: 22
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
# setNClob-Methode (int, java.io.Reader, long)
  Legt den angegebenen Parameter auf das angegebene Reader\-Objekt fest, dessen Länge der angegebenen Zeichenanzahl entspricht.  
  
## Syntax  
  
```  
  
public final void setNClob(int parameterIndex,  
                    java.io.Reader reader,  
                    long length)  
```  
  
#### Parameter  
 *parameterIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Parameterindex.  
  
 *reader*  
  
 Ein Reader\-Objekt zum Angeben des Parameterwerts.  
  
 *length*  
  
 Ein **long**\-Wert zum Angeben der Anzahl von Zeichen im Parameterwert.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setNClob\-Methode wird von der setNClob\-Methode in der java.sql.PreparedStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [setNClob-Methode &#40;ISQLServerPreparedStatement&#41;](../content/setNClob-Method--SQLServerPreparedStatement-.md)   
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)  
  
  