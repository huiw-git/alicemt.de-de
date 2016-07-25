---
title: "getNCharacterStream-Methode (int)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6ae704f5-823c-4dfe-8c08-07b547c61a3c
caps.latest.revision: 15
caps.handback.revision: 15
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
# getNCharacterStream-Methode (int)
  Ruft den Wert des angegebenen Parameters unter Berücksichtigung des Parameterindex als Reader\-Objekt ab.  
  
## Syntax  
  
```  
  
public final java.io.Reader getNCharacterStream(int parameterIndex)  
```  
  
#### Parameter  
 *parameterIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Parameterindex.  
  
## Rückgabewert  
 EinReader\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese Methode sollte beim Zugreifen auf Parameter vom Typ **NCHAR**, **NVARCHAR** und **LONGNVARCHAR** verwendet werden.  
  
 Diese getNCharacterStream\-Methode wird von der getNCharacterStream\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [getNCharacterStream-Methode &#40;SQLServerCallableStatement&#41;](../content/getNCharacterStream-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)  
  
  