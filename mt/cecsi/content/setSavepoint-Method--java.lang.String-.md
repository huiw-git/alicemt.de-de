---
title: "setSavepoint-Methode (java.lang.String)"
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
  - SQLServerConnection.setSavepoint (java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 1cf15ec4-d9d9-4ab3-bfee-2ea43ff609a6
caps.latest.revision: 12
caps.handback.revision: 12
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
# setSavepoint-Methode (java.lang.String)
  Erstellt in der aktuellen Transaktion einen Sicherungspunkt mit dem angegebenen Namen und gibt das neue [SQLServerSavepoint](../content/SQLServerSavepoint-Class.md)\-Objekt zurück, das für den Sicherungspunkt steht.  
  
## Syntax  
  
```  
  
public java.sql.Savepoint setSavepoint(java.lang.String sName)  
```  
  
#### Parameter  
 *sName*  
  
 Ein **String** mit dem Namen des Sicherungspunkts.  
  
## Rückgabewert  
 Ein SavePoint\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setSavePoint\-Methode wird von der setSavePoint\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
 Das *sName*\-Argument wird von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] automatisch mit Escapezeichen versehen.  
  
## Siehe auch  
 [setSavepoint-Methode &#40;ISQLServerConnection&#41;](../content/setSavepoint-Method--SQLServerConnection-.md)   
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  