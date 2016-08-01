---
title: "recover-Methode (SQLServerXAResource)"
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
  - SQLServerXAResource.recover
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 840ecfcf-0dd3-4b7b-976f-dc9a96cd1464
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
# recover-Methode (SQLServerXAResource)
    
## recover\-Methode \(SQLServerXAResource\)  
 Ruft eine Liste vorbereiteter Transaktionszweige von einem Ressourcen\-Manager ab.  
  
## Syntax  
  
```  
  
public javax.transaction.xa.Xid[] recover(int flags)  
```  
  
#### Parameter  
 *flags*  
  
 Ein Wert vom Typ **int** . Mögliche Werte: XAResource.TMSTARTRSCAN oder XAResource.TMENDRSCAN oder XAResource.TMNOFLAGS oder XAResource.TMSTARTTRSCAN | XAResource.TMENDRSCAN.  
  
## Rückgabewert  
 Ein Xid\-Objekt.  
  
## Ausnahmen  
 javax.transaction.xa.XAException  
  
## Hinweise  
 Diese recover\-Methode wird von der recover\-Methode in der javax.transaction.xa.XAResource\-Schnittstelle angegeben.  
  
 Wenn der Parameter **flag** nicht auf XAResource.TMSTARTRSCAN oder XAResource.TMSTARTRSCAN | XAResource.TMENDRSCAN festgelegt, wird gerade ein Wiederherstellungsscan ausgeführt.  
  
## Siehe auch  
 [SQLServerXAResource-Methoden](../content/SQLServerXAResource-Methods.md)   
 [SQLServerXAResource-Elemente](../content/SQLServerXAResource-Members.md)   
 [SQLServerXAResource-Klasse](../content/SQLServerXAResource-Class.md)  
  
  