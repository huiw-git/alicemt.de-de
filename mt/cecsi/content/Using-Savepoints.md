---
title: "Verwenden von Sicherungspunkten"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3b48eb13-32ef-4fb3-8e95-dbc9468c9a44
caps.latest.revision: 19
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
# Verwenden von Sicherungspunkten
  Sicherungspunkte bieten einen Mechanismus, um für Abschnitte einer Transaktion einen Rollback auszuführen. In [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] können Sie mit der Anweisung "SAVE TRANSACTION Sicherungspunktname" einen Sicherungspunkt erstellen. Später können Sie die Anweisung "ROLLBACK TRANSACTION Sicherungspunktname" ausführen, um ein Rollback bis zum Sicherungspunkt auszuführen, anstatt ein Rollback bis zum Beginn der Transaktion auszuführen.  
  
 Sicherungspunkte sind vor allem in Situationen hilfreich, in denen das Auftreten von Fehlern unwahrscheinlich ist. Die Verwendung eines Sicherungspunkts, um für einen Teil einer Transaktion im Falle eines seltenen Fehlers einen Rollback auszuführen, kann effizienter sein, als jede Transaktion vor dem Ausführen einer Aktualisierung daraufhin testen zu lassen, ob die Aktualisierung gültig ist. Aktualisierungen und Rollbacks sind kostspielige Operationen. Sicherungspunkte sind also nur dann effektiv, wenn die Wahrscheinlichkeit eines Fehlers gering und die Kosten für die Vorabüberprüfung der Gültigkeit einer Aktualisierung relativ hoch sind.  
  
 [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] unterstützt die Verwendung von Sicherungspunkten über die [setSavepoint](../content/setSavepoint-Method--SQLServerConnection-.md)\-Methode der [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Klasse. Mit der setSavepoint\-Methode können Sie in der aktuellen Transaktion einen benannten oder unbenannten Sicherungspunkt erstellen. Die Methode gibt ein [SQLServerSavepoint](../content/SQLServerSavepoint-Class.md)\-Objekt zurück. In einer Transaktion können mehrere Sicherungspunkte erstellt werden. Um ein Rollback einer Transaktion bis zu einem bestimmten Sicherungspunkt auszuführen, können Sie das SQLServerSavepoint\-Objekt an die [rollback](../content/rollback-Method--java.sql.Savepoint-.md)\-Methode \(java.sql.Savepoint\) übergeben.  
  
 Im folgenden Beispiel wird beim Ausführen einer lokalen Transaktion mit zwei getrennten Anweisungen im `try`\-Block ein Sicherungspunkt verwendet. Die Anweisungen werden für die Production.ScrapReason\-Tabelle in der [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)][!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank ausgeführt. Für den Rollback der zweiten Anweisung wird ein Sicherungspunkt verwendet. Dies führt dazu, dass nur für die erste Anweisung ein Commit in der Datenbank ausgeführt wird.  
  
 [!CODE [JDBC#UsingSavepoints1](../CodeSnippet/SQLDrivers/jdbc#usingsavepoints1)]  
  
## Siehe auch  
 [Ausführen von Transaktionen mit dem JDBC-Treiber](../content/Performing-Transactions-with-the-JDBC-Driver.md)  
  
  