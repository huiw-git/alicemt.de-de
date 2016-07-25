---
title: "isClosed-Methode (ISQLServerConnection)"
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
  - SQLServerConnection.isClosed
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 3560ab18-4350-4d02-9716-439f0c2f7142
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
# isClosed-Methode (ISQLServerConnection)
    
## isClosed\-Methode \(ISQLServerConnection\)  
 Gibt an, ob dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt geschlossen wurde.  
  
## Syntax  
  
```  
  
public boolean isClosed()  
```  
  
## Rückgabewert  
 **true**, wenn die Verbindung geschlossen ist, **false** wenn nicht.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese isClosed\-Methode wird von der isClosed\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
 Verifiziert den Status des aufgerufenen SQLServerConnection\-Objekts. Eine Verbindung wird geschlossen, wenn für sie die [close](../content/close-Method--SQLServerConnection-.md)\-Methode aufgerufen wurde oder bestimmte schwerwiegende Fehler aufgetreten sind. Diese Methode gibt nur dann **true** zurück, wenn sie nach dem Aufrufen der close\-Methode aufgerufen wurde.  
  
## Siehe auch  
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  