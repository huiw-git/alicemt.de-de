---
title: "Verarbeiten von Metadaten mit dem JDBC-Treiber"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5cfb35d4-ddcd-40a2-8091-f29cddc32552
caps.latest.revision: 12
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
# Verarbeiten von Metadaten mit dem JDBC-Treiber
  [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] bietet verschiedene Möglichkeiten zum Verarbeiten von Metadaten in einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank. Mit dem JDBC\-Treiber können Metadaten zur Datenbank, zu einem Resultset oder zu Parametern abgerufen werden.  
  
 Der JDBC\-Treiber umfasst drei Klassen zum Abrufen von Metadaten aus einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank:  
  
-   [SQLServerDatabaseMetaData](../content/SQLServerDatabaseMetaData-Class.md) gibt Informationen über die zurzeit verbundene Datenbank zurück.  
  
-   [SQLServerResultSetMetaData](../content/SQLServerResultSetMetaData-Class.md) gibt Informationen über das Resultset zurück.  
  
-   [SQLServerParameterMetaData](../content/SQLServerParameterMetaData-Class.md) gibt Informationen über die Parameter vorbereiteter und aufrufbarer Anweisungen zurück.  
  
 Die Themen in diesem Abschnitt beschreiben, wie Sie mit den drei Metadatenklassen Metadaten in einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank verarbeiten können.  
  
> [!NOTE]  
>  Die in diesem Abschnitt behandelten Metadatenmethoden wirken sich im Allgemeinen erheblich auf die Leistung der Anwendung aus, sodass deren Verwendung sorgfältig abgewägt werden muss.  
  
## In diesem Abschnitt  
  
|Thema|Beschreibung|  
|-----------|------------------|  
|[Verwenden von Datenbankmetadaten](../content/Using-Database-Metadata.md)|Beschreibt das Abrufen von Metadateninformationen über die zurzeit verbundene Datenbank.|  
|[Verwenden von Resultsetmetadaten](../content/Using-Result-Set-Metadata.md)|Beschreibt das Abrufen von Metadateninformationen über das aktuelle Resultset.|  
|[Verwenden von Parametermetadaten](../content/Using-Parameter-Metadata.md)|Beschreibt das Abrufen von Metadateninformationen über die Parameter vorbereiteter und aufrufbarer Anweisungen.|  
  
## Siehe auch  
 [Übersicht über den JDBC-Treiber](../content/Overview-of-the-JDBC-Driver.md)  
  
  