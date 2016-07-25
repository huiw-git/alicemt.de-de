---
title: "Verwalten des Transaktionsumfangs"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 82900342-bc80-445f-98a4-468a303aae1e
caps.latest.revision: 9
caps.handback.revision: 8
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
# Verwalten des Transaktionsumfangs
  Wenn Sie mit Transaktionen arbeiten, ist es wichtig, die Transaktionen so kurz wie möglich zu halten. Der Standardmodus von „auto\-commit“, den Sie mithilfe der [setAutoCommit](../content/setAutoCommit-Method--SQLServerConnection-.md)\-Methode aktivieren und deaktivieren können, führt einen Commit für jede Aktion aus. Dies ist der Modus, mit dem die meisten Entwickler am bequemsten arbeiten können.  
  
 Wenn Sie manuelle Transaktionen verwenden, stellen Sie sicher, dass im Code so schnell wie möglich ein Commit für die Transaktion ausgeführt wird. Durch das Offenhalten einer Transaktion wird blockiert, dass andere Benutzer auf die Daten zugreifen können. Es ist beispielsweise ein gutes Programmierverfahren, einen rollback\-Aufruf im catch\-Block und einen commit\-Aufruf im finally\-Block einzufügen. Dies ist jedoch vom Entwurf der Anwendung abhängig.  
  
 Wenn der Umfang der Transaktionen klein gehalten wird, führt dies zu einer besseren Parallelität. Wenn Sie beispielsweise eine manuelle Transaktion beginnen und 10.000 Zeilen in einer Tabelle mit 20.000 Zeilen ändern, ist die Hälfte der Tabelle für alle anderen Benutzer blockiert, auch wenn sie die Daten nur lesen. Durch das Reduzieren der Änderungen auf 2.000 Zeilen bleiben 90 Prozent der Tabelle verfügbar.  
  
 Stellen Sie außerdem sicher, dass Sie die Timeouteinstellung für Sperren verwenden, wenn die Anwendung Probleme mit Sperren erwartet und hierfür Timeouts benötigt. Dies kann auf einfache Weise mithilfe der [setLockTimeout](../content/setLockTimeout-Method--SQLServerDataSource-.md)\-Methode ausgeführt werden. Der Standardwert für das Sperrtimeout ist \-1. Dies bedeutet, dass beim Warten auf die Sperre unendlich lang blockiert wird. Sie können das Sperrtimeout auf 30 Sekunden festlegen. So tritt bei der gesperrten Verbindung nach 30 Sekunden ein Timeout auf, wenn eine Blockierung durch eine andere Verbindung vorliegt.  
  
## Siehe auch  
 [Verbessern von Leistung und Zuverlässigkeit mit dem JDBC-Treiber](../content/Improving-Performance-and-Reliability-with-the-JDBC-Driver.md)  
  
  