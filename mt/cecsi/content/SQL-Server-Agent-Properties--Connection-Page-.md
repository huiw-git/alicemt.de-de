---
title: "SQL Server-Agent-Eigenschaften (Seite Verbindung)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d6a677ff-60ad-47ba-a0cb-df4193b165e0
caps.latest.revision: 3
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
# SQL Server-Agent-Eigenschaften (Seite Verbindung)
Mithilfe dieser Seite können Sie die Einstellungen für die Verbindung zwischen dem [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Dienst und [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]anzeigen und ändern.  
  
## Optionen  
**Aliasname für den lokalen Hostserver**  
Gibt den Aliasnamen an, der beim Verbinden zur lokalen Instanz von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verwendet wird. Wenn Sie die Standardoptionen der Verbindung für den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent nicht verwenden können, definieren Sie einen Alias für die Instanz, und geben Sie den Aliasnamen hier an.  
  
**Windows-Authentifizierung verwenden**  
Legt die [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] Windows-Authentifizierung als die Authentifizierungsmethode fest, die für die Verbindung mit der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Instanz verwendet wird. [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent wird als das Konto verbunden, als das der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Dienst ausgeführt wird.  
  
**SQL Server-Authentifizierung verwenden**  
Legt die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Authentifizierung als die Authentifizierungsmethode fest, die für die Verbindung mit der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Instanz verwendet wird.  
  
> [!IMPORTANT]  
> [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Authentifizierung wird aus Gründen der Abwärtskompatibilität bereitgestellt. Aus Sicherheitsgründen sollte möglichst die Windows-Authentifizierung verwendet werden.  
  
**Anmeldename**  
Gibt den Anmeldenamen an, der für die Verbindung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verwendet wird.  
  
**Kennwort**  
Gibt das Kennwort an, das für die Verbindung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verwendet wird.  
  
