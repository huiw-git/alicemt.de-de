---
title: "Festlegen von Datenquelleneigenschaften"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f3363d05-07fc-4bf8-ae5e-2a7a968808ad
caps.latest.revision: 20
caps.handback.revision: 19
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
# Festlegen von Datenquelleneigenschaften
  Datenquellen bilden den bevorzugten Mechanismus, mit dem in einer Umgebung der Java\-Plattform, Enterprise Edition \(Java EE\) JDBC\-Verbindungen erstellt werden. Datenquellen ermöglichen Verbindungen, Poolverbindungen und verteilte Verbindungen, ohne die Verbindungseigenschaften fest im Java\-Code codieren zu müssen. Alle Datenquellen für [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] können alle Eigenschaften mit den entsprechenden Abruf\- oder Festlegungsmethoden abrufen bzw. festlegen.  
  
 Java EE\-Produkte wie Anwendungsserver und Servlet\-\/JSP\-Module lassen normalerweise die Konfiguration von Datenquellen für den Datenbankzugriff zu. Alle im Thema [Festlegen von Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md) aufgeführten Eigenschaften können überall angegeben werden, wo die Konfiguration die Eingabe einer Eigenschaft als Eigenschaft\=Wert\-Paar zulässt.  
  
 Weitere Informationen zu [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenquellen finden Sie unter der [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Klasse. Ein Beispiel für die Verwendung der SQLServerDataSource\-Klasse zum Herstellen einer Verbindung mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank finden Sie unter [Beispiel für Datenquellen](../content/Data-Source-Sample.md).  
  
## Siehe auch  
 [Verbinden von SQL Server mit dem JDBC-Treiber](../content/Connecting-to-SQL-Server-with-the-JDBC-Driver.md)  
  
  