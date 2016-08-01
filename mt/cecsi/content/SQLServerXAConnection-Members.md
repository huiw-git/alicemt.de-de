---
title: "SQLServerXAConnection-Elemente"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4b61dabd-369b-460c-8450-9fe424f76541
caps.latest.revision: 9
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
# SQLServerXAConnection-Elemente
    
## SQLServerXAConnection\-Elemente  
 Die folgenden Tabellen enthalten die Elemente, die von der [SQLServerXAConnection](../content/SQLServerXAConnection-Class.md)\-Klasse verfügbar gemacht werden.  
  
### Konstruktoren  
 Keine  
  
### Felder  
 Keine  
  
### Geerbte Felder  
 Keine  
  
### Methoden  
  
|Name|Beschreibung|  
|----------|------------------|  
|[addConnectionEventListener](../content/addConnectionEventListener-Method--SQLServerPooledConnection-.md)|\(Geerbt von [SQLServerPooledConnection](../content/SQLServerPooledConnection-Class.md)\) Registriert den angegebenen Ereignislistener, damit dieser benachrichtigt wird, wenn in Zusammenhang mit dem Connection\-Objekt ein Ereignis auftritt.|  
|[close](../content/close-Method--SQLServerPooledConnection-.md)|\(Geerbt von [SQLServerPooledConnection](../content/SQLServerPooledConnection-Class.md)\) Schließt die physische Verbindung, die von diesem Connection\-Objekt dargestellt wird.|  
|[getConnection](../content/getConnection-Method--SQLServerPooledConnection-.md)|\(Geerbt von [SQLServerPooledConnection](../content/SQLServerPooledConnection-Class.md)\) Erstellt ein Objekthandle für die physische Verbindung, die von diesem Connection\-Objekt dargestellt wird.|  
|[getXAResource](../content/getXAResource-Method--SQLServerXAConnection-.md)|Ruft ein [SQLServerXAResource](../content/SQLServerXAResource-Class.md)\-Objekt ab, mit dem der Transaktions\-Manager die Beteiligung des [SQLServerXAConnection](../content/SQLServerXAConnection-Class.md)\-Objekts in einer verteilten Transaktion verwaltet.|  
|[removeConnectionEventListener](../content/removeConnectionEventListener-Method--SQLServerPooledConnection-.md)|\(Geerbt von [SQLServerPooledConnection](../content/SQLServerPooledConnection-Class.md)\) Entfernt den angegebenen Ereignislistener.|  
  
### Geerbte Methoden  
  
|Klasse geerbt von:|Methoden|  
|------------------------|--------------|  
|com.microsoft.sqlserver.jdbc.SQLServerPooledConnection|addConnectionEventListener, close, getConnection, removeConnectionEventListener|  
|java.lang.Object|clone, equals, finalize, getClass, hashCode, notify, notifyAll, toString, wait|  
|javax.sql.PooledConnection|addConnectionEventListener, close, getConnection, removeConnectionEventListener|  
  
## Siehe auch  
 [SQLServerXAConnection-Klasse](../content/SQLServerXAConnection-Class.md)  
  
  