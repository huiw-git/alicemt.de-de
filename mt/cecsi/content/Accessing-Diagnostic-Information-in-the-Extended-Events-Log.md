---
title: "Zugreifen auf Diagnoseinformationen im Protokoll der erweiterten Ereignisse"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a79e9468-2257-4536-91f1-73b008c376c3
caps.latest.revision: 16
caps.handback.revision: 15
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
# Zugreifen auf Diagnoseinformationen im Protokoll der erweiterten Ereignisse
  In [!INCLUDE[jdbc_40](../content/includes/jdbc_40_md.md)] wurde die Ablaufverfolgung \([Ablaufverfolgung für Treibervorgänge](../content/Tracing-Driver-Operation.md)\) aktualisiert, damit Clientereignisse einfacher mit Diagnoseinformationen \(z. B. Verbindungsfehlern\) aus dem Konnektivitätsringpuffer des Servers und den anwendungsbezogenen Leistungsinformationen in den erweiterten Ereignisprotokollen korreliert werden können. Informationen zum Auswerten der erweiterten Ereignisprotokolle finden Sie unter [Anzeigen von Ereignissitzungsdaten](http://msdn.microsoft.com/library/hh710068(SQL.110).aspx).  
  
## Details  
 Bei Verbindungsvorgängen sendet [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] eine Clientverbindungs\-ID. Wenn die Verbindung nicht hergestellt werden kann, können Sie auf den Konnektivitätsringpuffer zugreifen \([Behandlung von Konnektivitätsproblemen in SQL Server 2008 mit dem Konnektivitätsringpuffer](http://go.microsoft.com/fwlink/?LinkId=207752)\), das Feld **ClientConnectionID** suchen und Diagnoseinformationen zum Verbindungsfehler abrufen. Clientverbindungs\-IDs werden nur im Ringpuffer protokolliert, wenn ein Fehler auftritt. \(Wenn vor dem Senden des prelogin\-Pakets keine Verbindung hergestellt werden kann, wird keine Clientverbindungs\-ID generiert.\) Die Clientverbindungs\-ID ist eine 16\-Byte\-GUID. Sie können die Clientverbindungs\-ID auch in der Zielausgabe der erweiterten Ereignisse suchen, wenn die **client\_connection\_id**\-Aktion Ereignissen in einer erweiterten Ereignissitzung hinzugefügt wird. Wenn Sie weitere Unterstützung zur Clienttreiberdiagnose benötigen, können Sie die Ablaufverfolgung aktivieren und den Verbindungsbefehl erneut ausführen. Beobachten Sie dabei das Feld **ClientConnectionID** in der Ablaufverfolgung.  
  
 Sie können die Clientverbindungs\-ID programmgesteuert über [ISQLServerConnection-Schnittstelle](../content/ISQLServerConnection-Interface.md) abrufen. Die Verbindungs\-ID ist auch in verbindungsbezogenen Ausnahmen enthalten.  
  
 Bei einem Verbindungsfehler kann die Clientverbindungs\-ID in den BID\-Ablaufverfolgungsinformationen des Servers und im Konnektivitätsringpuffer nützlich sein, um die Clientverbindungen mit Verbindungen auf dem Server zu korrelieren. Weitere Informationen zur BID\-Ablaufverfolgung auf dem Server finden Sie unter [Data Access Tracing](http://go.microsoft.com/fwlink/?LinkId=125805). Der Artikel zur Datenzugriffsablaufverfolgung enthält auch Informationen zum Ausführen einer Datenzugriffsablaufverfolgung, die sich nicht auf [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] bezieht. Informationen zum Ausführen einer Datenzugriffsablaufverfolgung unter Verwendung von [Ablaufverfolgung für Treibervorgänge](../content/Tracing-Driver-Operation.md) finden Sie unter [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)].  
  
 Der JDBC\-Treiber sendet außerdem eine threadspezifische Aktivitäts\-ID. Die Aktivitäts\-ID wird in den Sitzungen für erweiterte Ereignisse aufgezeichnet, wenn die Sitzungen bei aktivierter TRACK\_CAUSAILITY\-Option gestartet werden. Bei Leistungsproblemen mit einer aktiven Verbindung können Sie die Aktivitäts\-ID aus der Ablaufverfolgung des Clients \(Feld „ActivityID“\) abrufen und dann in der Ausgabe der erweiterten Ereignisse nach der Aktivitäts\-ID suchen. Die Aktivitäts\-ID in erweiterten Ereignissen ist eine 16\-Byte\-GUID \(entspricht nicht der GUID für die Clientverbindungs\-ID\), an die eine 4\-Byte\-Sequenznummer angehängt ist. Die Sequenznummer stellt die Reihenfolge einer Anforderung in einem Thread dar. Die ActivityId wird bei SQL\-Stapelanweisungen und RPC\-Anforderungen gesendet. Zum Aktivieren des Sendens der ActivityId an den Server müssen Sie zunächst das folgende Schlüssel\-Wert\-Par in der Datei „Logging.Properties“ angeben:  
  
```  
com.microsoft.sqlserver.jdbc.traceactivity = on  
```  
  
 Jeder andere Wert als `on` \(Groß\-\/Kleinschreibung beachten\) deaktiviert das Senden der ActivityId.  
  
 Weitere Informationen finden Sie unter [Ablaufverfolgung für Treibervorgänge](../content/Tracing-Driver-Operation.md). Dieses Ablaufverfolgungsflag wird mit den entsprechenden JDBC\-Objektprotokollierungen verwendet, um zu bestimmen, ob im JDBC\-Treiber eine Ablaufverfolgung der ActivityId ausgeführt und diese gesendet werden soll. Zusätzlich zum Aktualisieren der Datei „Logging.Properties“ muss die Protokollierung „com.microsoft.sqlserver.jdbc“ mit dem Wert FINER oder höher aktiviert werden. Wenn die ActivityId bei Anforderungen an eine bestimmte Klasse an den Server gesendet werden soll, muss die entsprechende Klassenprotokollierung mit dem Wert FINER oder FINEST aktiviert werden. Wenn die Klasse beispielsweise SQLServerStatement lautet, aktivieren Sie die Protokollierung „com.microsoft.sqlserver.jdbc.SQLServerStatement“.  
  
 Im folgenden Beispiel wird [!INCLUDE[tsql](../content/includes/tsql_md.md)] verwendet, um eine erweiterte Ereignissitzung zu starten, die in einem Ringpuffer gespeichert wird und die von einem Client bei RPC\- und Stapelvorgängen gesendete Aktivitäts\-ID aufzeichnet:  
  
```  
create event session MySession on server  
add event connectivity_ring_buffer_recorded,  
add event sql_statement_starting (action (client_connection_id)),  
add event sql_statement_completed (action (client_connection_id)),  
add event rpc_starting (action (client_connection_id)),  
add event rpc_completed (action (client_connection_id))  
add target ring_buffer with (track_causality=on)  
```  
  
## Siehe auch  
 [Diagnostizieren von Problemen mit dem JDBC-Treiber](../content/Diagnosing-Problems-with-the-JDBC-Driver.md)  
  
  