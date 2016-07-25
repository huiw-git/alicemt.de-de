---
title: "Funktionen von Microsoft ODBC Driver for SQL Server on Windows"
ms.custom: na
ms.date: 06/16/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 76326eeb-1144-4b9f-85db-50524c655d30
caps.latest.revision: 21
caps.handback.revision: 18
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
  - zh-cn
  - zh-tw
---
# Funktionen von Microsoft ODBC Driver for SQL Server on Windows
    
## Microsoft ODBC Driver 13 \(Preview\) for SQL Server on Windows  
 Der ODBC-Treiber 13 \(Preview\) for SQL Server enthält alle Funktionen der früheren Version \(11\) und bietet Unterstützung für das Datenbankmodul „Immer verschlüsselt“, ein neues Feature in Microsoft SQL Server 2016 \(Preview\).  
  
 „Immer verschlüsselt“ ermöglicht es Clients, sensible Daten in Clientanwendungen zu verschlüsseln und die Verschlüsselungsschlüssel niemals an SQL Server weiterzugeben. Ein auf dem Clientcomputer installierter Treiber, bei dem „Immer verschlüsselt“ aktiviert ist, erreicht dies durch die automatische Ver- und Entschlüsselung von sensiblen Daten in der SQL Server-Clientanwendung. Der Treiber verschlüsselt die Daten in vertraulichen Spalten, bevor er sie an SQL Server weitergibt, und schreibt Abfragen automatisch neu, sodass die Semantik der Anwendung beibehalten wird. Auf ähnliche Weise entschlüsselt der Treiber transparent Daten in verschlüsselten Datenbankspalten, die in Abfrageergebnissen enthalten sind. Weitere Informationen finden Sie unter [Using Always Encrypted with the Windows ODBC Driver](../content/Using-Always-Encrypted-with-the-Windows-ODBC-Driver.md).  
  
## Microsoft ODBC Driver 11 für SQL Server unter Windows  
 Der ODBC-Treiber für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] enthält die gesamte Funktionalität des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Native Client ODBC-Treibers, der im Lieferumfang von [!INCLUDE[ssSQL11](../content/includes/ssSQL11_md.md)]enthalten ist. Weitere Informationen finden Sie unter [SQL Server Native Client-Programmierung](http://msdn.microsoft.com/library/ms130892.aspx). Der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Native Client ODBC-Treiber basiert auf dem ODBC-Treiber, der im Lieferumfang des Betriebssystems von Windows enthalten ist. Weitere Informationen finden Sie unter [Windows Data Access Components SDK](http://msdn.microsoft.com/library/aa968814(VS.85).aspx).  
  
 Diese Version des ODBC-Treibers für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] enthält die folgenden neuen Features:  
  
 Die Option „–l“, die ein Anmeldungstimeout angibt, wurde „BCP.exe“ hinzugefügt.  
 Die Option „–I“ gibt an, wie viele Sekunden bei der Herstellung einer Verbindung mit einem Server verstreichen dürfen, bevor für eine Bcp.exe-Anmeldung bei [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ein Timeout eintritt. Das Standardtimeout für „Bcp.exe“ für die Anmeldung bei [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] beträgt 15 Sekunden. Der Timeoutwert für den Anmeldungszeitraum muss eine Zahl zwischen 0 und 65534 sein. Wenn der angegebene Wert kein numerischer Wert ist oder außerhalb dieses Bereichs liegt, generiert Bcp.exe eine Fehlermeldung. Mit dem Wert 0 wird eine unbegrenzte Wartezeit festgelegt.  
  
 Ein Anmeldungstimeout von weniger als \(circa\) 10 Sekunden ist nicht zuverlässig.  
  
 Treiberfähiges Verbindungspooling  
 Der ODBC-Treiber für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] unterstützt [Treiberfähiges Verbindungspooling](http://msdn.microsoft.com/library/hh405031(VS.85).aspx). Weitere Informationen finden Sie unter [Driver-Aware Connection Pooling in the ODBC Driver for SQL Server](../content/Driver-Aware-Connection-Pooling-in-the-ODBC-Driver-for-SQL-Server.md).  
  
 Asynchrone Ausführung \(Benachrichtigungsmethode\)  
 Der ODBC-Treiber für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] unterstützt [Asynchrone Ausführung \(Benachrichtigungsmethode\)](http://msdn.microsoft.com/library/hh405038(VS.85).aspx). Ein Verwendungsbeispiel finden Sie unter [Beispiel für asynchrone Ausführung &#40;Benachrichtigungsmethode&#41;](../content/Asynchronous-Execution--Notification-Method--Sample.md)  
  
 Verbindungsstabilität  
 Um sicherzustellen, dass die Anwendungen mit einer Microsoft Azure SQL-Datenbank verbunden sind, kann der ODBC-Treiber unter Windows Verbindungen im Leerlauf wiederherstellen. Weitere Informationen finden Sie unter [Connection Resiliency in the Windows ODBC Driver](../content/Connection-Resiliency-in-the-Windows-ODBC-Driver.md).  
  
## Verhaltensänderungen  
 In [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)], bewirkt die **\-y0**-Option für Sqlcmd.exe, dass die Ausgabe bei 1 MB abgeschnitten wird, wenn display\_width bei 0 lag.  
  
 Beginnend mit dem ODBC-Treiber 11 für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)], gibt es keine Beschränkung für die Menge der Daten, die in einer einzelnen Spalte abgerufen werden, wenn **– y0** angegeben ist. Sqlcmd.exe streamt jetzt Spalten bis zu 2 GB \([!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Datentyp-Maximum\).  
  
 Ein weiterer Unterschied ist, dass eine Kombination aus **\-h \-y0** nun einen Fehler erzeugt, der meldet, dass die Optionen inkompatibel sind. **\-h**, was die Anzahl der Zeilen angibt, die zwischen den Spaltenüberschriften gedruckt werden sollen, war noch nie mit **\-y0** kompatibel und wurde ignoriert , obwohl keine Überschriften gedruckt wurden.  
  
 **\-y0** kann je nach Größe der zurückgegebene Daten zu Leistungsproblemen auf dem Server und im Netzwerk führen.  
  
## Siehe auch  
 [Microsoft ODBC Driver for SQL Server on Windows](../content/Microsoft-ODBC-Driver-for-SQL-Server-on-Windows.md)  
  
  