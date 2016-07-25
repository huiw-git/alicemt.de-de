---
title: "Vollziehen des Austritts eines Zielservers aus einem Masterserver"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a6da262b-7b38-4ce4-bfd6-6a557c6e8a84
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
# Vollziehen des Austritts eines Zielservers aus einem Masterserver
In diesem Thema wird beschrieben, wie Sie den Austritt eines Zielservers aus einem Masterserver in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)], [!INCLUDE[tsql](../content/includes/tsql_md.md)] oder SQL Server Management Objects (SMO) vollziehen. Führen Sie die folgenden Schritte auf dem Zielserver aus.  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Sicherheit](#Security)  
  
-   **Vollziehen des Austritts eines Zielservers mit:**  
  
    [SQL Server Management Studio](#SSMSProcedure)  
  
    [Transact-SQL](#TsqlProcedure)  
  
    [SMO](#PowerShellProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Zum Ausführen dieser gespeicherten Prozedur muss ein Benutzer Mitglied der festen Serverrolle **sysadmin** sein.  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So tragen Sie bei einem Masterserver einen Zielserver aus  
  
1.  Erweitern Sie in **Objekt-Explorer**einen Server, der als Zielserver konfiguriert ist.  
  
2.  Rechts\-Klicken Sie auf **SQL Server-Agent**, zeigen Sie auf **Multiserveradministration**, und klicken Sie dann auf **Fehler**.  
  
3.  Klicken Sie auf **Ja** , um zu bestätigen, dass Sie diesen Zielserver bei einem Masterserver austragen möchten.  
  
## <a name="TsqlProcedure"></a>Mithilfe von Transact\-SQL  
  
#### So tragen Sie bei einem Masterserver einen Zielserver aus  
  
1.  Stellen Sie eine Verbindung mit dem [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]her.  
  
2.  Klicken Sie in der Standardleiste auf **Neue Abfrage**.  
  
3.  Kopieren Sie das folgende Beispiel, fügen Sie es in das Abfragefenster ein, und klicken Sie auf **Ausführen**.  
  
```  
sp_msx_defect ;  
```  
  
Weitere Informationen finden Sie unter [Sp_msx_defect (Transact-SQL)](assetId:///0dfd963a-3bc5-4b58-94f7-aec976da2883).  
  
## <a name="PowerShellProcedure"></a>Verwendung von SQL Server Management Objects (SMO)  
Verwenden Sie die **MsxDefect**-Methode.  
  
## Siehe auch  
[Erstellen einer Multiserverumgebung](../content/Create-a-Multiserver-Environment.md)  
[Automatisierte Verwaltung in einem Unternehmen](../content/Automated-Administration-Across-an-Enterprise.md)  
[Vollziehen des Austritts mehrerer Zielserver aus einem Masterserver](../content/Defect-Multiple-Target-Servers-from-a-Master-Server.md)  
  
