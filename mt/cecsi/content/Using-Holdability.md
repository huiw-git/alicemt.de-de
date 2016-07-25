---
title: "Verwenden der Haltbarkeit"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: aa48306c-e7a0-4dcb-af21-9ebb6898e45a
caps.latest.revision: 25
caps.handback.revision: 22
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
# Verwenden der Haltbarkeit
  Standardmäßig bleibt ein Resultset, das in einer Transaktion erstellt wurde, nach einem Commit der Transaktion in der Datenbank oder einem Rollback geöffnet. Bisweilen ist es aber von Nutzen, das Resultset nach einem Commit der Transaktion zu schließen. Zu diesem Zweck unterstützt [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] die Verwendung der Resultsethaltbarkeit.  
  
 Sie können die Resultsethaltbarkeit mit der [setHoldability](../content/setHoldability-Method--SQLServerConnection-.md)\-Methode der [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Klasse einstellen. Beim Einstellen der Haltbarkeit mit der setHoldability\-Methode können für die Resultsethaltbarkeit die Konstanten ResultSet.HOLD\_CURSORS\_OVER\_COMMIT oder ResultSet.CLOSE\_CURSORS\_AT\_COMMIT verwendet werden.  
  
 Der JDBC\-Treiber unterstützt auch das Festlegen der Haltbarkeit beim Erstellen eines der Statement\-Objekte. Beim Erstellen der Statement\-Objekte, die mit Parametern für die Resultsethaltbarkeit überladen sind, muss die Haltbarkeit des Statement\-Objekts der Haltbarkeit der Verbindung entsprechen. Stimmen sie nicht überein, wird eine Ausnahme ausgelöst. Der Grund hierfür ist, dass SQL Server die Haltbarkeit nur auf Verbindungsebene unterstützt.  
  
 Bei der Haltbarkeit eines Resultsets handelt es sich um die Haltbarkeit eines SQLServerConnection\-Objekts, das nur beim Erstellen von serverseitigen Cursorn dem Resultset zugeordnet wird. Dies gilt nicht für clientseitige Cursor. Alle Resultsets mit clientseitigen Cursorn besitzen immer den Haltbarkeitswert ResultSet.HOLD\_CURSORS\_OVER\_COMMIT.  
  
 Wenn Servercursor mit SQL Server 2005 oder höher verbunden sind, wirkt sich das Festlegen der Haltbarkeit nur auf die Haltbarkeit neuer Resultsets aus, die erst noch für diese Verbindung erstellt werden. Das heißt, das Festlegen der Haltbarkeit hat keine Auswirkungen auf die Haltbarkeit von Resultsets, die zuvor erstellt wurden und für die Verbindung bereits geöffnet sind. Bei SQL Server 2000 wirkt sich das Festlegen der Haltbarkeit jedoch sowohl auf die Haltbarkeit vorhandener als auch neuer, noch für die Verbindung zu erstellender Resultsets aus.  
  
 Im folgenden Beispiel wird die Resultsethaltbarkeit beim Ausführen einer lokalen Transaktion mit zwei getrennten Anweisungen im `try`\-Block eingestellt. Die Anweisungen werden für die Production.ScrapReason\-Tabelle in der [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)]\-Beispieldatenbank [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)] ausgeführt. Zunächst wird im Beispiel zum manuellen Transaktionsmodus gewechselt, indem die der automatische Commit auf **false** festgelegt wird. Sobald der automatische Commitmodus deaktiviert ist, wird ein Commit von SQL\-Anweisungen erst ausgeführt, wenn die Anwendung die [commit](../content/commit-Method--SQLServerConnection-.md)\-Methode explizit aufruft. Der Code im catch\-Block führt ein Rollback der Transaktion aus, wenn eine Ausnahme ausgelöst wird.  
  
 [!CODE [JDBC#UsingHoldability1](../CodeSnippet/SQLDrivers/jdbc#usingholdability1)]  
  
## Siehe auch  
 [Ausführen von Transaktionen mit dem JDBC-Treiber](../content/Performing-Transactions-with-the-JDBC-Driver.md)  
  
  