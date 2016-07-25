---
title: "Vollziehen des Austritts mehrerer Zielserver aus einem Masterserver"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 61a3713b-403a-4806-bfc4-66db72ca1156
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
# Vollziehen des Austritts mehrerer Zielserver aus einem Masterserver
In diesem Thema wird beschrieben, wie Sie den Austritt mehrerer Zielserver aus einer Multiserver-Verwaltungskonfiguration in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)]vollziehen. Führen Sie die folgenden Schritte auf dem Masterserver aus.  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So tragen Sie bei einem Masterserver mehrere Zielserver aus  
  
1.  Erweitern Sie im **Objekt-Explorer**einen Server, der als Masterserver konfiguriert ist.  
  
2.  Rechts\-Klicken Sie auf **SQL Server-Agent**, zeigen Sie auf **Multiserveradministration**, und klicken Sie dann auf **Zielserver verwalten**.  
  
3.  Klicken Sie auf **Anweisungen bereitstellen**, und klicken Sie in der Liste **Anweisungstyp** auf **Austragen**.  
  
4.  Führen Sie unter **Empfänger**eine der folgenden Aktionen aus:  
  
    -   Klicken Sie auf **Alle Zielserver** , um alle Zielserver dieses Masterservers auszutragen. Verwenden Sie diese Option, wenn die aktuelle Multiserververwaltungskonfiguration vollständig deinstalliert werden soll.  
  
    -   Klicken Sie auf **Diese Zielserver**, und klicken Sie dann auf das entsprechende Feld **Auswählen** , um einige, aber nicht alle Zielserver dieses Masterservers auszutragen.  
  
## Siehe auch  
[Erstellen einer Multiserverumgebung](../content/Create-a-Multiserver-Environment.md)  
[Automatisierte Verwaltung in einem Unternehmen](../content/Automated-Administration-Across-an-Enterprise.md)  
[Vollziehen des Austritts eines Zielservers aus einem Masterserver](../content/Defect-a-Target-Server-from-a-Master-Server.md)  
  
