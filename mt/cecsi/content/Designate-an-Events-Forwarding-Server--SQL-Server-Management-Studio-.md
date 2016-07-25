---
title: "Bestimmen eines Ereignisweiterleitungsservers (SQL Server Management Studio)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 81dfcbe4-3000-4e77-99de-bf85fef63a12
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
# Bestimmen eines Ereignisweiterleitungsservers (SQL Server Management Studio)
In diesem Thema wird beschrieben, wie Sie einen Server bestimmen, auf den von [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Ereignisse in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] . Ereignisweiterleitung gilt für Ereignisse, die zwischen Servern weitergeleitet werden, und nicht für Ereignisse, die zwischen Instanzen von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] weitergeleitet werden, die auf einem einzelnen Computer gehostet werden. Beachten Sie außerdem, dass zum Empfangen weitergeleiteter Ereignisse der Warnungsverwaltungsserver eine Standardinstanz von SQL Server sein muss.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Sicherheit](#Security)  
  
-   **So bestimmen Sie einen Ereignisweiterleitungsserver mit**  
  
    [SQL Server Management Studio](#SSMSProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Erfordert die Mitgliedschaft in der festen Serverrolle **sysadmin** .  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So bestimmen Sie einen Ereignisweiterleitungsserver  
  
1.  Klicken Sie im Objekt-Explorer **** auf das Pluszeichen, um den Server zu erweitern, von dem aus Sie Ereignisse an andere Server weiterleiten möchten.  
  
2.  Rechts\-Klicken Sie auf **SQL Server-Agent** und wählen Sie **Eigenschaften**.  
  
3.  In der **SQL Server-Agent-Eigenschaften –***Server\_Namen* Dialogfeld **Wählen Sie eine Seite**, Option **Erweitert**.  
  
4.  Aktivieren Sie unter **SQL Server-Ereignisweiterleitung**das Kontrollkästchen **Ereignisse an anderen Server weiterleiten** .  
  
5.  Klicken Sie in der Liste **Server** auf einen Server, und wählen Sie dann unter **Ereignisse**eine der folgenden Aktionen aus:  
  
    -   Klicken Sie auf **Ereignisse ohne Behandlung** , um nur Ereignisse weiterzuleiten, die noch nicht von lokalen Warnungen verarbeitet wurden.  
  
    -   Klicken Sie auf **Alle Ereignisse** , um alle Ereignisse unabhängig davon weiterzuleiten, ob sie von lokalen Warnungen verarbeitet wurden.  
  
6.  Klicken Sie in der Liste **Bei diesem Schweregrad des Ereignisses oder darüber** auf den Schweregrad, bei dem Ereignisse an den ausgewählten Server weitergeleitet werden.  
  
7.  Wenn Sie fertig sind, klicken Sie auf **OK**.  
  
