---
title: "Operatoren"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 38e8488f-2669-4cea-b9c3-5f394a663678
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
# Operatoren
Operatoren sind Aliasnamen für Personen oder Gruppen, die elektronische Benachrichtigungen erhalten können, sobald ein Auftrag abgeschlossen oder eine Warnung ausgelöst wird. Der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Dienst unterstützt die Benachrichtigung der Administratoren durch Operatoren. Durch Operatoren werden Benachrichtigungs- und Überwachungsfunktionen des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agents aktiviert.  
  
## Operatorattribute und -konzepte  
Für Operatoren gelten die folgenden Hauptattribute:  
  
-   Operatorname  
  
-   Kontaktinformationen  
  
### Benennen eines Operators  
Jeder Operator muss einen Namen aufweisen. Operatornamen müssen innerhalb von eindeutig sein der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Instanz und können nicht länger als **128** Zeichen.  
  
### Kontaktinformationen  
Die Kontaktinformationen eines Operators definieren, wie der Operator benachrichtigt wird. Operatoren durch e-Mail benachrichtigt werden\-e-Mail, Pager oder über die **net Send** Befehl:  
  
> [!IMPORTANT]  
> Die Pager- und **net send** -Optionen werden in zukünftigen Versionen von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] nicht mehr im [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]. Vermeiden Sie die Verwendung dieser Funktionen bei neuen Entwicklungsarbeiten, und planen Sie die Änderung von Anwendungen, die diese Funktionen zurzeit verwenden.  
  
-   **E\-e-Mail-Benachrichtigung**  
  
    E\-e-Mail-Benachrichtigung sendet einen e\-e-Mail-Nachricht an den Operator. E\-e-Mail-Benachrichtigung geben Sie die e\-e-Mail-Adresse des Operators.  
  
-   **Pagerbenachrichtigung**  
  
    Paging wird implementiert, indem e\-e-Mail-Nachrichten. Für die Pagerbenachrichtigung Geben Sie e\-e-Mail-Adresse, in denen der Operator per Pager-Nachrichten erhält. Zum Einrichten der Pagerbenachrichtigung müssen Sie Software auf dem Mailserver installieren, auf dem eingehende E-Mails verarbeitet und in eine Pagernachricht konvertiert werden. Mit der Software können unterschiedliche Methoden genutzt werden:  
  
    -   Weiterleiten der E-Mail an einen Remotemailserver am Standort des Pageranbieters.  
  
        Der Pageranbieter muss diesen Dienst anbieten, obwohl die erforderliche Software gewöhnlich als Teil des lokalen Mailsystems zur Verfügung steht. Weitere Informationen finden Sie in der Pager-Dokumentation.  
  
    -   Die e-Mail-Routing\-Mail über das Internet auf einen e\-e-Mail-Server am Standort des Pageranbieters.  
  
        Es handelt sich hierbei um eine Variation der ersten Methode.  
  
    -   Verarbeitung der eingehenden e\-e-Mail und Anwählen des Pagers mithilfe eines angeschlossenen Modems.  
  
        Diese Software wird vom Pagerdienstanbieter bereitgestellt. Die Software agiert als eine e\-e-Mail-Client, der in regelmäßigen Abständen einen Posteingang verarbeitet entweder durch die Interpretation oder einen Teil der e\-e-Mail-Adressinformationen als Pagernummern oder durch entsprechende e\-e-Mail-Namen einer Pagernummer in einer Übersetzungstabelle zugeordnet.  
  
        Wenn alle Operatoren Pageranbieter gemeinsam nutzen, können Sie [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] an eine spezielle e\-Pager erforderlichen e-Mail-Formatierung,\-\-e\-e-Mail-System. Die spezielle Formatierung kann ein Präfix oder Suffix und können aufgenommen werden in den folgenden Zeilen des e\-e-Mail:  
  
        **Betreff:**  
  
        **Cc**:  
  
        **Um**:  
  
    > [!NOTE]  
    > Wenn Sie einen niedrigen verwenden\-Kapazität alphanumerischen Pagingsystems, kürzen Sie den Text, der gesendet wird, indem Sie den Fehlertext aus der Pagerbenachrichtigung ausschließen. Ein Beispiel für einen niedrigen\-alphanumerischen Pagingsystems Kapazität ist eine, die auf 64 Zeichen pro Seite begrenzt ist.  
  
-   **NET sendnotification**  
  
    Dies sendet eine Nachricht an den Operator durch die **net Send** Befehl. Für **net Send**, geben Sie den Empfänger (Computer oder Benutzer) einer Netzwerknachricht an.  
  
    > [!NOTE]  
    > Die **net Send** Befehl verwendet Microsoft Windows Messenger. Um Warnungen fehlerfrei senden zu können, muss dieser Service sowohl auf dem Computer ausgeführt werden, auf dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ausgeführt wird, als auch auf dem Computer, den der Operator verwendet.  
  
## Warnung und Fehler\-Safe-Operatoren  
Sie können die Operatoren auswählen, die als Reaktion auf eine Warnung benachrichtigt werden sollen. So können Sie beispielsweise die Zuständigkeiten bei der Operatorbenachrichtigung abwechselnd zuweisen, indem Sie Zeitpläne für Warnungen verwenden. Auf diese Weise wird z. B. Person A über Warnungen benachrichtigt, die am Montag, Mittwoch oder Freitag auftreten, und Person B ist für Warnungen am Dienstag, Donnerstag oder Samstag zuständig.  
  
Der Fehler\-safe Operator empfängt eine Benachrichtigung, nachdem alle Pagerbenachrichtigungen an Operatoren fehlgeschlagen sind. Wenn Sie drei Operatoren für die Pagerbenachrichtigungen definiert haben und keiner dieser Operatoren ausgelagert werden kann, z. B. die Fail\-safe Operator benachrichtigt wird.  
  
Der fehlschlägt\-safe Operator wird benachrichtigt, wenn:  
  
-   Die für die Warnung verantwortlichen Operatoren können per Pager nicht benachrichtigt werden.  
  
    Gründe für Fehler bei der primären Operatoren umfassen die Pageradresse fehlerhaft aktivieren und deaktivieren,\-Zoll-Operatoren.  
  
-   [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent kann nicht auf die Systemtabellen in der **Msdb** Datenbank.  
  
    Die **Sysnotifications** -Systemtabelle gibt bei Warnungen an.  
  
Der Fehler\-safe Operator ist ein Sicherheitsfeature. Operators zugewiesen fehlschlagen kann nicht gelöscht werden\-sicher Aufgabe ohne Fehler Neuzuweisen\-sicher Pflicht, einen anderen Operator oder durch das Löschen der fehlschlägt\-sicher Zuweisung vollständig.  
  
## Benachrichtigen eines Operators  
Sie müssen mindestens eines der folgenden Elemente einrichten, um einen Operator benachrichtigen zu können:  
  
-   E-Mail senden\-e-Mail-Nachrichten mit den Funktionen der Datenbank-Mail, benötigen Sie Zugriff auf einen e\-e-Mail-Server, der SMTP unterstützt.  
  
-   Für das Paging, benötigen Sie dritten\-Partei Pager\-\-e\-e-Mail-Software und\/oder Hardware.  
  
-   Mit **net Send**, der Operator, mit dem angegebenen Computer angemeldet sein muss, und der angegebene Computer muss Nachrichten von Windows Messenger zulassen.  
  
## Verwandte Aufgaben  
  
|||  
|-|-|  
|**Aufgaben**|**Thema**|  
|Tasks beim Erstellen eines Operators|[Erstellen eines Operators](../content/Create-an-Operator.md)<br /><br />[Bestimmen eines Ausfallsicherheitsoperators](../content/Designate-a-Fail-Safe-Operator.md)|  
|Tasks beim Zuordnen von Warnungen|[Zuweisen von Warnungen zu einem Operator](../content/Assign-Alerts-to-an-Operator.md)<br /><br />[Definieren Sie die Antwort auf eine Warnung & #40. SQL Server Management Studio & #41;](../content/Define-the-Response-to-an-Alert--SQL-Server-Management-Studio-.md)<br /><br />[sp_add_notification (Transact-SQL)](assetId:///0525e0a2-ed0b-4e69-8a4c-a9e3e3622fbd)<br /><br />[Zuweisen von Warnungen zu einem Operator](../content/Assign-Alerts-to-an-Operator.md)|  
  
## Siehe auch  
[Datenbank-E-Mail](assetId:///9e4563dd-4799-4b32-a78a-048ea44a44c1)  
  
