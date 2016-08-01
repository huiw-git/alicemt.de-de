---
title: "setTransactionTimeout-Methode (SQLServerXAResource)"
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
  - SQLServerXAResource.setTransactionTimeout
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 38bf4a1a-6ad3-437c-b9ed-8792ab6dde7e
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
# setTransactionTimeout-Methode (SQLServerXAResource)
    
## setTransactionTimeout\-Methode \(SQLServerXAResource\)  
 Legt den aktuellen Transaktionstimeoutwert für das [SQLServerXAResource](../content/SQLServerXAResource-Class.md)\-Objekt fest.  
  
## Syntax  
  
```  
  
public boolean setTransactionTimeout(int seconds)  
```  
  
#### Parameter  
 *seconds*  
  
 Ein **int** \-Wert.  
  
## Rückgabewert  
 **true**, wenn das Timeout festgelegt wurde. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 javax.transaction.xa.XAException  
  
## Hinweise  
 Diese setTransactionTimeout\-Methode wird von der setTransactionTimeout\-Methode in der javax.transaction.xa.XAResource\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerXAResource-Methoden](../content/SQLServerXAResource-Methods.md)   
 [SQLServerXAResource-Elemente](../content/SQLServerXAResource-Members.md)   
 [SQLServerXAResource-Klasse](../content/SQLServerXAResource-Class.md)  
  
  