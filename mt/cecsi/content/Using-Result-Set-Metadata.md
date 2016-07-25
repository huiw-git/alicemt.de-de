---
title: "Verwenden von Resultsetmetadaten"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5e37529a-30db-48c8-b90a-ae9657d0f6b0
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
# Verwenden von Resultsetmetadaten
  Zum Abfragen eines Resultsets nach Informationen zu den enthaltenen Spalten ist in [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] die [SQLServerResultSetMetaData](../content/SQLServerResultSetMetaData-Class.md)\-Klasse implementiert. Diese Klasse enthält eine Vielzahl von Methoden, die Informationen in der Form eines einzelnen Werts zurückgeben.  
  
 Mit der [getMetaData](../content/getMetaData-Method--SQLServerResultSet-.md)\-Methode der [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Klasse können Sie ein SQLServerResultSetMetaData\-Objekt erstellen.  
  
 Im folgenden Beispiel werden eine offene Verbindung zur [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)][!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank an die Funktion übergeben, mit der getMetaData\-Methode der SQLServerResultSet\-Klasse ein SQLServerResultSetMetaData\-Objekt zurückgegeben und dann mit den verschiedenen Methoden des SQLServerResultSetMetaData\-Objekts Informationen zu Namen und Datentyp der im Resultset enthaltenen Spalten angezeigt.  
  
 [!CODE [JDBC#UsingResultSetMetaData1](../CodeSnippet/SQLDrivers/jdbc#usingresultsetmetadata1)]  
  
## Siehe auch  
 [Verarbeiten von Metadaten mit dem JDBC-Treiber](../content/Handling-Metadata-with-the-JDBC-Driver.md)  
  
  