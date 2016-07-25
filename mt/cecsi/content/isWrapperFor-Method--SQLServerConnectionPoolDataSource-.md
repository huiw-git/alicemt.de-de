---
title: "isWrapperFor-Methode (SQLServerConnectionPoolDataSource)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 09ed10eb-6e46-437b-a7c0-3c55574aad38
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
# isWrapperFor-Methode (SQLServerConnectionPoolDataSource)
  Gibt an, ob es sich bei diesem Objekt um einen Wrapper für die angegebene Schnittstelle handelt.  
  
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
 Die [isWrapperFor](../content/isWrapperFor-Method--SQLServerXADataSource-.md)\-Methode und die [unwrap](../content/unwrap-Method--SQLServerConnectionPoolDataSource-.md)\-Methode werden von der java.sql.Wrapper\-Schnittstelle definiert, die in den JDBC 4.0\-Spezifikationen eingeführt wird.  
  
 Wird von dieser Methode "true" zurückgegeben, kann [unwrap](../content/unwrap-Method--SQLServerConnectionPoolDataSource-.md) erfolgreich mit dem gleichen Argument aufgerufen werden.  
  
 Weitere Informationen finden Sie unter [Wrapper und Schnittstellen](../content/Wrappers-and-Interfaces.md).  
  
## Siehe auch  
 [unwrap-Methode &#40;SQLServerConnectionPoolDataSource&#41;](../content/unwrap-Method--SQLServerConnectionPoolDataSource-.md)   
 [SQLServerConnectionPoolDataSource-Methoden](../content/SQLServerConnectionPoolDataSource-Methods.md)   
 [SQLServerConnectionPoolDataSource-Elemente](../content/SQLServerConnectionPoolDataSource-Members.md)   
 [SQLServerConnectionPoolDataSource-Klasse](../content/SQLServerConnectionPoolDataSource-Class.md)  
  
  