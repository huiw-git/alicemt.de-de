---
title: "isWrapperFor-Methode (SQLServerXADataSource)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d612461d-4c3f-46db-b968-ff4c80b2aa7c
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
# isWrapperFor-Methode (SQLServerXADataSource)
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
 Die [isWrapperFor](../content/isWrapperFor-Method--SQLServerXADataSource-.md)\-Methode und die [unwrap](../content/unwrap-Method--SQLServerXADataSource-.md)\-Methode werden von der java.sql.Wrapper\-Schnittstelle definiert, die in den JDBC 4.0\-Spezifikationen eingeführt wird.  
  
 Wird von dieser Methode "true" zurückgegeben, kann [unwrap](../content/unwrap-Method--SQLServerXADataSource-.md) erfolgreich mit dem gleichen Argument aufgerufen werden.  
  
 Weitere Informationen finden Sie unter [Wrapper und Schnittstellen](../content/Wrappers-and-Interfaces.md).  
  
## Siehe auch  
 [unwrap-Methode &#40;SQLServerXADataSource&#41;](../content/unwrap-Method--SQLServerXADataSource-.md)   
 [SQLServerXADataSource-Methoden](../content/SQLServerXADataSource-Methods.md)   
 [SQLServerXADataSource-Elemente](../content/SQLServerXADataSource-Members.md)   
 [SQLServerXADataSource-Klasse](../content/SQLServerXADataSource-Class.md)  
  
  