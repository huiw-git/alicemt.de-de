---
title: "getCatalog-Methode (ISQLServerConnection)"
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
  - SQLServerConnection.getCatalog
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: e87ef65f-4b5a-4e1c-8db5-7f0932390bb0
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
# getCatalog-Methode (ISQLServerConnection)
    
## getCatalog\-Methode \(ISQLServerConnection\)  
 Ruft den aktuellen Katalognamen dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekts ab.  
  
## Syntax  
  
```  
  
public java.lang.String getCatalog()  
```  
  
## Rückgabewert  
 Ein **String** mit dem Katalognamen.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getCatalog\-Methode wird von der getCatalog\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
 Gibt die aktuelle Katalogeigenschaft des SQLServerConnection\-Objekts zurück, oder NULL, wenn sie nicht festgelegt ist. Die Katalogeigenschaft wird durch die [setCatalog](../content/setCatalog-Method--SQLServerConnection-.md)\-Methode eindeutig festgelegt oder durch Lesen der Umgebungsänderung für TDS für den aktuellen Katalog implizit aktualisiert.  
  
## Siehe auch  
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  