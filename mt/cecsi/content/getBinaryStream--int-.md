---
title: "getBinaryStream (int)"
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
  - SQLServerCallableStatement.getBinaryStream(int paramIndex)
apilocation: 
  - SQLServerCallableStatement.getBinaryStream(int paramIndex)
apitype: Assembly
ms.assetid: a766818e-cd05-4a07-a1ae-88966017448c
caps.latest.revision: 14
caps.handback.revision: 14
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
# getBinaryStream (int)
    
## getBinaryStream \(int\)  
 Ruft unter Berücksichtigung des Parameterindexes den Wert des angegebenen Parameters als Binärdatenstrom mit unterbrechungsfreien Bytes ab.  
  
## Syntax  
  
```  
  
public final java.io.InputStream getBinaryStream(int paramIndex)  
```  
  
#### Parameter  
 *paramIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Parameterindexes.  
  
## Rückgabewert  
 Ein InputStream\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Siehe auch  
 [getBinaryStream-Methode &#40;SQLServerCallableStatement&#41;](../content/getBinaryStream-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  