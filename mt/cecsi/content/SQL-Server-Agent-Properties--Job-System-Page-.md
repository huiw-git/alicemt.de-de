---
title: "Eigenschaften des SQL Server-Agents (Registerkarte Auftragssystem)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e171d13e-1302-4f0e-88be-67d656aec8d3
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
# Eigenschaften des SQL Server-Agents (Registerkarte Auftragssystem)
Verwenden Sie diese Seite zum Anzeigen und Ändern der [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Dienst verwaltet die Aufträge.  
  
## Optionen  
**Zeit des Herunterfahrens\-Timeoutintervall (in Sekunden)**  
Gibt an, wie viele Sekunden der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent vor dem Herunterfahren den Abschluss von Aufträgen abwartet. Wenn der Auftrag noch nach dem angegebenen Intervall ausgeführt wird, wird die Beendigung von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] erzwungen.  
  
**Verwenden Sie einen anderen\-Proxy-Administratorkonto**  
Legt eine nicht\-Proxy-Administratorkonto für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent. [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssKatmai](../content/includes/ssKatmai_md.md)] und höhere Versionen unterstützen mehrere Proxys, daher diese Option ist nur gültig beim Verwalten von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent-Versionen vor [!INCLUDE[ssKatmai](../content/includes/ssKatmai_md.md)].  
  
**Benutzername**  
Geben Sie den Namen des Benutzers für die nicht\-Proxy-Administratorkonto. [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] unterstützt mehrere Proxys, daher diese Option ist nur anwendbar beim Verwalten von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent-Versionen vor [!INCLUDE[ssKatmai](../content/includes/ssKatmai_md.md)].  
  
**Kennwort**  
Geben Sie das Kennwort des Benutzers für die nicht\-Proxy-Administratorkonto. [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] und höhere Versionen unterstützen mehrere Proxys, daher diese Option ist nur gültig beim Verwalten von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent-Versionen vor [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)].  
  
**Domäne**  
Geben Sie die Domäne des Benutzers für die nicht\-administrative Proxykonto. [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] unterstützt mehrere Proxys, daher diese Option ist nur anwendbar beim Verwalten von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent-Versionen vor [!INCLUDE[ssKatmai](../content/includes/ssKatmai_md.md)].  
  
## Siehe auch  
[Implementieren von Aufträgen](../content/Implement-Jobs.md)  
  
