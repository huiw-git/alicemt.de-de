---
title: "getClientConnectionID-Methode (SQLServerConnection)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bee39c11-733a-461f-92cc-33efcb2af87d
caps.latest.revision: 6
caps.handback.revision: 5
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
# getClientConnectionID-Methode (SQLServerConnection)
  Ruft die Verbindungs\-ID des letzten Versuchs der Verbindungsherstellung ab, wobei es keine Rolle spielt, ob dieser Versuch erfolgreich war oder fehlgeschlagen ist.  
  
## Syntax  
  
```vb  
public Java.util.UUID SQLServerConnection.getClientConnectionID();  
```  
  
## Rückgabewert  
 Eine 16\-Byte\-GUID, die die Verbindungs\-ID des letzten Verbindungsversuchs darstellt bzw. NULL, wenn nach dem Initiieren der Verbindungsanforderung und dem Voranmeldungshandshake ein Fehler aufgetreten ist.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Weitere Informationen zum Zugriff auf Diagnoseinformationen im erweiterten Ereignisprotokoll finden Sie unter [Zugreifen auf Diagnoseinformationen im Protokoll der erweiterten Ereignisse](../content/Accessing-Diagnostic-Information-in-the-Extended-Events-Log.md).  
  
 Das folgende Beispiel zeigt, wie die Verbindungs\-ID abgerufen wird:  
  
```  
Connection con = DriverManager.getConnection(connectionUrl);  
UUID id = ((ISQLServerConnection)con).getClientConnectionId();  
```  
  
 Das folgende Beispiel zeigt eine andere Methode zum Abrufen der Verbindungs\-ID:  
  
```  
SQLServerConnectionPoolDataSource ds = new SQLServerConnectionPoolDataSource();  
ds.setUser("…");  
ds.setPassword("…");  
ds.setServerName("…");  
PooledConnection pcon= ds.getPooledConnection();  
Connection cn = pcon.getConnection();  
UUID conid = ((ISQLServerConnection)cn).getClientConnectionId();  
```  
  
 **getClientConnectionID** funktioniert unabhängig von der Version des Servers, mit dem Sie eine Verbindung herstellen. Erweiterte Ereignisprotokolle und Einträge zu Fehlern im Verbindungsringpuffer sind in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] 2008 R2 und früheren Versionen jedoch nicht verfügbar.  
  
 Wenn das erweiterte Ereignis zur Protokollierung der Verbindungs\-ID aktiviert ist, können Sie die Verbindungs\-ID im erweiterten Ereignisprotokoll suchen, um festzustellen, ob der Fehler auf dem Server aufgetreten ist. Bei bestimmten Verbindungsfehlern können Sie die Verbindungs\-ID auch im Verbindungsringpuffer suchen \([Behandlung von Verbindungsproblemen in SQL Server 2008 mithilfe des Verbindungsringpuffers](http://go.microsoft.com/fwlink/?LinkId=207752)\). Wenn die Verbindungs\-ID nicht im Verbindungsringpuffer enthalten ist, ist von einem Netzwerkfehler auszugehen.  
  
## Siehe auch  
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  