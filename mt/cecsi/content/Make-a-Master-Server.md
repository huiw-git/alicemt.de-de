---
title: "Einrichten eines Masterservers"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 05739a73-1fdf-4d9d-92a6-70f328380322
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
# Einrichten eines Masterservers
In diesem Thema wird beschrieben, wie Sie mithilfe von [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] oder [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] einen [!INCLUDE[tsql](../content/includes/tsql_md.md)]-Masterserver einrichten.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Sicherheit](#Security)  
  
-   **Einrichten eines Masterservers mit:**  
  
    [SQL Server Management Studio](#SSMSProcedure)  
  
    [Transact-SQL](#TsqlProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Security"></a>Sicherheit  
Verteilte Aufträge mit Schritten, die einem Proxy zugeordnet sind, werden im Kontext des Proxykontos auf dem Zielserver ausgeführt. Stellen Sie sicher, dass die folgenden Bedingungen erfüllt sind, da andernfalls einem Proxy zugeordnete Auftragsschritte nicht vom Masterserver auf den Zielserver heruntergeladen werden:  
  
-   Der Registrierungsunterschlüssel des Masterservers **\\HKEY\_lokalen\_Computer\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\< & #42; Instanz\_Name & #42; >\\SQL Server-Agent\\AllowDownloadedJobsToMatchProxyName** (REG\_DWORD) auf 1 (True) festgelegt ist. Dieser Unterschlüssel ist standardmäßig auf 0 (false) festgelegt.  
  
-   Auf dem Zielserver ist ein Proxykonto vorhanden, das den gleichen Namen wie das Proxykonto des Masterservers hat, unter dem der Auftragsschritt ausgeführt wird.  
  
Wenn Auftragsschritte, die Verwendung von Proxykonten fehlschlagen, wenn sie auf dem Zielserver vom Masterserver herunterladen können Sie überprüfen die **Fehler\_Nachricht** -Spalte in der **Sysdownloadlist** -Tabelle in der **Msdb** Datenbank für die folgenden Fehlermeldungen:  
  
-   "Für den Auftragsschritt ist ein Proxykonto erforderlich, das Proxyabgleichen ist auf dem Zielserver aber deaktiviert."  
  
    Um diesen Fehler zu beheben, legen Sie den Registrierungsunterschlüssel **AllowDownloadedJobsToMatchProxyName** auf 1 fest.  
  
-   "Proxy nicht gefunden."  
  
    Um diesen Fehler zu beheben, stellen Sie sicher, dass auf dem Zielserver ein Proxykonto vorhanden ist, das den gleichen Namen wie das Proxykonto des Masterservers hat, unter dem der Auftragsschritt ausgeführt wird.  
  
#### <a name="Permissions"></a>Berechtigungen  
Standardmäßig verfügen Mitglieder der festen Serverrolle **sysadmin** über die Berechtigungen zum Ausführen dieser Prozedur.  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So richten Sie einen Masterserver ein  
  
1.  Stellen Sie im **Objekt-Explorer** eine Verbindung mit einer Instanz von [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)]her, und erweitern Sie dann diese Instanz.  
  
2.  Rechts\-Klicken Sie auf **SQL Server-Agent**, zeigen Sie auf **Multiserveradministration**, und klicken Sie dann auf **als Masterserver**. Der **Masterserver-Assistent** führt Sie durch die Schritte zum Einrichten eines Masterservers und Hinzufügen eines Zielservers.  
  
3.  Aus der **Masterserveroperator** Seite, konfigurieren Sie einen Operator für den Masterserver zum Senden von Benachrichtigungen an Operatoren mit e\-e-Mail oder Pager, [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent muss konfiguriert werden, um e-Mail zu senden\-e-Mail-Nachrichten. Senden von Benachrichtigungen an Operatoren mit **net Send**, der Messenger-Dienst muss auf dem Server ausgeführt werden, in denen [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent befindet.  
  
    **E\-e-Mail-Adresse**  
    Legt die e\-e-Mail-Adresse des Operators.  
  
    **Pageradresse**  
    Legt die Pager-e\-e-Mail-Adresse des Operators.  
  
    **NET SEND-Adresse**  
    Legt die **net Send** -Adresse des Operators.  
  
4.  Wählen Sie auf der Seite **Zielserver** Zielserver für den Masterserver aus.  
  
    **Registrierte Server**  
    Listet die in Microsoft [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] registrierten Server auf, die noch nicht als Zielserver festgelegt wurden.  
  
    **Zielserver**  
    Listet die Server auf, die Zielserver sind.  
  
    **>**  
    Verschiebt den ausgewählten Server in die Liste mit den Zielservern.  
  
    **>>**  
    Verschiebt alle Server auf die Zielserverliste.  
  
    **<**  
    Entfernt den ausgewählten Server aus der Liste mit den Zielservern.  
  
    **<<**  
    Entfernt alle Server von der Zielserverliste.  
  
    **Verbindung hinzufügen**  
    Fügt der Zielserverliste einen Server hinzu, ohne diesen zu registrieren.  
  
    **Verbindung**  
    Ändert die Verbindungseigenschaften der ausgewählten Server.  
  
5.  Geben Sie auf der Seite **Masterserver-Anmeldeinformationen** an, ob für den Zielserver ein neuer Anmeldename erstellt werden soll, und weisen Sie ihm ggf. Rechte für den Masterserver zu.  
  
    **Bei Bedarf eine neue Anmeldung erstellen und ihr Rechte für MSX zuweisen**  
    Erstellt eine neue Anmeldung auf dem Zielserver, sofern die angegebene Anmeldung noch nicht vorhanden ist.  
  
## <a name="TsqlProcedure"></a>Mithilfe von Transact\-SQL  
  
#### So richten Sie einen Masterserver ein  
  
1.  Stellen Sie eine Verbindung mit dem [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**. Im folgenden Beispiel wird der aktuelle Server auf dem Masterserver "AdventureWorks1" eingetragen. Der Speicherort für den aktuellen Server ist "Building 21, Room 309, Rack 5".  
  
```  
USE msdb ;  
GO  
  
EXEC dbo.sp_msx_enlist N'AdventureWorks1',   
    N'Building 21, Room 309, Rack 5' ;   
GO;  
```  
  
Weitere Informationen finden Sie unter [Sp_msx_enlist (Transact-SQL)](assetId:///ceb3b2bc-0cc4-48d8-9bdc-6a809556e35f).  
  
## Siehe auch  
[Erstellen einer Multiserverumgebung](../content/Create-a-Multiserver-Environment.md)  
[Automatisierte Verwaltung in einem Unternehmen](../content/Automated-Administration-Across-an-Enterprise.md)  
  
