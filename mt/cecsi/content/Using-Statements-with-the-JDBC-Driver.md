---
title: "Verwenden von Anweisungen mit dem JDBC-Treiber"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7f8f3e8f-841e-4449-9154-b5366870121f
caps.latest.revision: 13
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
# Verwenden von Anweisungen mit dem JDBC-Treiber
  [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] bietet verschiedene Möglichkeiten, um Daten in einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank zu verarbeiten. Mit dem JDBC\-Treiber können SQL\-Anweisungen für die Datenbank ausgeführt oder gespeicherte Prozeduren in der Datenbank aufgerufen werden, die sowohl Eingabe\- als Ausgabeparameter verwenden. Der JDBC\-Treiber unterstützt außerdem die Verwendung von SQL\-Escapesequenzen, Updatezählungen, automatisch generierten Schlüsseln und die Ausführung von Updates in einer Batchoperation.  
  
 Der JDBC\-Treiber umfasst drei Klassen zum Abrufen von Daten aus einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank:  
  
1.  [SQLServerStatement](../content/SQLServerStatement-Class.md): Ausführen von SQL\-Anweisungen ohne Parameter.  
  
2.  [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md): Ausführen von kompilierten SQL\-Anweisungen, die IN\-Parameter enthalten können \(geerbt von SQLServerStatement\).  
  
3.  [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md): Ausführen von gespeicherten Prozeduren, die IN\-Parameter und\/oder OUT\-Parameter enthalten können \(geerbt von SQLServerPreparedStatement\).  
  
 Die Themen in diesem Abschnitt beschreiben, wie Sie mit den drei Anweisungsklassen Daten in einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank verarbeiten können.  
  
## In diesem Abschnitt  
  
|Thema|Beschreibung|  
|-----------|------------------|  
|[Verwenden von Anweisungen mit SQL](../content/Using-Statements-with-SQL.md)|Beschreibt die Verwendung von SQL\-Anweisungen mit dem JDBC\-Treiber, um Daten in einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank zu verarbeiten.|  
|[Verwenden von Anweisungen mit gespeicherten Prozeduren](../content/Using-Statements-with-Stored-Procedures.md)|Beschreibt die Verwendung von gespeicherten Prozeduren mit dem JDBC\-Treiber, um Daten in einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank zu verarbeiten.|  
|[Verwenden von mehreren Resultsets](../content/Using-Multiple-Result-Sets.md)|Beschreibt die Verwendung des JDBC\-Treibers, um Daten aus mehreren Resultsets abzurufen.|  
|[Verwenden von SQL-Escapesequenzen](../content/Using-SQL-Escape-Sequences.md)|Beschreibt die Verwendung von SQL\-Escapesequenzen, wie z. B. Datums\- und Zeitliteralen und \-funktionen.|  
|[Verwenden von automatisch generierten Schlüsseln](../content/Using-Auto-Generated-Keys.md)|Beschreibt die Verwendung von automatisch generierten Schlüsseln.|  
|[Ausführen von Batchvorgängen](../content/Performing-Batch-Operations.md)|Beschreibt die Verwendung des JDBC\-Treibers, um Batchoperationen auszuführen.|  
|[Verarbeiten komplexer Anweisungen](../content/Handling-Complex-Statements.md)|Beschreibt die Verwendung des JDBC\-Treibers, um komplexe Anweisungen auszuführen, die vielfältige Tasks ausführen und verschiedene Datentypen zurückgeben können.|  
  
## Siehe auch  
 [Übersicht über den JDBC-Treiber](../content/Overview-of-the-JDBC-Driver.md)  
  
  