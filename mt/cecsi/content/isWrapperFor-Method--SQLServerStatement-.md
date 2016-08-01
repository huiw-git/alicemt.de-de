---
title: "isWrapperFor-Methode (SQLServerStatement)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 53f3291f-d43a-476b-a656-d86168dacf6c
caps.latest.revision: 20
caps.handback.revision: 20
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
# isWrapperFor-Methode (SQLServerStatement)
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
 Die [isWrapperFor](../content/isWrapperFor-Method--SQLServerStatement-.md)\-Methode und die [unwrap](../content/unwrap-Method--SQLServerStatement-.md)\-Methode werden von der java.sql.Wrapper\-Schnittstelle definiert, die in JDBC 4.0 eingeführt wird.  
  
 Wird von dieser Methode "true" zurückgegeben, kann [unwrap](../content/unwrap-Method--SQLServerStatement-.md) erfolgreich mit dem gleichen Argument aufgerufen werden.  
  
 Beispielcode finden Sie unter [Beispiel zum Aktualisieren umfangreicher Daten](../content/Updating-Large-Data-Sample.md).  
  
 Weitere Informationen finden Sie unter [Wrapper und Schnittstellen](../content/Wrappers-and-Interfaces.md).  
  
## Siehe auch  
 [unwrap-Methode &#40;SQLServerStatement&#41;](../content/unwrap-Method--SQLServerStatement-.md)   
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  