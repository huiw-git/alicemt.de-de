---
title: "Anzeigen der Auftragsaktivit&#228;t"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5c284e5e-7775-435d-ac49-f3f12a27ddc7
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
# Anzeigen der Auftragsaktivit&#228;t
In diesem Thema wird beschrieben, wie Sie den Laufzeitstatus von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Aufträgen in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] oder [!INCLUDE[tsql](../content/includes/tsql_md.md)]anzeigen können.  
  
Wenn der [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Dienst startet, wird eine neue Sitzung erstellt und die **sysjobactivity** -Tabelle in der **msdb** -Datenbank wird mit allen vorhandenen definierten Aufträgen aufgefüllt. In dieser Tabelle werden die aktuelle Auftragsaktivität und der aktuelle Auftragsstatus aufgezeichnet. Mithilfe des Auftragsaktivitätsmonitors im [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent können Sie den aktuellen Status von Aufträgen anzeigen. Falls der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Dienst unerwartet beendet wird, ersehen Sie aus der **sysjobactivity** -Tabelle, welche Aufträge ausgeführt wurden, als der Dienst beendet wurde.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Sicherheit](#Security)  
  
-   **So zeigen Sie die Auftragsaktivität an mit**  
  
    [SQL Server Management Studio](#SSMS)  
  
    [Transact-SQL](#TSQL)  
  
## Vorbereitungen  
  
### <a name="Security"></a>Sicherheit  
Ausführliche Informationen finden Sie unter [Implement SQL Server Agent Security](../content/Implement-SQL-Server-Agent-Security.md).  
  
## <a name="SSMS"></a>Verwendung von SQL Server Management Studio  
  
#### So zeigen Sie die Auftragsaktivität an  
  
1.  Stellen Sie im **Objekt-Explorer**eine Verbindung zu einer Instanz von [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)]her, und erweitern Sie dann diese Instanz.  
  
2.  Erweitern Sie **SQL Server-Agent**.  
  
3.  Rechts\-Klicken Sie auf **Auftragsaktivitätsmonitor** und klicken Sie auf **Anzeigen der Auftragsaktivität**.  
  
4.  Im **Auftragsaktivitätsmonitor**können Sie Details zu jedem Auftrag anzeigen, der für diesen Server definiert ist.  
  
5.  Rechts\-Klicken Sie auf einen Auftrag zum Starten, beenden, aktivieren oder deaktivieren, aktualisieren den Status im Auftragsaktivitätsmonitor angezeigt, löschen oder dessen Verlauf oder Eigenschaften anzeigen.  Wählen Sie zum Starten, beenden, aktivieren oder deaktivieren oder aktualisieren mehrere Aufträge, mehrere Zeilen im Auftragsaktivitätsmonitor, und rechts\-Klicken Sie auf Ihre Auswahl.  
  
6.  Klicken Sie auf **Aktualisieren**, um den Auftragsaktivitätsmonitor zu aktualisieren. Um weniger Zeilen anzuzeigen, klicken Sie auf **Filter** , und geben Sie Filterparameter ein.  
  
## <a name="TSQL"></a>Mithilfe von Transact\-SQL  
  
#### So zeigen Sie die Auftragsaktivität an  
  
1.  Stellen Sie im Objekt-Explorer ** **eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- lists activity for all jobs that the current user has permission to view.  
    USE msdb ;  
    GO  
  
    EXEC dbo.sp_help_jobactivity ;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_help_jobactivity (Transact-SQL)](assetId:///d344864f-b4d3-46b1-8933-b81dec71f511).  
  
