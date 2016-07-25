---
title: "nativeSQL-Methode (SQLServerConnection)"
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
  - SQLServerConnection.nativeSQL
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 2188a6e1-792f-47bd-b207-1d01741231b2
caps.latest.revision: 14
caps.handback.revision: 14
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
# nativeSQL-Methode (SQLServerConnection)
  Konvertiert die angegebene SQL\-Anweisung zur systemeigenen SQL\-Grammatik des Datenbankservers.  
  
> [!NOTE]  
>  Diese Methode wird von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] derzeit nicht unterstützt.  
  
## Syntax  
  
```  
  
public java.lang.String nativeSQL(java.lang.String sql)  
```  
  
#### Parameter  
 *sql*  
  
 Ein **String** mit einer SQL\-Anweisung.  
  
## Rückgabewert  
 Ein **String** mit der konvertierten SQL\-Anweisung.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese nativeSQL\-Methode wird von der nativeSQL\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  