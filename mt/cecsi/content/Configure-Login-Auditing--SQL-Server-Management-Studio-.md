---
title: "Konfigurieren der Anmeldungs&#252;berwachung (SQL Server Management Studio)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 16961116-57ac-4eef-8037-791b26ade548
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
# Konfigurieren der Anmeldungs&#252;berwachung (SQL Server Management Studio)
In diesem Thema wird beschrieben, wie die Anmeldeüberwachung in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] konfiguriert wird, um die [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)]-Anmeldeaktivität zu überwachen. Die Anmeldungsüberwachung kann so konfiguriert werden, dass die folgenden Ereignisse im Fehlerprotokoll aufgezeichnet werden.  
  
-   Fehlgeschlagene Anmeldungen  
  
-   Erfolgreiche Anmeldungen  
  
-   Erfolgreiche und fehlgeschlagene Anmeldungen  
  
Sie müssen [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] neu starten, damit die Option wirksam wird.  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So konfigurieren Sie die Anmeldungsüberwachung  
  
1.  Stellen Sie in [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] mithilfe des Objekt-Explorers eine Verbindung mit einer Instanz von [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)] her.  
  
2.  Mit der rechten Maustaste im Objekt-Explorer\-Klicken Sie auf den Namen des Servers, und klicken Sie dann auf **Eigenschaften**.  
  
3.  Auf der **Sicherheit** Seite **Anmeldung** Überwachung, klicken Sie auf die gewünschte Option, und schließen Sie die **Servereigenschaften** Seite.  
  
4.  Mit der rechten Maustaste im Objekt-Explorer\-Klicken Sie auf den Namen des Servers, und klicken Sie dann auf **Neustart**.  
  
