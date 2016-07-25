---
title: "setAutoCommit-Methode (ISQLServerConnection)"
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
  - SQLServerConnection.setAutoCommit
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: db1e22d2-e53f-474e-8c99-cb1fff7f491a
caps.latest.revision: 13
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
# setAutoCommit-Methode (ISQLServerConnection)
    
## setAutoCommit\-Methode \(ISQLServerConnection\)  
 Legt für dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt den aktuellen Modus für automatische Commits auf den angegebenen Zustand fest.  
  
## Syntax  
  
```  
  
public void setAutoCommit(boolean value)  
```  
  
#### Parameter  
 *value*  
  
 **true**, um den Modus für automatische Commits für die Verbindung zu aktivieren, oder **false**, um den Modus zu deaktivieren.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setAutoCommit\-Methode wird von der setAutoCommit\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
 Ist für eine Verbindung der Modus für automatische Commits aktiviert, werden alle SQL\-Anweisungen als einzelne Transaktionen ausgeführt, und die Commits der SQL\-Anweisungen werden als einzelne Transaktionen ausgeführt. Andernfalls werden die SQL\-Anweisungen in Transaktionen gruppiert, die mit einem Aufruf der [commit](../content/commit-Method--SQLServerConnection-.md)\- oder der [rollback](../content/rollback-Method--SQLServerConnection-.md)\-Methode beendet werden. Der Modus für automatische Commits ist für neue Verbindungen standardmäßig aktiviert.  
  
 Der Commit wird ausgeführt, wenn die Anweisung abgeschlossen wird oder die nächste Ausführung durchgeführt wird, je nachdem, welches Ereignis zuerst eintritt. Bei Anweisungen, von denen ein [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt zurückgegeben wird, wird die Anweisung abgeschlossen, wenn die letzte Zeile des Ergebnisses abgerufen oder das Resultset geschlossen wurde. In erweiterten Fällen kann eine einzelne Anweisung zusätzlich zu den Ausgabeparameterwerten mehrere Ergebnisse zurückgeben. In diesen Fällen wird der Commit ausgeführt, nachdem alle Ergebnisse und Ausgabeparameterwerte abgerufen wurden.  
  
 Ist der Modus für automatische Commits auf **false** gesetzt, startet der JDBC\-Treiber nach jedem Commit implizit eine neue Transaktion.  
  
> [!NOTE]  
>  Wenn diese Methode während einer Transaktion aufgerufen wird, wird ein Commit der Transaktion ausgeführt.  
  
## Siehe auch  
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  