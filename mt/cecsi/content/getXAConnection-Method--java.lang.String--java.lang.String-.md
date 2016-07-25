---
title: "getXAConnection-Methode (java.lang.String, java.lang.String)"
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
  - SQLServerXADataSource.getXAConnection (java.lang.String, java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 276e0093-3d42-4f73-acc4-2b5b98245b40
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
# getXAConnection-Methode (java.lang.String, java.lang.String)
    
## getXAConnection\-Methode \(java.lang.String, java.lang.String\)  
 Stellt eine physikalische Datenbankverbindung anhand des angegebenen Benutzernamens und \-kennworts her.  
  
## Syntax  
  
```  
  
public javax.sql.XAConnection getXAConnection(java.lang.String user,  
                                              java.lang.String password)  
```  
  
#### Parameter  
 *user*  
  
 Ein **String** mit dem Benutzernamen.  
  
 *password*  
  
 Ein **String** mit dem Kennwort.  
  
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
  
  