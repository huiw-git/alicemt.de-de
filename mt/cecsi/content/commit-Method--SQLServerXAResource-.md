---
title: "Commit-Methode (SQLServerXAResource)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLServerXAResource.commit
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 1d0f8612-fb4a-4eca-bc37-8342e1419fd4
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
# Commit-Methode (SQLServerXAResource)
    
## Commit\-Methode \(SQLServerXAResource\)  
 Führt einen Commit für die globale Transaktion aus, die durch das angegebene Xid\-Objekt festgelegt wird.  
  
## Syntax  
  
```  
  
public void commit(javax.transaction.xa.Xid xid,  
                   boolean onePhase)  
```  
  
#### Parameter  
 *xid*  
  
 Ein Xid\-Objekt.  
  
 *onePhase*  
  
 Ein Wert vom Typ **boolean** .  
  
## Ausnahmen  
 javax.transaction.xa.XAException  
  
## Hinweise  
 Diese commit\-Methode wird von der commit\-Methode in der javax.transaction.xa.XAResource\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerXAResource-Methoden](../content/SQLServerXAResource-Methods.md)   
 [SQLServerXAResource-Elemente](../content/SQLServerXAResource-Members.md)   
 [SQLServerXAResource-Klasse](../content/SQLServerXAResource-Class.md)  
  
  