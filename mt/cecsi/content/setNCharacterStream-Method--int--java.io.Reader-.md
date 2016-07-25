---
title: "setNCharacterStream-Methode (int, java.io.Reader)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7732746b-eda5-469e-8567-e8546c4d81cd
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
# setNCharacterStream-Methode (int, java.io.Reader)
  Legt den angegebenen Parameter auf das angegebene Reader\-Objekt fest.  
  
## Syntax  
  
```  
  
public final void setNCharacterStream(int parameterIndex,  
                                                 java.io.Reader value)  
```  
  
#### Parameter  
 *parameterIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Parameterindex.  
  
 *value*  
  
 Ein Reader\-Objekt, das den Parameterwert enthält.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setNCharacterStream\-Methode wird von der setNCharacterStream\-Methode in der java.sql.PreparedStatement\-Schnittstelle angegeben.  
  
 Diese Methode sollte für die Datentypen **NCHAR**, **NVARCHAR**, **NTEXT** und **XML** verwendet werden.  
  
## Siehe auch  
 [setNCharacterStream-Methode &#40;ISQLServerPreparedStatement&#41;](../content/setNCharacterStream-Method--SQLServerPreparedStatement-.md)   
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)  
  
  