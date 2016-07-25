---
title: "Angeben eines Speicherortes des Zielservers (SQL Server Management Studio)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 511ff311-21f5-4f2f-839f-b4deee26ec98
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
# Angeben eines Speicherortes des Zielservers (SQL Server Management Studio)
In diesem Thema wird beschrieben, wie Sie den Speicherort eines Zielservers in einer Multiserververwaltungskonfiguration in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] oder [!INCLUDE[tsql](../content/includes/tsql_md.md)]angeben können.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Einschränkungen](#Restrictions)  
  
    [Sicherheit](#Security)  
  
-   **So geben Sie den Speicherort eines Zielservers an mit**  
  
    [SQL Server Management Studio](#SSMSProcedure)  
  
    [Transact-SQL](#TsqlProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
Wenn diese Aktion ausgeführt wird, wird die Registrierung bearbeitet. Die Registrierung sollte nicht manuell bearbeitet werden, da durch ungeeignete oder fehlerhafte Änderungen schwerwiegende Konfigurationsprobleme auf dem System verursacht werden können. Nur erfahrene Benutzer sollten deshalb den Registrierungs-Editor zum Bearbeiten der Registrierung verwenden. Weitere Informationen finden Sie in der Dokumentation zu Microsoft Windows.  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Erfordert die Mitgliedschaft in der festen Serverrolle **sysadmin** .  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So geben Sie den Speicherort eines Zielservers an  
  
1.  Klicken Sie im Objekt-Explorer ****auf das Pluszeichen, um den Masterserver zu erweitern, auf dem Sie den Speicherort des Zielservers angeben möchten.  
  
2.  Rechts\-Klicken Sie auf **SQL Server-Agent**, zeigen Sie auf **Multiserveradministration**, und wählen Sie **Zielserver verwalten**.  
  
3.  Rechts\-Klicken Sie auf einen Zielserver, und wählen Sie **Eigenschaften**.  
  
4.  Geben Sie in das Feld **Speicherort** einen Speicherort für den Server ein, und klicken Sie dann auf **OK**.  
  
## <a name="TsqlProcedure"></a>Mithilfe von Transact\-SQL  
  
#### So geben Sie den Speicherort eines Zielservers an  
  
1.  Stellen Sie im Objekt-Explorer ** **eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    USE msdb ;  
    GO  
    -- enlists the current server into the AdventureWorks1 master server.   
    -- The location for the current server is Building 21, Room 309, Rack 5  
    EXEC dbo.sp_msx_enlist N'AdventureWorks2012',   
        N'Building 21, Room 309, Rack 5' ;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_msx_enlist (Transact-SQL)](assetId:///ceb3b2bc-0cc4-48d8-9bdc-6a809556e35f).  
  
