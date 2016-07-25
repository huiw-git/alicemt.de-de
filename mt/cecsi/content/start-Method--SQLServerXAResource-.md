---
title: "start-Methode (SQLServerXAResource)"
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
  - SQLServerXAResource.start
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 33c90213-92f7-416b-b2fa-67a1afe64e97
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
# start-Methode (SQLServerXAResource)
    
## start\-Methode \(SQLServerXAResource\)  
 Startet die Arbeit am Xid\-Objekt, das in einem Transaktionszweig angegeben ist.  
  
## Syntax  
  
```  
  
public void start(javax.transaction.xa.Xid xid,  
                  int flags)  
```  
  
#### Parameter  
 *xid*  
  
 Ein Xid\-Objekt.  
  
 *flags*  
  
 Ein **int** \-Wert.  
  
## Ausnahmen  
 javax.transaction.xa.XAException  
  
## Hinweise  
 Diese start\-Methode wird von der start\-Methode in der javax.transaction.xa.XAResource\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerXAResource-Methoden](../content/SQLServerXAResource-Methods.md)   
 [SQLServerXAResource-Elemente](../content/SQLServerXAResource-Members.md)   
 [SQLServerXAResource-Klasse](../content/SQLServerXAResource-Class.md)  
  
  