---
title: "SQLServerXADataSource-Klasse"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 95fc7b07-2498-4a7e-8f7f-ee0d86b598b4
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
# SQLServerXADataSource-Klasse
  Stellt eine intern verwendete Factory für [SQLServerXAConnection](../content/SQLServerXAConnection-Class.md)\-Objekte dar.  
  
 **Paket:** com.microsoft.sqlserver.jdbc  
  
 **Erweitert:** [SQLServerConnectionPoolDataSource](../content/SQLServerConnectionPoolDataSource-Class.md)  
  
 **Implementiert:** javax.sql.XADataSource  
  
## Syntax  
  
```  
  
public class SQLServerXADataSource  
```  
  
## Hinweise  
 Ein Objekt, von dem die SQLServerXADataSource\-Schnittstelle implementiert wird, ist normalerweise bei einem Bezeichnungsdienst registriert, der das JNDI \(Java Naming and Directory Interface\) verwendet.  
  
 Die SQLServerXADataSource\-Klasse stellt Datenbankverbindungen zur Verwendung in verteilten \(XA\) Transaktionen bereit. Die SQLServerXADataSource\-Klasse unterstützt außerdem Verbindungspools aus physikalischen Verbindungen. Die SQLServerXADataSource\- und SQLServerXAConnection\-Schnittstellen, die im Paket "javax.sql" definiert sind, wurden von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] implementiert.  
  
 Ein SQLServerXAConnection\-Objekt ist eine Poolverbindung, die für eine verteilte Transaktion verwendet werden können. Genauer gesagt wird von SQLServerXAConnection die SQLServerPooledConnection\-Schnittstelle durch Hinzufügen der [getXAResource](../content/getXAResource-Method--SQLServerXAConnection-.md)\-Methode erweitert. Von dieser Methode wird ein [SQLServerXAResource](../content/SQLServerXAResource-Class.md)\-Objekt erzeugt, das von einem Transaktions\-Manager zur Koordination der Arbeit an dieser Verbindung mit den anderen an der verteilten Transaktion Beteiligten verwendet werden kann. Da durch sie die SQLServerPooledConnection\-Schnittstelle erweitert wird, werden von SQLServerXAConnection\-Objekten alle Methoden der SQLServerPooledConnection\-Objekte unterstützt. Sie sind wiederverwendbare physikalische Verbindungen mit einer zu Grunde liegenden Datenquelle und erzeugen logische Verbindungshandles, die an eine JDBC\-Anwendung zurückgegeben werden können.  
  
 SQLServerXAConnection\-Objekte werden von einem SQLServerXADataSource\-Objekt erzeugt.SQLServerConnectionPoolDataSource\-Objekte und SQLServerXADataSource\-Objekte sind ähnlich, da sie beide unterhalb einer Datenquellenebene implementiert sind, die für die JDBC\-Anwendung sichtbar ist. Dank dieser Architektur kann [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verteilte Transaktionen auf eine Weise unterstützen, die für die Anwendung transparent ist.SQLServerXADataSource kann für die Integration mit [!INCLUDE[msCoName](../content/includes/msCoName_md.md)]\-DTC \(Distributed Transaction Coordinator\) konfiguriert werden, um echte verteilte Transaktionsverarbeitung zu ermöglichen.  
  
## Siehe auch  
 [SQLServerXADataSource-Elemente](../content/SQLServerXADataSource-Members.md)   
 [API-Referenz für den JDBC-Treiber](../content/JDBC-Driver-API-Reference.md)  
  
  