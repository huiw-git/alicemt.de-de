---
title: "isSameRM-Methode (SQLServerXAResource)"
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
  - SQLServerXAResource.isSameRM
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: bfa24c46-b7cf-470a-afa1-52301847a448
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
# isSameRM-Methode (SQLServerXAResource)
    
## isSameRM\-Methode \(SQLServerXAResource\)  
 Ermittelt, ob die vom Zielobjekt dargestellte Ressourcen\-Manager\-Instanz der vom XAResource\-Objekt dargestellten Ressourcen\-Manager\-Instanz entspricht.  
  
## Syntax  
  
```  
  
public boolean isSameRM(javax.transaction.xa.XAResource xares)  
```  
  
#### Parameter  
 *xares*  
  
 Ein XAResource\-Objekt.  
  
## Rückgabewert  
 **true**, wenn die Instanzen identisch sind. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 javax.transaction.xa.XAException  
  
## Hinweise  
 Diese commit\-Methode wird von der commit\-Methode in der javax.transaction.xa.XAResource\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerXAResource-Methoden](../content/SQLServerXAResource-Methods.md)   
 [SQLServerXAResource-Elemente](../content/SQLServerXAResource-Members.md)   
 [SQLServerXAResource-Klasse](../content/SQLServerXAResource-Class.md)  
  
  