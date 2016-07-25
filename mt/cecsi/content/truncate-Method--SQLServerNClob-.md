---
title: "truncate-Methode (SQLServerNClob)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b7e8210d-a724-4bae-832a-ae4c63031c9c
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
# truncate-Methode (SQLServerNClob)
  Kürzt das **NCLOB** auf die angegebene Länge.  
  
## Syntax  
  
```  
  
public void truncate(long len)  
```  
  
#### Parameter  
 *len*  
  
 Die Länge \(in Zeichen\), auf die der **NCLOB**\-Wert gekürzt werden soll.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese truncate\-Methode wird von der truncate\-Methode in der java.sql.NClob\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerNClob-Methoden](../content/SQLServerNClob-Methods.md)   
 [SQLServerNClob-Elemente](../content/SQLServerNClob-Members.md)   
 [SQLServerNClob-Klasse](../content/SQLServerNClob-Class.md)  
  
  