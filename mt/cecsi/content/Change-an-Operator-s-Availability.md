---
title: "&#196;ndern der Verf&#252;gbarkeit eines Operators"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 10d58b92-b67b-47e2-af9c-9f9fd6968bba
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
# &#196;ndern der Verf&#252;gbarkeit eines Operators
In diesem Thema wird beschrieben, wie der Zeitplan für den Empfang von Warnmeldungen für einen Operator in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] oder [!INCLUDE[tsql](../content/includes/tsql_md.md)]geändert wird.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Sicherheit](#Security)  
  
-   **So ändern Sie die Verfügbarkeit eines Operators mit**  
  
    [SQL Server Management Studio](#SSMSProcedure)  
  
    [Transact-SQL](#TsqlProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Nur Mitglieder der festen Serverrolle **sysadmin** können Operatoren bearbeiten.  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So ändern Sie die Verfügbarkeit eines Operators  
  
1.  Klicken Sie im **Objekt-Explorer**auf das Pluszeichen, um den Server zu erweitern, der den Operator enthält, auf dem Sie die Indizes aktivieren möchten.  
  
2.  Klicken Sie auf das Pluszeichen, um **SQL Server-Agent**zu erweitern.  
  
3.  Klicken Sie auf das Pluszeichen, um den Ordner **Operatoren** zu erweitern.  
  
4.  Rechts\-Klicken Sie auf den Operator, den Sie verwenden möchten, aktivieren oder deaktivieren, und wählen Sie **Eigenschaften**, klicken Sie dann auf die **Allgemein** Registerkarte.  
  
5.  In der *Operator\_Namen***Eigenschaften** Dialogfeld aktivieren oder Deaktivieren der **aktiviert** das Kontrollkästchen.  
  
6.  Klicken Sie auf **OK**.  
  
## <a name="TsqlProcedure"></a>Mithilfe von Transact\-SQL  
  
#### So ändern Sie die Verfügbarkeit eines Operators  
  
1.  Stellen Sie im Objekt-Explorer ** **eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- disables the 'François Ajenstat' operator  
    USE msdb ;  
    GO  
  
    EXEC dbo.sp_update_operator   
        @name = N'François Ajenstat',  
        @enabled = 0;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_update_operator (Transact-SQL)](assetId:///231750a6-4828-4d03-afe6-b91d38c42ed3).  
  
