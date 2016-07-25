---
title: "Force a Target Server to Poll the Master Server"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f1189a47-5ac3-45e2-9c5f-847810672279
caps.latest.revision: 4
caps.handback.revision: 3
manager: jhubbard
translation.priority.mt: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pt-br
  - ru-ru
  - zh-cn
  - zh-tw
---
# Force a Target Server to Poll the Master Server
Dieses Thema beschreibt, wie Sie erzwingen, dass ein Zielserver den Masterserver abruft. Der Zielserver muss ein registrierter Server auf dem Masterserver sein.  
  
Ein Auftrag ist eine festgelegte Reihe von Aktionen, die der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent ausführt. Ein Multiserverauftrag ist ein Auftrag, der von einem Masterserver auf mindestens einem Zielserver ausgeführt wird. Auf jedem Server kann gleichzeitig eine Instanz des gleichen Auftrags ausgeführt werden. Jeder Zielserver ruft in regelmäßigen Abständen den Masterserver ab, lädt eine Kopie aller neuen Aufträge herunter, die dem Zielserver zugewiesen wurden, und trennt dann die Verbindung. Der Zielserver führt den Auftrag lokal aus und stellt dann erneut eine Verbindung mit dem Masterserver her, um den Auftragsergebnisstatus hochzuladen.  
  
> [!NOTE]  
> Wenn der Masterserver nicht möglich ist, wenn der Zielserver versucht, den Auftragsstatus hochzuladen, wird der Status des Auftrags in die Warteschlange gestellt, bis der Masterserver zugegriffen werden kann.  
  
-   **Vorbereitungen:**  [Einschränkungen](#Restrictions), [Sicherheit](#Security)  
  
-   **Einen Zielserver den Masterserver abruft erzwingen verwenden:** [SQL Server Management Studio](#SSMS)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
Der Zielserver muss ein registrierter Server auf dem Masterserver sein. Die Anweisungen in diesem Thema müssen auf dem Masterserver ausgeführt werden.  
  
### <a name="Security"></a>Sicherheit  
Ausführliche Informationen finden Sie unter [Implement SQL Server Agent Security](../content/Implement-SQL-Server-Agent-Security.md) und [Choose the Right SQL Server Agent Service Account for Multiserver Environments](../content/Choose-the-Right-SQL-Server-Agent-Service-Account-for-Multiserver-Environments.md).  
  
## <a name="SSMS"></a>Verwendung von SQL Server Management Studio  
**So erzwingen Sie, dass ein Zielserver den Masterserver abruft**  
  
1.  Erweitern Sie im **Objekt-Explorer**den Masterserver.  
  
2.  Rechts\-Klicken Sie auf **SQL Server-Agent**, zeigen Sie auf **Multiserveradministration**, und klicken Sie dann auf **Zielserver verwalten**.  
  
3.  Klicken Sie auf einen Zielserver und dann auf **Abruf erzwingen**.  
  
