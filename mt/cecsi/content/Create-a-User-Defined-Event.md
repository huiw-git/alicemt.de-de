---
title: "Erstellen eines benutzerdefinierten Ereignisses"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 03d71a35-97fa-4bba-aa9a-23ac9c9cf879
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
# Erstellen eines benutzerdefinierten Ereignisses
Sie können die Benutzer erstellen\-Ereignisse definiert, gegebenenfalls zu Ereignissen Weitere Ereignisse überwachen, die vordefinierten [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]. Sie können auch einen Schweregrad zuweisen, für jeden Benutzer\-Ereignis definiert.  
  
> [!NOTE]  
> Verwendung von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)], wählen die **in Windows-Anwendungsereignisprotokoll schreiben** Option für jeden Benutzer\-definiert die Meldung, um sicherzustellen, dass die Nachrichten protokolliert werden. In der Standardeinstellung Benutzer\-definierten Nachrichten mit einem Schweregrad kleiner als 19 werden nicht an die [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] Windows-Anwendungsprotokoll, wenn sie auftreten. Benutzer\-definierten Meldungen mit einem Schweregrad niedriger als 19 daher keine Warnungen des SQL Server-Agent aus.  
  
Benutzer\-definierten Ereignisse müssen eine eindeutige Meldungsnummer besitzen. Nachricht für einen Benutzer Zahlen\-definiertes Ereignis muss größer als 50.000 sein. Meldungen für das Ereignis können in mehreren Sprachen definiert werden. Allerdings eine **En\-US** Fehlermeldung muss vorhanden sein, bevor Nachrichten in anderen Sprachen hinzugefügt werden können.  
  
Wenn Sie ein Vielfaches verwalten\-Language [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Umgebung erstellen Benutzer\-definierten Nachrichten in allen Sprachen, die unterstützt werden. Wenn Sie beispielsweise eine neue Ereignismeldung erstellen, die sowohl auf einem deutschen als auch auf einem englischen Server verwendet werden soll, können Sie für beide dieselbe Meldungsnummer und denselben Schweregrad verwenden, müssen ihnen jedoch unterschiedliche Sprachen zuweisen.  
  
Die folgenden Aufgaben finden Sie Informationen dazu, wie Sie Benutzer erstellen\-Ereignisse und die dazugehörigen Warnungen definiert:  
  
**So erstellen Sie eine Warnung auf der Grundlage einer Meldungsnummer**  
  
-   [SQL Server Management Studio](../content/Create-an-Alert-Using-an-Error-Number.md)  
  
-   [Transact-SQL](assetId:///d9b41853-e22d-4813-a79f-57efb4511f09)  
  
**So erstellen Sie eine Warnung auf der Grundlage von Schweregraden**  
  
-   [SQL Server Management Studio](../content/Create-an-Alert-Using-Severity-Level.md)  
  
-   [Transact-SQL](assetId:///d9b41853-e22d-4813-a79f-57efb4511f09)  
  
**So definieren Sie die Antwort auf eine Warnung**  
  
-   [SQL Server Management Studio](../content/Define-the-Response-to-an-Alert--SQL-Server-Management-Studio-.md)  
  
-   [Transact-SQL](assetId:///0525e0a2-ed0b-4e69-8a4c-a9e3e3622fbd)  
  
**Zum Erstellen eines Benutzers\-Ereignisfehlermeldung definiert**  
  
-   [Transact-SQL](assetId:///54746d30-f944-40e5-a707-f2d9be0fb9eb)  
  
**Bearbeiten eines Benutzers\-Ereignisfehlermeldung definiert**  
  
-   [Transact-SQL](assetId:///1b28f280-8ef9-48e9-bd99-ec14d79abaca)  
  
**Zum Löschen eines Benutzers\-Ereignisfehlermeldung definiert**  
  
-   [Transact-SQL](assetId:///17287a15-cdde-43d1-bb18-9f920bc15db8)  
  
**So deaktivieren oder reaktivieren Sie eine Warnung**  
  
-   [SQL Server Management Studio](../content/Disable-or-Reactivate-an-Alert.md)  
  
-   [Transact-SQL](assetId:///4bbaeaab-8aca-4c9e-abc1-82ce73090bd3)  
  
## Siehe auch  
[sp_update_alert (Transact-SQL)](assetId:///4bbaeaab-8aca-4c9e-abc1-82ce73090bd3)  
  
