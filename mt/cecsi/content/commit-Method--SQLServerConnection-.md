---
title: "commit-Methode (ISQLServerConnection)"
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
  - SQLServerConnection.commit
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: c7346165-51bf-4844-b64c-29833c147236
caps.latest.revision: 11
caps.handback.revision: 10
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
# commit-Methode (ISQLServerConnection)
    
## commit\-Methode \(ISQLServerConnection\)  
 Macht alle Änderungen, die seit dem letzten Commit oder Rollback vorgenommen wurden, zu dauerhaften Änderungen und hebt sämtliche Datenbanksperren auf, die derzeit von diesem [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt aufrecht erhalten werden.  
  
## Syntax  
  
```  
  
public void commit()  
```  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese commit\-Methode wird von der commit\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
 Die Methode sollte nur bei deaktiviertem Modus für automatische Commits verwendet werden.  
  
 Diese Methode ergibt einen Fehler und löst eine Ausnahme aus, wenn der Client mit einer manuellen Transaktion beginnt und von SQL Server aus irgendeinem Grund ein Rollback der manuellen Transaktion ausgeführt wird. Beispielsweise wird eine Ausnahme ausgelöst, wenn vom Client eine gespeicherte Prozedur, die explizit ROLLBACK TRANSACTION aufruft, und anschließend die commit\-Methode aufgerufen wird. Wird von SQL Server zudem ein Fehler mit einem Schweregrad ab 16 ausgelöst, um ein Rollback der vom Client initiierten manuellen Transaktion auszuführen, wird eine Ausnahme ausgelöst, wenn anschließend die commit\-Methode aufgerufen wird.  
  
## Siehe auch  
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  