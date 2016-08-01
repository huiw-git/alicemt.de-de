---
title: "Festlegen der Leerlaufzeit und Leerlaufdauer der CPU (SQL Server Management Studio)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8647b465-d899-4cc7-9640-134a506d0a2e
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
# Festlegen der Leerlaufzeit und Leerlaufdauer der CPU (SQL Server Management Studio)
In diesem Thema wird erläutert, wie Sie die CPU-Leerlaufbedingung für den Server in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mithilfe von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)]definieren. Die CPU-Leerlaufdefinition beeinflusst die Reaktion des [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agents auf Ereignisse. Nehmen wir beispielsweise an, dass Sie die CPU als im Leerlauf befindlich definieren, wenn die durchschnittliche CPU-Auslastung unter 10 Prozent fällt und für 10 Minuten auf dieser Stufe bleibt. Wenn Sie Aufträge definiert haben, die immer dann ausgeführt werden sollen, wenn die Server-CPU eine Leerlaufbedingung erfüllt, wird der Auftrag gestartet, wenn die CPU-Auslastung unter 10 Prozent fällt und für 10 Minuten auf dieser Stufe bleibt. Wenn es sich dabei um einen Auftrag handelt, der sich spürbar auf die Serverleistung auswirkt, ist die Art wichtig, wie Sie die CPU-Leerlaufbedingung definieren.  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So legen Sie die Leerlaufzeit und die Leerlaufdauer der CPU fest  
  
1.  Stellen Sie im **Objekt-Explorer** eine Verbindung mit einer Instanz von [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)]her, und erweitern Sie dann diese Instanz.  
  
2.  Rechts\-Klicken Sie auf **SQL Server-Agent**, klicken Sie auf **Eigenschaften**, und wählen Sie die **Erweitert** Seite.  
  
3.  Führen Sie unter **Bedingung für 'CPU im Leerlauf'**eine der folgenden Aktionen aus :  
  
    -   Aktivieren Sie **Bedingung für 'CPU im Leerlauf' definieren**.  
  
    -   Geben Sie einen Prozentsatz für die **Durchschnittliche CPU-Auslastung unterschreitet** Feld (für alle CPUs). Damit wird die Auslastungsgrenze festgelegt, unterhalb der die CPU als im Leerlauf befindlich angesehen wird.  
  
    -   Geben Sie einen Wert für Sekunden im Feld **und Verbleiben unterhalb dieser Stufe für** an. Damit wird die Dauer der minimalen CPU-Auslastung angegeben, bevor die CPU als im Leerlauf befindlich angesehen wird.  
  
