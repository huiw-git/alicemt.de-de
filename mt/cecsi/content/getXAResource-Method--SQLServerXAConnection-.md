---
title: "getXAResource-Methode (SQLServerXAConnection)"
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
  - SQLServerXAConnection.getXAResource
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: e1d2828f-fd20-44b0-b796-dc70f77c5b03
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
# getXAResource-Methode (SQLServerXAConnection)
    
## getXAResource\-Methode \(SQLServerXAConnection\)  
 Ruft ein [SQLServerXAResource](../content/SQLServerXAResource-Class.md)\-Objekt ab, mit dem der Transaktions\-Manager die Beteiligung des [SQLServerXAConnection](../content/SQLServerXAConnection-Class.md)\-Objekts in einer verteilten Transaktion verwaltet.  
  
## Syntax  
  
```  
  
public javax.transaction.xa.XAResource getXAResource()  
```  
  
## Rückgabewert  
 Ein XAResource\-Objekt.  
  
## Ausnahmen  
 java.sql.SQLException  
  
## Hinweise  
 Diese getXAResource\-Methode wird von der getXAResource\-Methode in der javax.sql.XAConnection\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerXAConnection-Methoden](../content/SQLServerXAConnection-Methods.md)   
 [SQLServerXAConnection-Elemente](../content/SQLServerXAConnection-Members.md)   
 [SQLServerXAConnection-Klasse](../content/SQLServerXAConnection-Class.md)  
  
  