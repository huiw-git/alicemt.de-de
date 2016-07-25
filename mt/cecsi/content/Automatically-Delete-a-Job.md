---
title: "Automatisches L&#246;schen eines Auftrags"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 92dbb6da-5919-4bde-9354-d454e9ea3da0
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
# Automatisches L&#246;schen eines Auftrags
In diesem Thema wird beschrieben, wie Sie den [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] konfigurieren können, um Aufträge mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] oder SQL Server Management Objects automatisch zu löschen, wenn sie erfolgreich, fehlerhaft oder abgeschlossen sind.  
  
Sie stellen sicher, dass Datenbankadministratoren wissen, wann Aufträge fertig gestellt sind und wie oft diese ausgeführt werden. Zu den typischen Auftragsantworten gehören folgende:  
  
-   Benachrichtigen den Operator per e\-e-Mail, elektronische auslagern, oder ein **net Send** Nachricht.  
  
    Verwenden Sie eine dieser Auftragsantworten, wenn der Operator Schritte ausführen muss\-Aktion einrichten. Wenn beispielsweise ein Sicherungsauftrag erfolgreich ausgeführt wurde, muss der Operator darüber informiert werden, um das Sicherungsband entfernen zu können und an einem sicheren Standort aufbewahren zu lassen.  
  
-   Schreiben einer Ereignismeldung in das Windows-Anwendungsprotokoll.  
  
    Diese Art der Antwort können Sie nur bei fehlgeschlagenen Aufträgen verwenden.  
  
-   Automatisches Löschen des Auftrags.  
  
    Verwenden Sie diese Auftragsantwort, wenn Sie sicher sind, dass Sie diesen Auftrag nicht erneut ausführen müssen.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Sicherheit](#Security)  
  
-   **So geben Sie Auftragsantworten an mit**  
  
    [SQL Server Management Studio](#SSMS)  
  
    [SQL Server Management Objects](#SMO)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Security"></a>Sicherheit  
Ausführliche Informationen finden Sie unter [Implement SQL Server Agent Security](../content/Implement-SQL-Server-Agent-Security.md).  
  
## <a name="SSMS"></a>Verwendung von SQL Server Management Studio  
  
#### So löschen Sie einen Auftrag automatisch  
  
1.  Stellen Sie im **Objekt-Explorer** eine Verbindung mit einer Instanz von [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)]her, und erweitern Sie dann diese Instanz.  
  
2.  Erweitern Sie **SQL Server-Agent**, erweitern Sie **Aufträge**, mit der rechten Maustaste\-Klicken Sie auf den Auftrag zu bearbeiten, und klicken Sie dann auf **Eigenschaften**.  
  
3.  Wählen Sie die Seite **Benachrichtigungen** aus.  
  
4.  Aktivieren Sie **Auftrag automatisch löschen**, und führen Sie eine der folgenden Handlungen aus:  
  
    -   Klicken Sie auf **Bei erfolgreicher Ausführung des Auftrags** , um den Auftragsstatus zu löschen, wenn der Auftrag erfolgreich abgeschlossen wurde.  
  
    -   Klicken Sie auf **Bei Auftragsfehler** , um den Auftrag zu löschen, wenn er nicht erfolgreich abgeschlossen wurde.  
  
    -   Klicken Sie auf **Beim Abschluss des Auftrags** , um den Auftrag unabhängig vom Abschlussstatus zu löschen.  
  
## <a name="SMO"></a>Verwendung von SQL Server Management Objects  
**So löschen Sie einen Auftrag automatisch**  
  
Verwenden der **DeleteLevel** Eigenschaft der **Auftrag** Klasse, indem Sie eine Programmiersprache, die Sie, wie z. B. Visual Basic, Visual C# auswählen\#, oder PowerShell. Weitere Informationen finden Sie unter [SQL Server Management Objects (SMO)](http://msdn.microsoft.com/library/ms162169.aspx).  
  
