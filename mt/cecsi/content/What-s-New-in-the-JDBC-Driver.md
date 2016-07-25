---
title: "Neues im JDBC-Treiber"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 074f211e-984a-4b76-bb15-ee36f5946f12
caps.latest.revision: 206
caps.handback.revision: 196
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
# Neues im JDBC-Treiber
    
## Updates in Microsoft JDBC Driver 6.0 \(Vorschau\) für SQL Server  
 **Always Encrypted**  
  
 Unterstützung für das kürzlich vorgestellte Always Encrypted\-Feature in SQL Server 2016 \(Vorschau\), ein neues Sicherheitsfeature, das sicherstellt, dass sensible Daten in einer SQL Server\-Instanz zu keiner Zeit im Klartext sichtbar sind. Always Encrypted arbeitet mit transparenter Verschlüsselung der Daten in der Anwendung, sodass SQL Server nur die verschlüsselten Daten verarbeitet, aber keine Klartextwerte. Selbst, wenn die Integrität der SQL\-Instanz oder des Hostcomputers beschädigt ist, kann ein Angreifer sensible Daten nur als chiffrierten Text sehen. Einzelheiten finden Sie unter [Verwenden von „Immer verschlüsselt“ mit dem JDBC-Treiber](../content/Using-Always-Encrypted-with-the-JDBC-Driver.md).  
  
 **Internationaler Domänenname \(IDN\)**  
  
 Unterstützung für internationale Domänennamen \(IDNs\) bei Servernamen. Details finden Sie unter „Verwendung von internationalen Domänennamen“ auf der Seite [Internationale Funktionen des JDBC-Treibers](../content/International-Features-of-the-JDBC-Driver.md).  
  
 **Parametrisierte Abfrage**  
  
 Jetzt wird das Abrufen von Parametermetadaten mit vorbereiteten Anweisungen für komplexe Abfragen unterstützt, wie etwa Teilabfragen und\/oder Joins. Beachten Sie, dass diese Verbesserung nur bei Verwendung von SQL Server 2012 und neueren Versionen verfügbar ist.  
  
## Updates in Microsoft JDBC Driver 4.2 für SQL Server und höheren Versionen  
 **Unterstützung für JDK 8**  
  
 Unterstützung für Java Development Kit \(JDK\), Version 8.0, zusätzlich zu JDK 7.0, 6.0 und 5.0.  
  
 **JDBC 4.1\- und 4.2\-Kompatibilität**  
  
 Unterstützung für die Java Database Connectivity\-API\-Spezifikationen 4.1 und 4.2, zusätzlich zu 4.0. Detaillierte Informationen zu diesem Thema finden Sie unter [JDBC 4.1-Kompatibilität für den JDBC-Treiber](../content/JDBC-4.1-Compliance-for-the-JDBC-Driver.md) und [JDBC 4.2-Kompatibilität für den JDBC-Treiber](../content/JDBC-4.2-Compliance-for-the-JDBC-Driver.md).  
  
 **Massenkopieren**  
  
 Die Massenkopierfunktion wird verwendet, um schnell große Datenmengen in Tabellen oder Ansichten in SQL Server\-Datenbanken zu kopieren. Einzelheiten finden Sie unter [Verwenden von Massenkopieren mit dem JDBC Driver](../content/Using-Bulk-Copy-with-the-JDBC-Driver.md).  
  
 **Rollbackoption für XA\-Transaktionen**  
  
 Es wurden neue Timeoutoptionen für das vorhandene automatische Rollback nicht vorbereiteter Transaktionen hinzugefügt. Einzelheiten dazu finden Sie unter [Grundlegendes zu XA-Transaktionen](../content/Understanding-XA-Transactions.md).  
  
 **Neue Kerberos\-Prinzipalverbindungseigenschaft**  
  
 Es wurde eine neue Verbindungseigenschaft hinzugefügt, um mehr Flexibilität für Kerberos\-Verbindungen zu ermöglichen. Einzelheiten dazu finden Sie unter [Herstellen von Verbindungen mit SQL Server mit der integrierten Kerberos-Authentifizierung](../content/Using-Kerberos-Integrated-Authentication-to-Connect-to-SQL-Server.md).  
  
## Updates in Microsoft JDBC Driver 4.1 für SQL Server und höheren Versionen  
 **Unterstützung für JDK 7**  
  
 Unterstützung für Java Development Kit \(JDK\), Version 7.0, zusätzlich zu JDK 6.0 und 5.0.  
  
## Updates in Microsoft JDBC Driver 4.0 für SQL Server und höheren Versionen  
 **Informationen zum Herstellen von Verbindungen mit einer Azure SQL\-Datenbank**  
  
 Jetzt ist ein Thema mit Informationen zum Herstellen von Verbindungen mit einer Azure SQL\-Datenbank verfügbar. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit einer Azure SQL-Datenbank](../content/Connecting-to-an-Azure-SQL-database.md).  
  
 **Unterstützung für hohe Verfügbarkeit bei Notfallwiederherstellung**  
  
 Unterstützung für hoch verfügbare Verbindungen zur Notfallwiederherstellung bei AlwaysOn\-Verfügbarkeitsgruppen in [!INCLUDE[ssSQL11](../content/includes/ssSQL11_md.md)]. Weitere Informationen finden Sie unter [JDBC Driver-Unterstützung für hohe Verfügbarkeit, Notfallwiederherstellung](../content/JDBC-Driver-Support-for-High-Availability--Disaster-Recovery.md).  
  
 **Verwenden der integrierten Kerberos\-Authentifizierung für Verbindungen mit SQL Server**  
  
 Unterstützung für die integrierte Kerberos\-Authentifizierung vom Typ 4 für Verbindungen von Anwendungen mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank. Weitere Informationen finden Sie unter [Herstellen von Verbindungen mit SQL Server mit der integrierten Kerberos-Authentifizierung](../content/Using-Kerberos-Integrated-Authentication-to-Connect-to-SQL-Server.md). \(Integrierte Kerberos\-Authentifizierung vom Typ 2 ist in [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-Versionen vor 4.0 verfügbar.\)  
  
 **Zugreifen auf Diagnoseinformationen im Protokoll der erweiterten Ereignisse**  
  
 Sie können auf die Informationen in den erweiterten Ereignisprotokollen des Servers zugreifen, um die Ursachen von Verbindungsfehlern zu bestimmen. Weitere Informationen finden Sie unter [Zugreifen auf Diagnoseinformationen im Protokoll der erweiterten Ereignisse](../content/Accessing-Diagnostic-Information-in-the-Extended-Events-Log.md).  
  
 **Zusätzliche Unterstützung für Spalten mit geringer Dichte**  
  
 Wenn Ihre Anwendung bereits auf Daten in einer Tabelle zugreift, die Daten mit geringer Dichte verwendet, sollten Sie einen Leistungszuwachs feststellen können. Informationen zu Spalten \(einschließlich Spalten mit geringer Dichte\) erhalten Sie bei [getColumns-Methode &#40;SQLServerDatabaseMetaData&#41;](../content/getColumns-Method--SQLServerDatabaseMetaData-.md). Weitere Informationen zu [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Spalten mit geringer Dichte finden Sie unter [Verwenden von Spalten mit geringer Dichte](http://go.microsoft.com/fwlink/?LinkId=224244).  
  
 **Xid.getFormatId**  
  
 Seit der Version [!INCLUDE[jdbc_40](../content/includes/jdbc_40_md.md)] übergibt der JDBC\-Treiber den Formatbezeichner von der Anwendung an den Datenbankserver. Um das aktualisierte Verhalten nutzen zu können, stellen Sie sicher, dass ein Update von „sqljdbc\_xa.dll“ auf dem Server ausgeführt wird. Weitere Informationen zum Kopieren einer aktualisierten Version von „sqljdbc\_xa.dll“ auf den Server finden Sie unter [Grundlegendes zu XA-Transaktionen](../content/Understanding-XA-Transactions.md).  
  
## Keine Itanium\-Unterstützung für Anwendungen, die JDBC Driver 6.0 \(Vorschau\) sowie und 4.2, 4.1 und 4.0 nutzen  
  
 Anwendungen, die Microsoft JDBC Driver 6.0 \(Vorschau\) sowie 4.2, 4.1 und 4.0 für SQL Server nutzen, werden auf Itanium\-Computern nicht unterstützt.  
  
## Siehe auch  
 [Übersicht über den JDBC-Treiber](../content/Overview-of-the-JDBC-Driver.md)  
  
  