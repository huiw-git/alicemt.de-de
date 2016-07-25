---
title: "Verwalten von Resultsets mit dem JDBC-Treiber"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9ed5ad41-22e0-4e4a-8a79-10512db60d50
caps.latest.revision: 18
caps.handback.revision: 16
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
# Verwalten von Resultsets mit dem JDBC-Treiber
  Beim Resultset handelt es sich um ein Objekt, das die von einer Datenquelle zurückgegebenen Daten darstellt \(normalerweise als Ergebnis einer Abfrage\). Das Resultset enthält Zeilen und Spalten, die die angeforderten Datenelemente enthalten. Die Navigation erfolgt über einen Cursor. Ein Resultset kann aktualisiert werden, d. h., es besteht die Möglichkeit das Resultset zu ändern und diese Änderungen an die ursprüngliche Datenquelle zu übergeben. Ein Resultset kann auch unterschiedlich sensitiv gegenüber Änderungen in der zugrunde liegenden Datenquelle sein.  
  
 Der Typ des Resultset wird beim Erstellen der Anweisung bestimmt, d. h., wenn die [createStatement](../content/createStatement-Method--SQLServerConnection-.md)\-Methode der [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Klasse aufgerufen wird. Die grundlegende Aufgabe eines Resultsets besteht darin, Java\-Anwendungen eine nutzbare Darstellung der Datenbankdaten bereitzustellen. Dies erfolgt normalerweise mit den typisierten Abruf\- und Festlegungsmethoden der Datenelemente des Resultset.  
  
 Im folgenden Beispiel, das auf der [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)][!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank basiert, wird durch Aufrufen der [executeQuery](../content/executeQuery-Method--SQLServerStatement-.md)\-Methode der [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Klasse ein Resultset erstellt. Die Daten des Resultset werden anschließend mit der [getString](../content/getString-Method--SQLServerResultSet-.md)\-Methode der [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Klasse angezeigt.  
  
 [!CODE [JDBC#ManagingResultSets1](../CodeSnippet/SQLDrivers/jdbc#managingresultsets1)]  
  
 Die Themen in diesem Abschnitt beschreiben verschiedene Aspekte der Verwendung von Resultsets wie Cursortypen, Gleichzeitigkeit und Zeilensperren.  
  
## In diesem Abschnitt  
  
|Thema|Beschreibung|  
|-----------|------------------|  
|[Grundlegendes zu Cursortypen](../content/Understanding-Cursor-Types.md)|Beschreibt die verschiedenen Cursortypen, die von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] unterstützt werden.|  
|[Grundlegendes zur Parallelitätssteuerung](../content/Understanding-Concurrency-Control.md)|Beschreibt, wie der JDBC\-Treiber die Parallelitätssteuerung unterstützt.|  
|[Grundlegendes zu Zeilensperren](../content/Understanding-Row-Locking.md)|Beschreibt, wie der JDBC\-Treiber Zeilensperren unterstützt.|  
  
## Siehe auch  
 [Übersicht über den JDBC-Treiber](../content/Overview-of-the-JDBC-Driver.md)  
  
  