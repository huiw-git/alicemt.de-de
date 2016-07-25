---
title: "Fehlerbehandlung"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8fd5b5ef-d939-4b78-b900-5b7b6ddb3eb9
caps.latest.revision: 14
caps.handback.revision: 13
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
# Fehlerbehandlung
  Wenn Sie [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] verwenden, werden alle Datenbankfehlerbedingungen mit der [SQLServerException](../content/SQLServerException-Class.md)\-Klasse als Ausnahmen an die Java\-Anwendung übergeben. Die folgenden Methoden der SQLServerException\-Klasse werden von "java.sql.SQLException" und "java.lang.Throwable" geerbt. Mit ihnen können spezielle Informationen zum aufgetretenen [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Fehler zurückgegeben werden:  
  
-   getSQLState gibt den normalen X\/Open\- oder SQL99\-Statuscode der Ausnahme zurück.  
  
-   getErrorCode gibt die jeweilige Datenbankfehlernummer zurück.  
  
-   getMessage gibt den vollständigen Text der Ausnahme zurück. Der Text der Fehlermeldung beschreibt das Problem und enthält häufig Platzhalter für Informationen wie Objektnamen, die in die angezeigte Fehlermeldung eingefügt werden.  
  
-   getNextException gibt das nächste SQLServerException\-Objekt oder NULL zurück, wenn keine weiteren Ausnahmeobjekte mehr vorhanden sind.  
  
 Im folgenden Beispiel werden eine offene Verbindung zur [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)][!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank an die Funktion übergeben und eine fehlerhafte SQL\-Anweisung ohne FROM\-Klausel erstellt. Anschließend werden die Anweisung ausgeführt und eine SQL\-Ausnahme verarbeitet.  
  
 [!CODE [JDBC#HandlingErrors1](../CodeSnippet/SQLDrivers/jdbc#handlingerrors1)]  
  
## Siehe auch  
 [Diagnostizieren von Problemen mit dem JDBC-Treiber](../content/Diagnosing-Problems-with-the-JDBC-Driver.md)  
  
  