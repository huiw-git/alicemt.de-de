---
title: "rollback-Methode (SQLServerXAResource)"
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
  - SQLServerXAResource.rollback
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 93d9d7e6-54b6-4d86-8f8c-386c6057e85e
caps.latest.revision: 6
caps.handback.revision: 6
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
# rollback-Methode (SQLServerXAResource)
    
## rollback\-Methode \(SQLServerXAResource\)  
 Fordert an, dass der Ressourcen\-Manager für die für den Transaktionszweig durchgeführte Arbeit ein Rollback ausführt.  
  
## Syntax  
  
```  
  
public void rollback(javax.transaction.xa.Xid xid)  
```  
  
#### Parameter  
 *xid*  
  
 Ein Xid\-Objekt.  
  
## Ausnahmen  
 javax.transaction.xa.XAException  
  
## Hinweise  
 Diese rollback\-Methode wird von der rollback\-Methode in der javax.transaction.xa.XAResource\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerXAResource-Methoden](../content/SQLServerXAResource-Methods.md)   
 [SQLServerXAResource-Elemente](../content/SQLServerXAResource-Members.md)   
 [SQLServerXAResource-Klasse](../content/SQLServerXAResource-Class.md)  
  
  