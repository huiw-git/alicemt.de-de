---
title: "Auflisten von Informationen zu Auftragskategorien"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0fc668d4-6244-4fef-b90e-62d2c776cd7c
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
# Auflisten von Informationen zu Auftragskategorien
In diesem Thema wird beschrieben, wie Sie Auftragskategorieinformationen in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[tsql](../content/includes/tsql_md.md)] oder SQL Server Management Objects auflisten können.  
  
-   **Vorbereitungen:**  
  
    [Sicherheit](#Security)  
  
-   **So listen Sie Informationen zu Auftragskategorien auf, und zwar mit**  
  
    [Transact-SQL](#TSQL)  
  
    [SQL Server Management Objects](#SMO)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Security"></a>Sicherheit  
Ausführliche Informationen finden Sie unter [Implement SQL Server Agent Security](../content/Implement-SQL-Server-Agent-Security.md).  
  
## <a name="TSQL"></a>Mithilfe von Transact\-SQL  
  
#### So listen Sie Informationen zu Auftragskategorien auf  
  
1.  Stellen Sie im **Objekt-Explorer**eine Verbindung mit einer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Instanz her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
    ```  
    -- returns information about jobs that are administered locally  
    USE msdb ;  
    GO  
  
    EXEC dbo.sp_help_category  
        @type = N'LOCAL' ;  
    GO  
    ```  
  
Weitere Informationen finden Sie unter [Sp_help_category (Transact-SQL)](assetId:///8cad1dcc-b43e-43bd-bea0-cb0055c84169).  
  
## <a name="SMO"></a>Verwendung von SQL Server Management Objects  
**So listen Sie Informationen zu Auftragskategorien auf**  
  
Verwenden der **JobCategory** Klasse, indem Sie eine Programmiersprache, die Sie, wie z. B. Visual Basic, Visual C# auswählen\#, oder PowerShell.  
  
