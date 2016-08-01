---
title: "Verwenden von Datenbankmetadaten"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8b048371-e912-4ed1-afd7-436978f48888
caps.latest.revision: 13
caps.handback.revision: 11
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
# Verwenden von Datenbankmetadaten
  Zum Abfragen einer Datenbank nach Informationen zu den unterstützten Funktionen ist in [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] die [SQLServerDatabaseMetaData](../content/SQLServerDatabaseMetaData-Class.md)\-Klasse implementiert. Diese Klasse enthält eine Vielzahl von Methoden, die Informationen in der Form eines einzelnen Werts oder als Resultset zurückgeben.  
  
 Um ein SQLServerDatabaseMetaData\-Objekt zu erstellen, können Sie mit der [getMetaData](../content/getMetaData-Method--SQLServerConnection-.md)\-Methode der [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Klasse Informationen über die verbundene Datenbank abrufen.  
  
 Im folgenden Beispiel werden eine offene Verbindung zur [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)][!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank an die Funktion übergeben, mit der getMetaData\-Methode der SQLServerConnection\-Klasse ein SQLServerDatabaseMetadata\-Objekt zurückgegeben und dann mit den verschiedenen Methoden des SQLServerDatabaseMetaData\-Objekts Informationen zu Treiber, Treiberversion, Datenbankname und Datenbankversion angezeigt.  
  
 [!CODE [JDBC#UsingDBMetaData1](../CodeSnippet/SQLDrivers/jdbc#usingdbmetadata1)]  
  
## Siehe auch  
 [Verarbeiten von Metadaten mit dem JDBC-Treiber](../content/Handling-Metadata-with-the-JDBC-Driver.md)  
  
  