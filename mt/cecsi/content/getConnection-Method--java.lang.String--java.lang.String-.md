---
title: "getConnection-Methode (java.lang.String, java.lang.String)"
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
  - SQLServerDataSource.getConnection (java.lang.String, java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 78db89d6-a8a0-4116-8885-548e627220ed
caps.latest.revision: 10
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
# getConnection-Methode (java.lang.String, java.lang.String)
    
## getConnection\-Methode \(java.lang.String, java.lang.String\)  
 Stellt anhand des Benutzernamens und des Kennworts eine Verbindung mit der Datenquelle her, für die dieses [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Objekt steht.  
  
## Syntax  
  
```  
  
public java.sql.Connection getConnection(java.lang.String username,  
                                         java.lang.String password)  
```  
  
#### Parameter  
 *username*  
  
 Ein **String** mit dem Benutzernamen.  
  
 *password*  
  
 Ein **String** mit dem Kennwort.  
  
## Rückgabewert  
 Ein [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt.  
  
## Ausnahmen  
 java.sql.SQLException  
  
## Hinweise  
 Diese getConnection\-Methode wird von der getConnection\-Methode in der javax.sql.DataSource\-Schnittstelle angegeben.  
  
 Durch Aufrufen der getConnection\-Methode mit einem Benutzernamen oder Kennwort ungleich NULL werden die Benutzername\- und Kennworteigenschaften für die SQLServerDataSource\-Klasse beim Initialisieren des SQLServerConnection\-Objekts ersetzt. Beispiel: Hat der Aufrufer [setUser](../content/setUser-Method--SQLServerDataSource-.md) und [setPassword](../content/setPassword-Method--SQLServerDataSource-.md) für die Datenquelle aufgerufen und ruft anschließend getConnection auf und gibt einen Benutzernamen und ein Kennwort ungleich NULL an, werden der Benutzername und das Kennwort, der bzw. das durch setUser und setPassword festgelegt sind, durch das an getConnection weitergegebene Kennwort ersetzt.  
  
> [!NOTE]  
>  Benutzernamen und Kennwörter, die in der URL durch einen Aufruf der [setURL](../content/setURL-Method--SQLServerDataSource-.md)\-Methode festgelegt sind, werden in diesem Fall nicht geändert.  
  
## Siehe auch  
 [getConnection-Methode &#40;SQLServerDataSource&#41;](../content/getConnection-Method--SQLServerDataSource-.md)   
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  