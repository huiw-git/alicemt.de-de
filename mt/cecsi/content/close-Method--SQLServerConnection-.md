---
title: "close-Methode (ISQLServerConnection)"
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
  - SQLServerConnection.close
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: f0f26585-bdf7-4737-b434-8c7e115c8e94
caps.latest.revision: 8
caps.handback.revision: 8
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
# close-Methode (ISQLServerConnection)
    
## close\-Methode \(ISQLServerConnection\)  
 Gibt die Datenbank\- und JDBC\-Ressourcen dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekts umgehend frei, sodass nicht auf deren automatische Freigabe gewartet werden muss.  
  
## Syntax  
  
```  
  
public void close()  
```  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese close\-Methode wird von der close\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
 Durch Aufrufen der close\-Methode in der Mitte einer Transaktion wird ein Rollback für die Transaktion ausgeführt.  
  
## Siehe auch  
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  