---
title: "setSavepoint-Methode ()"
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
  - SQLServerConnection.setSavepoint ()
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 11013055-4fd3-45a9-b2da-28b2908dad52
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
# setSavepoint-Methode ()
    
## setSavepoint\-Methode \(\)  
 Erstellt in der aktuellen Transaktion einen unbenannten Sicherungspunkt und gibt das neue [SQLServerSavepoint](../content/SQLServerSavepoint-Class.md)\-Objekt zurück, das für den Sicherungspunkt steht.  
  
## Syntax  
  
```  
  
public java.sql.Savepoint setSavepoint()  
```  
  
## Rückgabewert  
 Ein SavePoint\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setSavePoint\-Methode wird von der setSavePoint\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
## Siehe auch  
 [setSavepoint-Methode &#40;ISQLServerConnection&#41;](../content/setSavepoint-Method--SQLServerConnection-.md)   
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  