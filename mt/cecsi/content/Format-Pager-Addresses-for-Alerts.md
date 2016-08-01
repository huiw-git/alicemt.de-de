---
title: "Formatieren von Pageradressen f&#252;r Warnungen"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a9797d01-1050-442c-9038-ed4bfee1e76a
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
# Formatieren von Pageradressen f&#252;r Warnungen
In diesem Thema wird beschrieben, wie Pageradressen für [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Warnungen in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] oder [!INCLUDE[tsql](../content/includes/tsql_md.md)]formatiert werden.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Sicherheit](#Security)  
  
-   **So formatieren Sie Pageradressen mit**  
  
    [SQL Server Management Studio](#SSMSProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Standardmäßig können nur Mitglieder der festen Serverrolle **sysadmin** Information über eine Warnung anzeigen. Andere Benutzer müssen Mitglieder der festen Datenbankrolle **SQLAgentOperatorRole** in der **msdb** -Datenbank sein.  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So formatieren Sie Pageradressen  
  
1.  Klicken Sie im Objekt-Explorer ****auf das Pluszeichen, um den Server zu erweitern, der die Warnung enthält, die Sie an einen Pager senden möchten.  
  
2.  Rechts\-Klicken Sie auf **SQL Server-Agent** und wählen Sie **Eigenschaften**  
  
3.  Wählen Sie unter **Seite auswählen**die Option **Warnungssystem**aus.  
  
4.  In der **Zeile** und **CC-Zeile** Felder die **Adressformatierung für Pager-e\-e-Mails** Geben Sie die Pageradressenpräfix oder Suffix. Die eigentliche Pageradresse des Operators wird beim Senden einer Benachrichtigung eingefügt.  
  
5.  Geben Sie in das Feld **Betreff** das Präfix oder Suffix der Betreffzeile ein.  
  
6.  Wählen Sie den **Text der e-Mail enthalten\-e-Mail in Benachrichtigungsseite** Kontrollkästchen, um die vollständige e\-e-Mail-Nachricht in die Pagernachricht (statt lediglich die Betreffzeile).  
  
7.  Wenn Sie fertig sind, klicken Sie auf **OK**.  
  
