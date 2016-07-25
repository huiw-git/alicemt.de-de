---
title: "Grundlegendes zu Transaktionen"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d3e0414c-6809-4bb1-93b1-4960507faecc
caps.latest.revision: 32
caps.handback.revision: 29
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
# Grundlegendes zu Transaktionen
  Bei Transaktionen handelt es sich um Gruppen von Operationen, die in logische Arbeitseinheiten zusammengefasst sind. Damit wird die Konsistenz und Integrität der einzelnen Aktionen in einer Transaktion gesteuert und gewährleistet, falls im System Fehler auftreten sollten.  
  
 Mit [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] ist eine lokale oder verteilte Transaktionsverarbeitung möglich. Transaktionen können auch Isolationsstufen verwenden. Weitere Informationen zu den vom JDBC\-Treiber unterstützten Isolationsstufen finden Sie unter [Grundlegendes zu Isolationsstufen](../content/Understanding-Isolation-Levels.md).  
  
 Anwendungen sollten Transaktionen nur entweder mit Transact\-SQL\-Anweisungen oder den vom JDBC\-Treiber bereitgestellten Methoden steuern. Wenn für die gleiche Transaktion sowohl Transact\-SQL\-Anweisungen als auch JDBC\-API\-Methoden verwendet werden, führt dies möglicherweise zu Problemen, z. B. kann der Commit einer Transaktion nicht wie erwartet durchgeführt werden, ein unerwarteter Commit oder Rollback der Transaktion wird durchgeführt und eine neue Transaktion gestartet, oder es treten Ausnahmen wie "Fehler beim Wiederaufnehmen der Transaktion" auf.  
  
## Verwenden von lokalen Transaktionen  
 Eine Transaktion wird als lokal angesehen, wenn es sich um eine Einphasentransaktion handelt, die von der Datenbank direkt verarbeitet wird. Der JDBC\-Treiber unterstützt lokale Transaktionen über die Methoden der [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Klasse, wie z. B. [setAutoCommit](../content/setAutoCommit-Method--SQLServerConnection-.md), [commit](../content/commit-Method--SQLServerConnection-.md) und [rollback](../content/rollback-Method---.md). Lokale Transaktionen werden normalerweise explizit von der Anwendung oder automatisch vom Anwendungsserver für die Java\-Plattform, Enterprise Edition \(Java EE\) verwaltet.  
  
 Im folgenden Beispiel wird eine lokale Transaktion mit zwei getrennten Anweisungen im `try` \-Block ausgeführt. Die Anweisungen werden für die Production.ScrapReason\-Tabelle in der [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)][!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)]\-Beispieldatenbank ausgeführt. Wenn keine Ausnahmen ausgegeben werden, wird ein Commit ausgeführt. Der Code im `catch` \-Block führt ein Rollback der Transaktion aus, wenn eine Ausnahme ausgelöst wird.  
  
 [!CODE [JDBC#UnderstandingTransactions1](../CodeSnippet/SQLDrivers/jdbc#understandingtransactions1)]  
  
## Verwenden von verteilten Transaktionen  
 Eine verteilte Transaktion aktualisiert Daten in mindestens zwei vernetzten Datenbanken, wobei die wichtigen Eigenschaften der Transaktionsverarbeitung \(unteilbar, konsistent, isoliert und dauerhaft\) gewährleistet werden. Die Unterstützung verteilter Transaktionen wurde in der optionalen API\-Spezifikation von JDBC 2.0 in die JDBC\-API aufgenommen. Die Verwaltung verteilter Anwendungen wird normalerweise automatisch vom JTS\-Transaktions\-Manager \(Java Transaction Service\) in einer Java EE\-Anwendungsserverumgebung ausgeführt.[!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] unterstützt jedoch verteilte Transaktionen mit jedem JTA\-kompatiblen \(Java Transaction API\) Transaktions\-Manager.  
  
 Der JDBC\-Treiber ist nahtlos in [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] Distributed Transaction Coordinator \(MS DTC\) integriert, um eine echte Unterstützung von verteilten Transaktionen mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] zu ermöglichen. Bei MS DTC handelt es sich um eine Funktion für verteilte Transaktionen, die von [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] für [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] Windows\-Systeme bereitgestellt wird. MS DTC verwendet bewährte Transaktionsverarbeitungstechnologien von [!INCLUDE[msCoName](../content/includes/msCoName_md.md)], um XA\-Funktionen wie das vollständige verteilte Protokoll für Zweiphasencommit und die Wiederherstellung von verteilten Transaktionen zu unterstützen.  
  
 Weitere Informationen zur Verwendung von verteilten Transaktionen finden Sie unter [Grundlegendes zu XA-Transaktionen](../content/Understanding-XA-Transactions.md).  
  
## Siehe auch  
 [Ausführen von Transaktionen mit dem JDBC-Treiber](../content/Performing-Transactions-with-the-JDBC-Driver.md)  
  
  