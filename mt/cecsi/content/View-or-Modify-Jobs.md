---
title: "Anzeigen oder &#196;ndern von Auftr&#228;gen"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 57f649b8-190c-4304-abd7-7ca5297deab7
caps.latest.revision: 4
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
# Anzeigen oder &#196;ndern von Auftr&#228;gen
Jeden Auftrag, den Sie erstellt haben, können Sie anzeigen. Nachdem Sie einen Auftrag ausgeführt haben, können Sie auch den Auftragsverlauf anzeigen. Auf diese Weise erfahren Sie, wann der Auftrag ausgeführt wurde, den Status des Auftrags insgesamt sowie den Status jedes Auftragsschritts. Sie sehen, ob bei dem Auftrag in der Vergangenheit jemals ein Fehler aufgetreten ist, wann der Auftrag zuletzt erfolgreich ausgeführt wurde sowie welche Ausgabe bei jeder Ausführung des Auftrags erstellt wurde. Mitglieder der **Sysadmin** festen Serverrollen anzeigen oder jeden Auftrag, unabhängig vom Besitzer ändern kann.  
  
> [!NOTE]  
> Ein Auftrag muss mindestens einmal ausgeführt worden sein, damit ein Auftragsverlauf vorhanden ist. Sie können die Gesamtgröße des Auftragsverlaufsprotokolls und die Größe pro Auftrag begrenzen.  
  
Schließlich können Sie einen Auftrag an neue Anforderungen anpassen. Sie können Folgendes ändern:  
  
-   Benachrichtigungsoptionen  
  
-   Zeitpläne  
  
-   Auftragsschritte  
  
-   Besitzer  
  
-   Auftragskategorie  
  
-   Zielserver (ausschließlich bei Multiserveraufträgen)  
  
Wenn Sie Änderungen an Multiserveraufträgen vornehmen, müssen Sie die Änderungen der Downloadliste bereitstellen, damit die Zielserver den aktualisierten Auftrag herunterladen können. Um sicherzustellen, dass die Zielserver über die aktuellsten Auftragsdefinitionen verfügen, führen Sie nach dem Aktualisieren des Multiserverauftrags wie folgt eine INSERT-Anweisung aus:  
  
```  
EXECUTE sp_post_msx_operation 'INSERT', 'JOB', '<job id>'  
```  
  
Weitere Informationen finden Sie unter [Sp_purge_jobhistory (Transact-SQL)](assetId:///237f9bad-636d-4262-9bfb-66c034a43e88).  
  
Mitglieder der **Sysadmin** festen Serverrolle kann die Definition oder den Verlauf jedes Auftrags anzeigen und können jeden Auftrag ändern.  
  
## Verwandte Aufgaben  
  
|||  
|-|-|  
|**Beschreibung**|**Thema**|  
|Beschreibt das Anzeigen von [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Aufträge.|[Anzeigen eines Auftrags](../content/View-a-Job.md)|  
|Beschreibt das Anzeigen der [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Auftragsverlaufsprotokoll Agent.|[Anzeigen des Auftragsverlaufs](../content/View-the-Job-History.md)|  
|Beschreibt, wie Sie das Löschen des Inhalts der [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Auftragsverlaufsprotokoll Agent.|[Löschen des Auftragsverlaufsprotokolls](../content/Clear-the-Job-History-Log.md)|  
|Beschreibt, wie Sie größenbeschränkungen für [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agents.|[Ändern der Größe des Auftragsverlaufsprotokolls](../content/Resize-the-Job-History-Log.md)|  
|Beschreibt, wie Sie die Eigenschaften ändern [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Aufträge.|[Ändern eines Auftrags](../content/Modify-a-Job.md)|  
  
## Siehe auch  
[sysjobhistory](assetId:///1b1fcdbb-2af2-45e6-bf3f-e8279432ce13)  
  
