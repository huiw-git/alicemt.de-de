---
title: "Anzeigen eines SQL Server-Agent-Fehlerprotokolls (SQL Server Management Studio)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: de920425-fa44-469f-b83d-49e3f97e97f4
caps.latest.revision: 6
caps.handback.revision: 5
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
# Anzeigen eines SQL Server-Agent-Fehlerprotokolls (SQL Server Management Studio)
In diesem Thema wird das Anzeigen des  [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Fehlerprotokolls in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)]beschrieben.  
  
Im Protokolldatei-Viewer können Protokollinformationen aus einer Vielzahl von Komponenten angezeigt werden. Wählen Sie im geöffneten Protokolldatei-Viewer im Bereich **Protokolle auswählen** die Protokolle aus, die angezeigt werden sollen. In jedem Protokoll werden dem Protokolltyp entsprechende Spalten angezeigt. Welche Protokolle verfügbar sind, ist davon abhängig, wie der Protokolldatei-Viewer geöffnet wird.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Einschränkungen](#Restrictions)  
  
    [Sicherheit](#Security)  
  
-   [So zeigen Sie ein SQL Server-Agent-Fehlerprotokoll mithilfe von SQL Server Management Studio an](#SSMSProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
Der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Knoten wird nur im Objekt-Explorer angezeigt, wenn Sie die Berechtigung besitzen, ihn zu verwenden.  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent muss zur Verwendung der Anmeldeinformationen eines Kontos konfiguriert werden, das Mitglied der festen Serverrolle **sysadmin** in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]ist, um seine Funktionen ausführen zu können. Das Konto muss über die folgenden Windows-Berechtigungen verfügen:  
  
-   Anmelden als Dienst (SeServiceLogonRight)  
  
-   Ersetzen Sie einen Prozess\-Tokens auf Prozessebene (SeAssignPrimaryTokenPrivilege)  
  
-   Umgehen von durchsuchenden Prüfungen (SeChangeNotifyPrivilege)  
  
-   Anpassen des Arbeitsspeicherkontingents für einen Prozess (SeIncreaseQuotaPrivilege)  
  
Weitere Informationen zu den Windows-Berechtigungen erforderlich sind, für die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Dienstkonto finden Sie unter [Auswählen eines Kontos für SQL Server-Agent-Dienst](../content/Select-an-Account-for-the-SQL-Server-Agent-Service.md) und [Einrichten von Windows-Dienstkonten](assetId:///309b9dac-0b3a-4617-85ef-c4519ce9d014).  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So zeigen Sie das [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Fehlerprotokoll an  
  
1.  Klicken Sie im Objekt-Explorer ****auf das Pluszeichen, um den Server zu erweitern, der das [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Fehlerprotokoll enthält, das Sie anzeigen möchten.  
  
2.  Klicken Sie auf das Pluszeichen, um **SQL Server-Agent**zu erweitern.  
  
3.  Klicken Sie auf das Pluszeichen, um den Ordner **Fehlerprotokolle** zu erweitern.  
  
4.  Rechts\-Klicken Sie auf das Fehlerprotokoll, die Sie anzeigen möchten und wählen Sie **Agentprotokoll anzeigen**.  
  
    Die folgenden Optionen stehen in der **Protokolldatei-Viewer –***Server\_Namen* (Dialogfeld):  
  
    **Protokoll laden**  
    Öffnen Sie ein Dialogfeld, in dem Sie eine zu ladende Protokolldatei angeben können.  
  
    **Exportieren**  
    Öffnen Sie das Dialogfeld, mit dem Sie die Informationen zu exportieren, die in angezeigt wird der **protokolldateizusammenfassung** Raster in eine Textdatei.  
  
    **Aktualisieren**  
    Aktualisieren Sie die Anzeige der ausgewählten Protokolle. Beim Übernehmen von Filtereinstellungen werden mithilfe der Schaltfläche **Aktualisieren** die ausgewählten Protokolle erneut vom Zielserver gelesen.  
  
    **Filter**  
    Öffnen Sie das Dialogfeld, mit dem Sie die Einstellungen an, die verwendet werden, um die Protokolldatei, z. B. filtern **Verbindung**, **Datum**, oder andere **Allgemeine** Kriterien zu filtern.  
  
    **Suchen**  
    Durchsuchen Sie die Protokolldatei nach bestimmtem Text. Das Suchen mit Platzhalterzeichen wird nicht unterstützt.  
  
    **Beenden**  
    Beendet das Laden der Protokolldateieinträge. Diese Option können Sie z. B. verwenden, wenn das Laden einer Remote- oder Offline-Protokolldatei eine lange Zeit in Anspruch nimmt und Sie nur die zuletzt erstellten Einträge anzeigen möchten.  
  
    **Protokolldateizusammenfassung**  
    In diesem Informationsbereich wird eine Zusammenfassung der Protokolldateifilterung angezeigt. Wenn die Datei nicht gefiltert wurde, wird folgender Text angezeigt: **Kein Filter angewendet**. Wenn im Protokoll ein Filter angewendet wird, sehen Sie den folgenden Text, **Filtern von Protokolleinträgen, in denen:** <filter criteria>.  
  
    **Details für die ausgewählte Zeile**  
    Wählen Sie eine Zahl aus, um am unteren Rand der Seite zusätzliche Details zu der ausgewählten Ereigniszeile anzuzeigen. Die Spalten können durch Ziehen an neue Positionen im Raster neu angeordnet werden. Die Breite der Spalten kann durch Ziehen der Spaltentrennbalken in der Kopfzeile des Rasters nach links oder rechts geändert werden. Doppelte\-Klicken Sie auf die spaltentrennbalken in der Kopfzeile des Rasters automatisch die Größe der Spalte an die Breite des Inhalts.  
  
    **Instanz**  
    Der Name der Instanz, bei der das Ereignis aufgetreten ist. Dieser wird im Format *Computername*\\*Instanzname*.  
  
    **Datum**  
    Zeigt das Datum des Ereignisses an.  
  
    **Quelle**  
    Zeigt die Ausgangsfunktion an, mit dem das Ereignis erstellt wurde, z. B. den Namen des Diensts (z. B. MSSQLSERVER). Dies wird nicht für alle Protokolltypen angezeigt.  
  
    **MessageBox**  
    Zeigt die Meldungen an, die dem Ereignis zugeordnet sind.  
  
    **Protokolltyp**  
    Zeigt den Typ des Protokolls an, zu dem das Ereignis gehört. Alle ausgewählten Protokolle werden im Fenster für die Protokolldateizusammenfassung angezeigt.  
  
    **Protokollquelle**  
    Zeigt eine Beschreibung des Quellprotokolls an, in dem das Ereignis aufgezeichnet wird.  
  
5.  Wenn Sie fertig sind, klicken Sie auf **Schließen**.  
  
