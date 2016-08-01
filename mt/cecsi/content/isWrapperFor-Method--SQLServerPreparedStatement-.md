---
title: "isWrapperFor-Methode (SQLServerPreparedStatement)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b0e591b1-73e2-4f90-967f-5555eadfc3f1
caps.latest.revision: 10
caps.handback.revision: 10
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
# isWrapperFor-Methode (SQLServerPreparedStatement)
  Gibt an, ob es sich bei diesem Anweisungsobjekt um einen Wrapper für die angegebene Schnittstelle handelt.  
  
## Syntax  
  
```  
  
public boolean isWrapperFor(Class iface)  
```  
  
#### Parameter  
 *iface*  
  
 **class** zum Definieren einer Schnittstelle.  
  
## Rückgabewert  
 **true**, wenn die Schnittstelle von diesem Objekt implementiert wird oder das Objekt als Wrapper für ein Objekt fungiert, von dem die Schnittstelle implementiert wird. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Die [isWrapperFor](../content/isWrapperFor-Method--SQLServerPreparedStatement-.md)\-Methode und die [unwrap](../content/unwrap-Method--SQLServerPreparedStatement-.md)\-Methode werden von der java.sql.Wrapper\-Schnittstelle definiert, die in den JDBC 4.0\-Spezifikationen eingeführt wird.  
  
 Wird von dieser Methode "true" zurückgegeben, kann [unwrap](../content/unwrap-Method--SQLServerPreparedStatement-.md) erfolgreich mit dem gleichen Argument aufgerufen werden.  
  
 Weitere Informationen finden Sie unter [Wrapper und Schnittstellen](../content/Wrappers-and-Interfaces.md).  
  
## Siehe auch  
 [unwrap-Methode &#40;SQLServerPreparedStatement&#41;](../content/unwrap-Method--SQLServerPreparedStatement-.md)   
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)   
 [SQLServerPreparedStatement-Klasse](../content/SQLServerPreparedStatement-Class.md)  
  
  