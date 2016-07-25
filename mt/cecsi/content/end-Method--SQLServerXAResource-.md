---
title: "end-Methode (SQLServerXAResource)"
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
  - SQLServerXAResource.end
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: e6418b27-793b-4b36-8dfb-756aec7bcbba
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
# end-Methode (SQLServerXAResource)
    
## end\-Methode \(SQLServerXAResource\)  
 Beendet die für einen Transaktionszweig durchgeführte Arbeit.  
  
## Syntax  
  
```  
  
public void end(javax.transaction.xa.Xid xid,  
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
 Diese end\-Methode wird von der end\-Methode in der javax.transaction.xa.XAResource\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerXAResource-Methoden](../content/SQLServerXAResource-Methods.md)   
 [SQLServerXAResource-Elemente](../content/SQLServerXAResource-Members.md)   
 [SQLServerXAResource-Klasse](../content/SQLServerXAResource-Class.md)  
  
  