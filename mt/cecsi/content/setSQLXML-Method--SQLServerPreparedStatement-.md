---
title: "setSQLXML-Methode (SQLServerPreparedStatement)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 70bbdde0-75f7-4169-88c5-dbbe2c4bcd03
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
# setSQLXML-Methode (SQLServerPreparedStatement)
  Legt den angegebenen Parameter auf das angegebene SQLXML\-Objekt fest.  
  
## Syntax  
  
```  
  
public final void setSQLXML(int parameterIndex,  
                            java.sql.SQLXML xmlObject)  
```  
  
#### Parameter  
 *parameterIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Parameterindex.  
  
 *xmlObject*  
  
 Ein SQLXML\-Objekt, das den Parameterwert enthält.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setSQLXML\-Methode wird von der setSQLXML\-Methode in der java.sql.PreparedStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)  
  
  