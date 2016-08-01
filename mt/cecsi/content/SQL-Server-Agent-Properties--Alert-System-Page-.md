---
title: "SQL Server-Agent-Eigenschaften (Seite Warnungssystem)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3e6d3bfd-20ee-4593-86cc-f65b1c08c69d
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
# SQL Server-Agent-Eigenschaften (Seite Warnungssystem)
Verwenden Sie diese Seite zum Anzeigen und Ändern der Einstellungen für Nachrichten von [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Warnungen.  
  
## Optionen  
**Mailsitzung**  
Mithilfe der Optionen in diesem Abschnitt wird [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Mail konfiguriert.  
  
**Mailprofil aktivieren**  
Aktiviert [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Mail. Standardmäßig ist [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Mail nicht aktiviert.  
  
**Mailsystem**  
Legt das von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent zu verwendende Mailsystem fest. Datenbank-E-Mail  
  
> [!NOTE]  
> Nach dem Ändern der e\-e-Mail-System muss neu gestartet werden die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent-Diensts für die Änderung wirksam wird.  
  
**Mailprofil**  
Legt das von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent zu verwendende Profil fest. Sie können auch auswählen **<new Database Mail profile...>** ein neues Profil zu erstellen.  
  
**Pager-e\-e-Mails**  
Die Optionen in diesem Abschnitt können Sie e konfigurieren\-e-Mail-Nachrichten, die an Pageradressen Paging-System arbeiten.  
  
**Adressformatierung für Pager-e\-e-Mails**  
In diesem Abschnitt können Sie angeben, das Format für Adressen und Betreffzeile in Pager-e\-versendet.  
  
**An-Zeile**  
Gibt die Optionen für die **** der Nachricht  
  
**Präfix**  
Geben Sie einen beliebigen festgelegten Text ein, die Ihr System benötigt am Anfang der **zu** Nachrichten, die an Pager gesendet.  
  
**Pager**  
Umfasst e\-e-Mail-Adresse für die Nachricht zwischen Präfix und das Suffix.  
  
**Suffix**  
Geben Sie einen beliebigen festgelegten Text, der das pagingsystem am Ende der **zu** Nachrichten, die an Pager gesendet.  
  
**Cc-Zeile**  
Gibt die Optionen für die **Cc** der Nachricht.  
  
**Präfix**  
Geben Sie einen beliebigen festgelegten Text ein, die Ihr System benötigt am Anfang der **Cc** Nachrichten, die an Pager gesendet.  
  
**Pager**  
Umfasst e\-e-Mail-Adresse für die Nachricht zwischen Präfix und das Suffix.  
  
**Suffix**  
Geben Sie einen beliebigen festgelegten Text, der das pagingsystem am Ende der **Cc** Nachrichten, die an Pager gesendet.  
  
**Betreff**  
Bestimmt die Optionen für den Betreff der Nachricht.  
  
**Präfix**  
Geben Sie einen beliebigen festgelegten Text, der das pagingsystem am Anfang der **Betreff** Nachrichten, die an Pager gesendet.  
  
**Suffix**  
Geben Sie einen beliebigen festgelegten Text, der das pagingsystem am Ende der **Betreff** Nachrichten, die an Pager gesendet.  
  
**Text der e-Mail enthalten\-e-Mail-Nachrichten in der Benachrichtigung**  
Enthält den Text des e\-e-Mail-Nachricht die Nachricht an den Pager gesendet.  
  
**Fehler\-safe-Operator**  
In diesem Abschnitt können Sie die Optionen für den Fehler an\-safe Operator.  
  
**Aktivieren Sie Fehler\-safe-Operator**  
Legt einen Ausfallsicherheitsoperator fest.  
  
**Operator**  
Legt den Namen des Operators, der Fehler empfangen\-sicher Benachrichtigungen.  
  
**Benachrichtigen durch**  
Legt die Methode zur Benachrichtigung der fehlschlägt\-safe Operator.  
  
**Tokenersetzung**  
In diesem Abschnitt können Sie Tokens für Auftragsschritte aktivieren, die in von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Warnungen ausgeführten Aufträgen verwendet werden können. Weitere Informationen zu auftragsschritttokens finden Sie unter [Verwendung von Token in Auftragsschritten](../content/Use-Tokens-in-Job-Steps.md).  
  
> [!IMPORTANT]  
> Jeder Windows-Benutzer mit Schreibberechtigungen für das Windows-Ereignisprotokoll hat u. U. die Möglichkeit, auf Auftragsschritte zuzugreifen, die von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Warnungen aktiviert werden. Zur Vermeidung dieses Sicherheitsrisikos sind [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Tokens, die in von Warnungen aktivierten Aufträgen verwendet werden können, standardmäßig deaktiviert. Diese Token werden: **$(A\-DBN)**, **$(A\-SVR)**, **$(A\-ERR)**, **$(A\-SEV)**, und **$(A\-MSG)**.  
>   
> Wenn Sie diese Tokens verwenden müssen, können Sie sie aktivieren. Stellen Sie zuvor jedoch sicher, dass nur Mitglieder von vertrauenswürdigen Windows-Sicherheitsgruppen, wie z. B. die Gruppe Administratoren, über Schreibberechtigungen für das Ereignisprotokoll des Computers verfügen, auf dem sich [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] befindet.  
  
**Token für alle Auftragsantworten auf Warnungen ersetzen**  
Aktivieren Sie dieses Kontrollkästchen, um die Tokenersetzung für Aufträge zu aktivieren, die von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Warnungen aktiviert werden.  
  
## Siehe auch  
[Operatoren](../content/Operators.md)  
[Konfigurieren von SQL Server-Agent-Mail zum Verwenden von Datenbank-E-Mails](assetId:///4b8b61bd-4bd1-43cd-b6e5-c6ed2e101dce)  
[Datenbank-E-Mail](assetId:///9e4563dd-4799-4b32-a78a-048ea44a44c1)  
  
