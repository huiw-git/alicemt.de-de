---
title: "forget-Methode (SQLServerXAResource)"
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
  - SQLServerXAResource.forget
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 6d83138d-aa45-4d94-9da6-fdfe7ed28edc
caps.latest.revision: 7
caps.handback.revision: 7
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
# forget-Methode (SQLServerXAResource)
    
## forget\-Methode \(SQLServerXAResource\)  
 Teilt dem Ressourcen\-Manager mit, dass eine heuristisch abgeschlossene Transaktionsverzweigung ignoriert \(vergessen\) werden kann.  
  
## Syntax  
  
```  
  
public void forget(javax.transaction.xa.Xid xid)  
```  
  
#### Parameter  
 *xid*  
  
 Ein Xid\-Objekt.  
  
## Ausnahmen  
 javax.transaction.xa.XAException  
  
## Hinweise  
 Diese forget\-Methode wird von der forget\-Methode in der javax.transaction.xa.XAResource\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerXAResource-Methoden](../content/SQLServerXAResource-Methods.md)   
 [SQLServerXAResource-Elemente](../content/SQLServerXAResource-Members.md)   
 [SQLServerXAResource-Klasse](../content/SQLServerXAResource-Class.md)  
  
  