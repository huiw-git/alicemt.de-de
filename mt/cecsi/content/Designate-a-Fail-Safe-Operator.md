---
title: "Bestimmen eines Ausfallsicherheitsoperators"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0f4eb513-5c0a-4523-974e-e85c1deeb57f
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
# Bestimmen eines Ausfallsicherheitsoperators
Fail\-safe Operator ist ein Benutzer, der die Benachrichtigung erhält, wenn der vorgesehene Operator nicht erreicht werden kann. In diesem Thema wird beschrieben, wie ein Fehler festgelegt\-safe Operator zum Empfangen von [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent-warnbenachrichtigungen in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mit [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)].  
  
**In diesem Thema**  
  
-   **Vorbereitungen:**  
  
    [Einschränkungen](#Restrictions)  
  
    [Sicherheit](#Security)  
  
-   **Zuweisen einer Fail\-safe Operator mit:**  
  
    [SQL Server Management Studio](#SSMSProcedure)  
  
## <a name="BeforeYouBegin"></a>Vorbereitungen  
  
### <a name="Restrictions"></a>Einschränkungen  
  
-   Die Pager- und **net send** -Optionen werden in zukünftigen Versionen von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] nicht mehr im [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]. Vermeiden Sie die Verwendung dieser Funktionen bei neuen Entwicklungsarbeiten, und planen Sie die Änderung von Anwendungen, die diese Funktionen zurzeit verwenden.  
  
-   Beachten Sie, dass SQL Server-Agent konfiguriert werden müssen, um Datenbank-Mail verwenden, um e-Mail senden\-an Operatoren senden, e-Mail und Pager. Weitere Informationen finden Sie unter [Zuweisen von Warnungen zu einem Operator](http://msdn.microsoft.com/library/ms190038.aspx).  
  
-   [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] können Aufträge problemlos mithilfe einer grafischen Oberfläche verwaltet werden. Dies ist die empfohlene Vorgehensweise für die Erstellung und Verwaltung der Auftragsinfrastruktur.  
  
### <a name="Security"></a>Sicherheit  
  
#### <a name="Permissions"></a>Berechtigungen  
Nur Mitglieder der **Sysadmin** -Serverrolle kann Fehler festlegen\-sicher Operatoren.  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### Zuweisen einer Fail\-safe-Operator  
  
1.  In **Objekt-Explorer** Klicken Sie auf das Pluszeichen, um den Server zu erweitern, die den SQL Server-Agent-Operator enthält, die Sie als Fail festlegen möchten\-sicher.  
  
2.  Rechts\-Klicken Sie auf **SQL Server-Agent** und wählen Sie **Eigenschaften**.  
  
3.  In der **SQL Server-Agent-Eigenschaften –***Server\_Namen* Dialogfeld **Wählen Sie eine Seite**, Option **Warnungssystem**.  
  
4.  Unter **fehl\-safe Operator**, Option **Fail aktivieren\-safe Operator**.  
  
5.  In der **Operator** wählen Sie den Operator, der einen Fehler machen möchten\-sicher.  
  
6.  Wählen Sie beliebige oder alle der folgenden Kontrollkästchen, um anzugeben, wie der Operator benachrichtigt werden soll: **E\-Mail**, **Pager**, oder **Net Send**.  
  
7.  Wenn Sie fertig sind, klicken Sie auf **OK**.  
  
