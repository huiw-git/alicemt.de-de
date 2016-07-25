---
title: "getCharacterStream (int)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLServerCallableStatement.getCharacterStream(int paramIndex)
apilocation: 
  - SQLServerCallableStatement.getCharacterStream(int paramIndex)
apitype: Assembly
ms.assetid: eb20714b-52bc-4b6c-b23f-c9c3c9d73783
caps.latest.revision: 13
caps.handback.revision: 13
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
# getCharacterStream (int)
    
## getCharacterStream \(int\)  
 Ruft den Wert des angegebenen Parameters unter Berücksichtigung des Parameterindexes als java.io.Reader\-Objekt ab.  
  
## Syntax  
  
```  
  
public final java.io.Reader getCharacterStream(int paramIndex)  
```  
  
#### Parameter  
 *paramIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Parameterindexes.  
  
## Rückgabewert  
 Ein Reader\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Siehe auch  
 [getCharacterStream-Methode &#40;SQLServerCallableStatement&#41;](../content/getCharacterStream-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  