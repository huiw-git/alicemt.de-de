---
title: "Nach Servern suchen (Netzwerkserver)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a59ffcd6-4b69-4c5c-9740-699ccb2183fb
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
# Nach Servern suchen (Netzwerkserver)
Wenn Sie eine Verbindung mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Komponente herstellen und nicht den genauen Namen der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Instanz kennen, klicken Sie im Feld **Servername** auf **Suche fortsetzen** , um das Dialogfeld **Nach Servern suchen** zu öffnen.  
  
Dieses Dialogfeld wird vom [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Browser-Dienst aufgefüllt, sofern dieser auf den Servercomputern ausgeführt wird. Es gibt mehrere Gründe, warum der Name einer Instanz ggf. nicht in der Liste angezeigt wird:  
  
-   Der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Browser-Dienst wird auf dem Computer, auf dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]ausgeführt wird, möglicherweise nicht ausgeführt.  
  
-   UDP-Port 1434 wird möglicherweise von einer Firewall blockiert.  
  
-   Das **HideInstance** -Flag wurde möglicherweise festgelegt.  
  
Um zu einer Instanz herzustellen, die nicht in der Liste angezeigt wird, geben Sie eine vollständige Verbindungszeichenfolge für die Instanz, einschließlich TCP\/IP-Portnummer oder named Pipes pipe-Namen.  
  
## Optionen  
**Wählen Sie für Ihre Verbindung eine SQL Server-Instanz im Netzwerk aus**  
Legen Sie den Server fest, zu dem eine Verbindung hergestellt werden soll, indem Sie auf die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Instanz klicken, die in der Baumstruktur angezeigt wird. Sie können Teile der Strukturansicht durch Klicken auf die Knoten ein- bzw. ausblenden, die mit den Symbolen **\+** bzw. **–** gekennzeichnet sind.  
  
