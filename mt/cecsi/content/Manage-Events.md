---
title: "Verwalten von Ereignissen"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8f4ee7f5-80df-49fd-b2b8-d020e04b6e1b
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
# Verwalten von Ereignissen
Sie können an eine Instanz von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] alle Ereignismeldungen weiterleiten, die einen bestimmten Fehlerschweregrad aufweisen oder überschreiten. Dies wird als *Ereignisweiterleitung*bezeichnet. Der Weiterleitungsserver ist ein dedizierter Server, bei dem es sich auch um einen Masterserver handeln kann. Durch die Ereignisweiterleitung können Sie die Warnungsverwaltung für eine Gruppe von Servern zentralisieren und so die Arbeitsauslastung stark belasteter Server reduzieren.  
  
Wenn ein Server Ereignisse für eine Gruppe anderer Server empfängt, wird dieser Server als *Warnungsverwaltungsserver*bezeichnet. In einer Multiserverumgebung bestimmen Sie den Masterserver zum Warnungsverwaltungsserver.  
  
## Vorteile der Verwendung eines Warnungsverwaltungsservers  
Das Einrichten eines Warnungsverwaltungsservers hat u. a. folgende Vorteile:  
  
-   **Zentralisierung**. Die zentralisierte Steuerung und eine zusammenfassende Ansicht der Ereignisse mehrerer Instanzen von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] sind von einem einzigen Server aus möglich.  
  
-   **Skalierbarkeit**. Viele physische Server können als ein einziger logischer Server verwaltet werden. Sie können nach Bedarf Server zur Gruppe der physischen Server hinzufügen oder Server aus dieser Gruppe entfernen.  
  
-   **Effizienz**. Der Konfigurationsaufwand wird reduziert, da Warnungen und Operatoren nur einmal definiert werden müssen.  
  
## Nachteile der Verwendung eines Warnungsverwaltungsservers  
Das Einrichten eines Warnungsverwaltungsservers hat u. a. folgende Nachteile:  
  
-   **Erhöhter Datenverkehr**. Das Weiterleiten von Ereignissen an einen Warnungsverwaltungsserver kann den Netzwerkverkehr erhöhen. Diese Erhöhung kann durch Beschränken der Ereignisweiterleitung auf Ereignisse, die einen bestimmten Schweregrad überschreiten, verringert werden.  
  
-   **Einzelne Fehlerquelle**. Wenn der Warnungsverwaltungsserver offline geschaltet wird, werden keine Warnungen für Ereignisse auf der verwalteten Servergruppe ausgegeben.  
  
-   **Serverauslastung**. Das Behandeln von Warnungen für die weitergeleiteten Ereignisse verursacht eine erhöhte Verarbeitungsauslastung des Warnungsverwaltungsservers.  
  
## Richtlinien für das Verwenden eines Warnungsverwaltungsservers  
Beachten Sie beim Konfigurieren eines Warnungsverwaltungsservers folgende Richtlinien:  
  
-   Zum Empfangen weitergeleiteter Ereignisse muss der Warnungsverwaltungsserver eine Standardinstanz von SQL Server sein.  
  
-   Vermeiden Sie es, auf dem Warnungsverwaltungsserver Anwendungen auszuführen, die störanfällig sind oder das System stark beanspruchen.  
  
-   Ziehen Sie den Netzwerkverkehr in Betracht, der entsteht, wenn Sie mehrere Server für die Verwendung desselben Warnungsverwaltungsservers konfigurieren. Reduzieren Sie bei Überlastung die Anzahl der Server, die einen bestimmten Warnungsverwaltungsserver verwenden.  
  
    Die Server, die in registriert sind [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] bilden die Liste der von diesem Server ausgewählt werden, als Warnungen verfügbaren Server\-Server weiterleiten.  
  
-   Definieren von Warnungen auf der lokalen Instanz von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] erfordern einen Server\-bestimmte Antwort, statt die Warnungen an den Warnungsverwaltungsserver weiterzuleiten.  
  
    Für den Warnungsverwaltungsserver bilden alle an ihn weiterleitenden Server eine logische Einheit. So antwortet ein Warnungsverwaltungsserver auf dieselbe Art auf ein 605-Ereignis von Server A wie auf ein 605-Ereignis von Server B.  
  
-   Nach dem Konfigurieren des Warnungssystems sollten Sie das Microsoft Windows-Anwendungsprotokoll auf [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Ereignisse hin überprüfen.  
  
    Fehlerbedingungen, die vom Warnungsmodul erkannt werden, werden mit dem Quellnamen "SQL Server-Agent" in das lokale Windows-Anwendungsprotokoll geschrieben. Zum Beispiel wenn [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent kann keinen e senden\-e-Mail-Benachrichtigung, wie sie definiert wurde, wird ein Ereignis im Anwendungsprotokoll protokolliert.  
  
Wenn eine lokal definierte Warnung deaktiviert ist, und ein Ereignis auftritt, würde die Warnung ausgelöst verursacht haben, wird das Ereignis an den Warnungsverwaltungsserver weitergeleitet (sofern es sich um die Warnung erfüllt\-Bedingung weiterleiten). Die Weiterleitung ermöglicht es, dass lokale Überschreibungen (lokal definierte Warnungen, die auch auf dem Warnungsverwaltungsserver definiert sind) nach Bedarf des Benutzers am lokalen Standort aktiviert und deaktiviert werden können. Sie können auch anfordern, dass Ereignisse immer weitergeleitet werden, selbst wenn sie auch von lokalen Warnungen behandelt werden.  
  
Beim Verwalten von Ereignissen in einer Multiserverumgebung fallen die folgenden allgemeinen Aufgaben an:  
  
**So bestimmen Sie einen Server zum Warnungsverwaltungsserver**  
  
-   [SQL Server Management Studio](../content/Designate-an-Events-Forwarding-Server--SQL-Server-Management-Studio-.md)  
  
**So definieren Sie die Antwort auf eine Warnung**  
  
-   [SQL Server Management Studio](../content/Define-the-Response-to-an-Alert--SQL-Server-Management-Studio-.md)  
  
-   [Transact-SQL](assetId:///0525e0a2-ed0b-4e69-8a4c-a9e3e3622fbd)  
  
## Veranstaltungen\-Aufträge ausgelöst  
Sie können einen Auftrag so definieren, dass er als Antwort auf eine Warnung ausgeführt werden soll. Sie können beispielsweise einen Auftrag ausführen, der ein von einer Warnung erkanntes Problem behebt oder weiter diagnostiziert.  
  
> [!NOTE]  
> Da ein Auftrag ein Ereignis auslösen kann, Sie darauf achten, nicht auf eine rekursive Warnung erstellen\-Auftrag Schleife.  
  
## Siehe auch  
[sp_add_notification (Transact-SQL)](assetId:///44bee7d9-7517-4071-99be-8b36f979c7cc)  
  
