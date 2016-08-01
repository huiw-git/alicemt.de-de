---
title: "Entfernen oder L&#246;schen eines Elements oder Projekts"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3fd92434-70f5-466e-bef0-7e0fd73ddb1c
caps.latest.revision: 3
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
# Entfernen oder L&#246;schen eines Elements oder Projekts
Projektelemente in [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)]-Projekten sind Abfragen, Verbindungen und sonstige Dateien. Sie können Projektabfragen und sonstige Dateien aus der Projektmappe löschen, ohne die Dateien aus dem Speicher zu löschen. Entfernen Sie ein Projekt oder Element, wenn es in der aktuellen Projektmappe nicht nützlich ist und in eine andere Projektmappe eingefügt werden soll.  
  
### So entfernen Sie ein Projektelement  
  
1.  Wählen Sie im Projektmappen-Explorer das Projektelement aus, das Sie entfernen möchten.  
  
2.  Auf der **Bearbeiten** Menü klicken Sie auf **Entfernen**.  
  
3.  Klicken Sie im Bestätigungsdialogfeld auf **Entfernen** aus dem Projekt entfernen.  
  
Ein entferntes Element ist weiterhin im Dateisystem vorhanden. Deshalb können Sie ein entferntes Element wieder zu seiner ursprünglichen oder zu einer anderen Projektmappe hinzufügen.  
  
#### So entfernen Sie ein Projekt  
  
1.  Wählen Sie im Projektmappen-Explorer das Projekt aus, das Sie entfernen möchten.  
  
2.  Auf der **Bearbeiten** Menü klicken Sie auf **Entfernen**.  
  
3.  Klicken Sie im Bestätigungsdialogfeld auf **OK**, um das Projekt aus der Projektmappe zu entfernen.  
  
Sie können ein Projekt dauerhaft löschen, müssen jedoch zuerst alle Verweise auf das Projekt aus [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)]-Projektmappen entfernen und dann die zugeordneten Dateien mithilfe von [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] Windows Explorer dauerhaft aus dem Speicher löschen.  
  
#### So löschen Sie ein Projekt  
  
1.  Entfernen Sie im Projektmappen-Explorer das Projekt, das Sie löschen möchten, aus der Projektmappe.  
  
2.  Suchen und markieren Sie in Windows Explorer die Dateien, die dem zu löschenden Projekt oder Element zugeordnet sind.  
  
3.  Auf der **Datei** Menü klicken Sie auf **Löschen**.  
  
## Siehe auch  
[Projektmappen-Explorer](../content/Solution-Explorer.md)  
[Hinzufügen neuer Elemente zu einem Projekt](../content/Add-New-Items-to-a-Project.md)  
[Hinzufügen vorhandener Elemente zu einem Projekt](../content/Add-Existing-Items-to-a-Project.md)  
  
