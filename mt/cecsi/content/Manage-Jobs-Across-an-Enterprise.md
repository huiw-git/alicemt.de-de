---
title: "Verwalten von Auftr&#228;gen &#252;ber ein gesamtes Unternehmen"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4fe7f6c6-f89b-4430-979c-4994a5dcf7a6
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
# Verwalten von Auftr&#228;gen &#252;ber ein gesamtes Unternehmen
Wenn Sie Definitionen von Multiserveraufträgen außerhalb ändern [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)], Sie müssen die Änderungen der Downloadliste bereitstellen, damit die Zielserver erneut des aktualisierten Auftrags herunterladen können. Um sicherzustellen, dass die Zielserver über aktuelle Auftragsdefinitionen verfügen, führen Sie nach dem Aktualisieren des Multiserverauftrags eine INSERT-Anweisung aus:  
  
```  
EXECUTE sp_post_msx_operation 'INSERT', 'JOB', '<job id>'  
```  
  
Um Zielserver darüber zu benachrichtigen, dass ein Multiserverauftrag geändert wurde, müssen Sie den vorherigen Befehl aufrufen, nachdem Sie eine der folgenden Prozeduren verwendet haben:  
  
-   [sp_add_jobstep (Transact-SQL)](assetId:///97900032-523d-49d6-9865-2734fba1c755)  
  
-   [sp_update_jobstep (Transact-SQL)](assetId:///e158802c-c347-4a5d-bf75-c03e5ae56e6b)  
  
-   [sp_delete_jobstep (Transact-SQL)](assetId:///421ede8e-ad57-474a-9fb9-92f70a3e77e3)  
  
-   [Verwalten von Ereignissen](assetId:///80c80eaf-cf23-4ed8-b8dd-65fe59830dd1)  
  
-   [sp_detach_schedule (Transact-SQL)](assetId:///9a1fc335-1bef-4638-a33a-771c54a5dd19)  
  
    > [!NOTE]  
    > Es ist nicht notwendig, rufen Sie **sp\_buchen\_Msx\_Vorgang** nach dem Aufruf von **sp\_Aktualisieren\_Auftrag** oder **sp\_Löschen\_Auftrag**, da diese gespeicherten Prozeduren automatisch die erforderlichen Änderungen der Downloadliste bereitstellen.  
  
Mithilfe der folgenden Tasks werden häufig Aufträge über ein gesamtes Unternehmen hinweg verwaltet:  
  
**So überprüfen Sie den Status eines Zielservers**  
  
-   [Transact-SQL](assetId:///f841d3bd-901a-4980-ad0b-1c6eeba3f717)  
  
-   [SQL Server Management Objects (SMO)](assetId:///4cde2b85-2a31-4cac-8d16-7a4196066193)  
  
**So wechseln Sie die Zielserver für einen Auftrag**  
  
-   [SQL Server Management Studio](../content/Modify-the-Target-Servers-for-a-Job.md)  
  
-   [Transact-SQL](assetId:///485252cc-0081-490a-9bd1-cbbd68eea286)  
  
-   [SQL Server Management Objects (SMO)](assetId:///4cde2b85-2a31-4cac-8d16-7a4196066193)  
  
**So ändern Sie den Speicherort eines Zielservers**  
  
-   [SQL Server Management Studio](../content/Specify-a-Target-Server-s-Location--SQL-Server-Management-Studio-.md)  
  
-   [Transact-SQL](assetId:///ceb3b2bc-0cc4-48d8-9bdc-6a809556e35f)  
  
-   [SQL Server Management Objects (SMO)](assetId:///4cde2b85-2a31-4cac-8d16-7a4196066193)  
  
**So synchronisieren Sie die Uhren der Zielserver**  
  
-   [SQL Server Management Studio](../content/Synchronize-Target-Server-Clocks--SQL-Server-Management-Studio-.md)  
  
-   [Transact-SQL](assetId:///40e44df7-d3e3-44ee-b149-08aba629a21f)  
  
**So erzwingen Sie, dass ein Zielserver den Masterserver abruft**  
  
-   [SQL Server Management Studio](../content/Force-a-Target-Server-to-Poll-the-Master-Server.md)  
  
-   [Transact-SQL](assetId:///085deef8-2709-4da9-bb97-9ab32effdacf)  
  
## Siehe auch  
[Verwalten von Ereignissen](../content/Manage-Events.md)  
  
