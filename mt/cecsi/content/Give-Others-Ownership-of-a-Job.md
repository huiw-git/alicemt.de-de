---
title: "Give Others Ownership of a Job"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2ded5e9c-4251-4fb1-a047-99f13d150b61
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
# Give Others Ownership of a Job
In diesem Thema wird beschrieben, wie Sie den Besitz eines [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agentauftrags einem anderen Benutzer neu zuweisen können.  
  
-   **Vorbereitungen:**  [Einschränkungen](#Restrictions), [Sicherheit](#Security)  
  
-   **So ändern Sie den Besitz eines Auftrags mit:**  
  
    [SQL Server Management Studio](#SSMSProc2)  
  
    [Transact-SQL](#TsqlProc2)  
  
    [SQL Server Management Objects](#SMOProc2)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
Um einen Auftrag erstellen zu können, muss ein Benutzer Mitglied einer der festen Datenbankrollen des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agents oder Mitglied der festen Serverrolle **sysadmin** sein. Ein Auftrag kann nur von seinem Besitzer bzw. Mitgliedern der **sysadmin** -Rolle bearbeitet werden. Weitere Informationen zu den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent festen Datenbankrollen finden Sie unter [SQL Server-Agent-festen Datenbankrollen](../content/SQL-Server-Agent-Fixed-Database-Roles.md).  
  
Den Besitzer eines Auftrags können Sie nur ändern, wenn Sie als Systemadministrator angemeldet sind.  
  
Wenn Sie einen Auftrag einem anderen Anmeldenamen zuweisen, ist nicht sichergestellt, dass die Berechtigungen des neuen Besitzers zum erfolgreichen Ausführen des Auftrags ausreichen.  
  
### <a name="Security"></a>Sicherheit  
Aus Sicherheitsgründen kann nur der Auftragsbesitzer bzw. ein Mitglied der **sysadmin** -Rolle die Definition des Auftrags ändern. Nur Mitglieder der festen Serverrolle **sysadmin** können anderen Benutzern den Auftragsbesitz zuweisen. Zudem können sie unabhängig vom Auftragsbesitzer alle Aufträge ausführen.  
  
> [!NOTE]  
> Wenn Auftragsbesitz einem Benutzer ändern, der kein Mitglied von der **Sysadmin** festen Serverrolle und der Auftrag Schritte ausgeführt werden, die Proxykonten erforderlich sind (z. B. [!INCLUDE[ssIS](../content/includes/ssIS_md.md)] Ausführung von Paketen), stellen Sie sicher, dass der Benutzer hat Zugriff auf dieses Proxykonto, sonst schlägt der Auftrag fehl.  
  
#### <a name="Permissions"></a>Berechtigungen  
Ausführliche Informationen finden Sie unter [Implement SQL Server Agent Security](../content/Implement-SQL-Server-Agent-Security.md).  
  
## <a name="SSMSProc2"></a>Verwendung von SQL Server Management Studio  
**So ändern Sie den Besitz eines Auftrags**  
  
1.  Stellen Sie im **Objekt-Explorer** eine Verbindung mit einer Instanz von [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)]her, und erweitern Sie dann diese Instanz.  
  
2.  Erweitern Sie **SQL Server-Agent**, erweitern Sie **Aufträge**, mit der rechten Maustaste\-Klicken Sie auf den Auftrag, und klicken Sie dann auf **Eigenschaften**.  
  
3.  Wählen Sie aus der Liste **Besitzer** einen Anmeldenamen aus. Den Besitzer eines Auftrags können Sie nur ändern, wenn Sie als Systemadministrator angemeldet sind.  
  
    Wenn Sie einen Auftrag einem anderen Anmeldenamen zuweisen, ist nicht sichergestellt, dass die Berechtigungen des neuen Besitzers zum erfolgreichen Ausführen des Auftrags ausreichen.  
  
## <a name="TsqlProc2"></a>Mithilfe von Transact\-SQL  
**So ändern Sie den Besitz eines Auftrags**  
  
1.  Stellen Sie im Objekt-Explorer eine Verbindung mit einer Instanz von Database Engine (Datenbankmodul) her, und erweitern Sie dann diese Instanz.  
  
2.  Klicken Sie auf der Symbolleiste auf **Neue Abfrage**.  
  
3.  Geben Sie im Abfragefenster die folgenden Anweisungen, mit denen die [Sp_manage_jobs_by_login (Transact-SQL)](assetId:///832ec15a-6e92-4eb5-8c4a-af4dba79fbaa) gespeicherten Systemprozedur. Im folgenden Beispiel erfolgt eine Neuzuweisung aller Aufträge von `danw` an `françoisa`.  
  
    ```  
    USE msdb ;  
    GO  
  
    EXEC dbo.sp_manage_jobs_by_login  
        @action = N'REASSIGN',  
        @current_owner_login_name = N'danw',  
        @new_owner_login_name = N'françoisa' ;  
    GO  
    ```  
  
## <a name="SMOProc2"></a>Verwendung von SQL Server Management Objects  
**So ändern Sie den Besitz eines Auftrags**  
  
1.  Rufen Sie die **Auftrag** Klasse, indem Sie eine Programmiersprache, die Sie, wie z. B. Visual Basic, Visual C# auswählen\#, oder PowerShell. Beispielcode, finden Sie unter [Planen von automatischen, administrativen Tasks im SQL Server-Agent](assetId:///900242ad-d6a2-48e9-8a1b-f0eea4413c16).  
  
## Siehe auch  
[Implementieren von Aufträgen](../content/Implement-Jobs.md)  
[Erstellen von Aufträgen](../content/Create-Jobs.md)  
  
