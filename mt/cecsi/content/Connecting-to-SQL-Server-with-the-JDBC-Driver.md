---
title: "Verbinden von SQL Server mit dem JDBC-Treiber"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 94bcfbe3-f00e-4774-bda8-bb7577518fec
caps.latest.revision: 30
caps.handback.revision: 28
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
# Verbinden von SQL Server mit dem JDBC-Treiber
  Eine der grundlegenden Aufgaben, die mit [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] ausgeführt werden, ist das Herstellen einer Verbindung mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank. Die gesamte Interaktion mit der Datenbank erfolgt über das [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt. Da der JDBC\-Treiber eine extrem flache Architektur aufweist, beziehen sich nahezu alle wesentlichen Verhalten auf das SQLServerConnection\-Objekt.  
  
 Wenn [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] nur einen IPv6\-Port überwacht, legen Sie die Systemeigenschaft "java.net.preferIPv6Addresses" fest, um sicherzustellen, dass für die Verbindung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] IPv6 statt IPv4 verwendet wird:  
  
```  
System.setProperty("java.net.preferIPv6Addresses", "true");  
```  
  
 Die Themen in diesem Abschnitt beschreiben, wie Sie Verbindungen mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank herstellen und verwalten.  
  
## In diesem Abschnitt  
  
|Thema|Beschreibung|  
|-----------|------------------|  
|[Erstellen der Verbindungs-URL](../content/Building-the-Connection-URL.md)|Beschreibt das Erstellen einer Verbindungs\-URL für Verbindungen zu einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank. Darüber hinaus wird das Herstellen einer Verbindung zu benannten Instanzen einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank beschrieben.|  
|[Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md)|Beschreibt die verschiedenen Verbindungseigenschaften und deren Verwendung für Verbindungen mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank.|  
|[Festlegen von Datenquelleneigenschaften](../content/Setting-the-Data-Source-Properties.md)|Beschreibt die Verwendung von Datenquellen auf einer Java\-Plattform, Enterprise Edition \(Java EE\).|  
|[Arbeiten mit einer Verbindung](../content/Working-with-a-Connection.md)|Beschreibt die verschiedenen Möglichkeiten, um die Instanz einer Verbindung mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank zu erstellen.|  
|[Verwenden von Verbindungspools](../content/Using-Connection-Pooling.md)|Beschreibt die Unterstützung von Verbindungspools durch den JDBC\-Treiber.|  
|[Verwenden der Datenbankspiegelung &#40;JDBC&#41;](../content/Using-Database-Mirroring--JDBC-.md)|Beschreibt die Unterstützung der Datenbankspiegelung durch den JDBC\-Treiber.|  
|[JDBC Driver-Unterstützung für hohe Verfügbarkeit, Notfallwiederherstellung](../content/JDBC-Driver-Support-for-High-Availability--Disaster-Recovery.md)|Beschreibt das Entwickeln einer Anwendung, die eine Verbindung mit einer AlwaysOn\-Verfügbarkeitsgruppe herstellt.|  
|[Herstellen von Verbindungen mit SQL Server mit der integrierten Kerberos-Authentifizierung](../content/Using-Kerberos-Integrated-Authentication-to-Connect-to-SQL-Server.md)|Erläutert eine Java\-Implementierung für Anwendungen zum Herstellen von Verbindungen mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank mit integrierter Kerberos\-Authentifizierung.|  
|[Herstellen einer Verbindung mit einer Azure SQL-Datenbank](../content/Connecting-to-an-Azure-SQL-database.md)|Erläutert Verbindungsprobleme für Datenbanken in SQL Azure.|  
  
## Siehe auch  
 [Übersicht über den JDBC-Treiber](../content/Overview-of-the-JDBC-Driver.md)  
  
  