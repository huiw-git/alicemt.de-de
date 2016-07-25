---
title: "Set the Polling Interval for Target Servers"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4ffbbefa-77fb-442e-a77c-cb8c6cab9f3c
caps.latest.revision: 5
caps.handback.revision: 4
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
# Set the Polling Interval for Target Servers
In diesem Thema wird das Festlegen der Frequenz für den [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent beschrieben, mit der Informationen vom Master- zu den Zielservern aktualisiert werden. Ein Auftrag ist eine festgelegte Reihe von Aktionen, die der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent ausführt. Ein Multiserverauftrag ist ein Auftrag, der von einem Masterserver auf mindestens einem Zielserver ausgeführt wird.  
  
-   **Vorbereitungen:**  [Sicherheit](#Security)  
  
-   **Festlegen des Abrufintervalls für Zielserver mit:** [SQL Server Management Studio](#SSMS), [Transact-SQL](#TSQL)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
Auf jedem Server kann gleichzeitig eine Instanz des gleichen Auftrags ausgeführt werden. Jeder Zielserver ruft in regelmäßigen Abständen den Masterserver ab, lädt eine Kopie aller neuen Aufträge herunter, die dem Zielserver zugewiesen wurden, und trennt dann die Verbindung. Der Zielserver führt den Auftrag lokal aus und stellt dann erneut eine Verbindung mit dem Masterserver her, um den Auftragsergebnisstatus hochzuladen.  
  
> [!NOTE]  
> Wenn der Masterserver nicht möglich ist, wenn der Zielserver versucht, den Auftragsstatus hochzuladen, wird der Status des Auftrags in die Warteschlange gestellt, bis der Masterserver zugegriffen werden kann.  
  
### <a name="Security"></a>Sicherheit  
Ausführliche Informationen finden Sie unter [Implement SQL Server Agent Security](../content/Implement-SQL-Server-Agent-Security.md) und [Choose the Right SQL Server Agent Service Account for Multiserver Environments](../content/Choose-the-Right-SQL-Server-Agent-Service-Account-for-Multiserver-Environments.md).  
  
## <a name="SSMS"></a>Verwendung von SQL Server Management Studio  
**So legen Sie das Abrufintervall für Zielserver fest**  
  
1.  Stellen Sie im **Objekt-Explorer** eine Verbindung mit einer Instanz von [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)]her, und erweitern Sie dann diese Instanz.  
  
2.  Rechts\-Klicken Sie auf **SQL Server-Agent**, zeigen Sie auf **Multiserveradministration**, und klicken Sie dann auf **Zielserver verwalten**.  
  
3.  Klicken Sie auf der Registerkarte **Status des Zielservers** auf **Anweisungen bereitstellen**.  
  
4.  Wählen Sie in der Liste **Anweisungstyp** die Option **Abrufintervall festlegen**aus.  
  
5.  Geben Sie im Feld **Abrufintervall** die Anzahl von Sekunden zwischen 10 und 28.800 ein, die verstreichen müssen, bevor der Zielserver den Masterserver abruft.  
  
6.  Führen Sie unter **Empfänger**eine der folgenden Aktionen aus:  
  
    1.  Klicken Sie auf **Alle Zielserver** , wenn für alle Zielserver dasselbe Abrufintervall gilt.  
  
    2.  Klicken Sie auf **Diese Zielserver** , wenn nicht für alle Zielserver dasselbe Abrufintervall gilt, und wählen Sie dann die Zielserver aus, für die dieses Abrufintervall verwendet werden soll.  
  
## <a name="TSQL"></a>Mithilfe von Transact\-SQL  
**So legen Sie das Abrufintervall für Zielserver fest**  
  
1.  Stellen Sie im Objekt-Explorer eine Verbindung mit einer Instanz von Database Engine (Datenbankmodul) her, und erweitern Sie dann diese Instanz.  
  
2.  Klicken Sie auf der Symbolleiste auf **Neue Abfrage**.  
  
3.  Verwenden Sie im Abfragefenster die [Sp_post_msx_operation (Transact-SQL)](assetId:///085deef8-2709-4da9-bb97-9ab32effdacf) gespeicherten Systemprozedur des Abrufintervalls für Zielserver festzulegen.  
  
## Siehe auch  
[sysdownloadlist](assetId:///71087a4c-e829-488e-aa7d-a9476e2b4779)  
  
