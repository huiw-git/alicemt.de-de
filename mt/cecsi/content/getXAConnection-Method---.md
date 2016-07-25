---
title: "getXAConnection-Methode ()"
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
  - SQLServerXADataSource.getXAConnection ()
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: b2710613-78b1-438f-b996-c7ae6f34381a
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
# getXAConnection-Methode ()
    
## getXAConnection\-Methode \(\)  
 Stellt eine physische Datenbankverbindung her, die in einer verteilten Transaktion verwendet werden kann.  
  
## Syntax  
  
```  
  
public javax.sql.XAConnection getXAConnection()  
```  
  
## Rückgabewert  
 Ein XAConnection\-Objekt.  
  
## Ausnahmen  
 java.sql.SQLException  
  
## Hinweise  
 Diese getXAConnection\-Methode wird von der getXAConnection\-Methode in der javax.sql.XADataSource\-Schnittstelle angegeben.  
  
> [!NOTE]  
>  Diese Methode wird normalerweise von XA\-Verbindungspoolimplementierungen und nicht vom regulären JDBC\-Anwendungscode aufgerufen.  
  
## Siehe auch  
 [getXAConnection-Methode &#40;SQLServerXADataSource&#41;](../content/getXAConnection-Method--SQLServerXADataSource-.md)   
 [SQLServerXADataSource-Methoden](../content/SQLServerXADataSource-Methods.md)   
 [SQLServerXADataSource-Elemente](../content/SQLServerXADataSource-Members.md)   
 [SQLServerXADataSource-Klasse](../content/SQLServerXADataSource-Class.md)  
  
  