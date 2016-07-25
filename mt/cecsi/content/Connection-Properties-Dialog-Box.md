---
title: "Verbindungseigenschaften (Dialogfeld)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6df812ad-4d80-4503-8a23-47719ce85624
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
# Verbindungseigenschaften (Dialogfeld)
Zeigen Sie mithilfe dieses Dialogfelds die aktuellen Verbindungseigenschaften an. Das Dialogfeld wird angezeigt, wenn Sie in verschiedenen Dialogfeldern des Objekt-Explorers auf **Verbindungseigenschaften anzeigen** klicken. Auf dieser Seite angezeigten Eigenschaften gelesen werden\-nur.  
  
Wenn Sie Eigenschaften, z. B. den Wert für **Datenbank**, ändern möchten, stellen Sie, bevor Sie das Dialogfeld **Verbindungseigenschaften** öffnen, mit dem Objekt-Explorer eine Verbindung zu der gewünschten Datenbank her.  
  
Beachten Sie, dass die Abfragezeit\-out Zeitraum für SQL Azure ist 30 Minuten.  
  
## Authentifizierung  
Zeigt die Authentifizierungseigenschaften für die aktuelle Verbindung an. Zu den Authentifizierungseigenschaften zählen der Anmeldename und die Authentifizierungsmethode, die beim Herstellen der Verbindung verwendet wurden. Zum Ändern der Authentifizierungseigenschaften trennen Sie die Verbindung zu [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)], und stellen Sie dann erneut eine Verbindung zwischen dem Objekt-Explorer und dem Server her, wobei Sie die gewünschten Verbindungsoptionen verwenden.  
  
**Authentifizierungsmethode**  
Für die aktuelle Verbindung verwendete Authentifizierungsmethode.  
  
**Benutzername**  
Bei der Verbindungsauthentifizierung für die Anmeldung verwendeter Benutzername.  
  
## Verbindungskategorie  
Zeigt die Verbindungseigenschaften für die aktuelle Verbindung an. Die meisten Verbindungseigenschaften wurden beim Herstellen der Verbindung auf der Registerkarte **Verbindungseigenschaften** des Dialogfelds **Verbindung mit Server herstellen** ausgewählt.  
  
**Datenbank**  
Name der Datenbank, mit der zurzeit eine Verbindung besteht. Diese Einstellung können Sie über die Symbolleiste des SQL-Editors ändern.  
  
**SPID**  
Der Verbindung durch den Server zugewiesene Systemprozess-ID. Diese kann für die Verbindung nicht geändert werden.  
  
**Netzwerkprotokoll**  
Das für die [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)]-Verbindung verwendete Netzwerkprotokoll. Zum Ändern dieser Größe stellen Sie mithilfe der gewünschten Verbindungseigenschaften die Verbindung erneut her.  
  
**Netzwerkpaketgröße**  
Bei der Kommunikation mit dem Server verwendete Netzwerkpaketgröße. Zum Ändern dieser Größe stellen Sie mithilfe der gewünschten Verbindungseigenschaften die Verbindung erneut her.  
  
**Verbindungstimeout**  
Die beim Herstellen einer Verbindung zu [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] abzuwartende Zeitdauer (in Sekunden), bevor ein Timeout eintritt und eine Fehlermeldung an den Benutzer ausgegeben wird. Zum Ändern dieser Größe stellen Sie mithilfe der gewünschten Verbindungseigenschaften die Verbindung erneut her.  
  
**Ausführungstimeout**  
Zeitdauer (in Sekunden), die auf den Abschluss eines Tasks auf dem Server gewartet werden soll. Zum Ändern dieser Größe stellen Sie mithilfe der gewünschten Verbindungseigenschaften die Verbindung erneut her.  
  
**Verschlüsselt**  
Gibt an, ob die aktuelle Verbindung verschlüsselt ist. Zum Ändern dieser Größe stellen Sie mithilfe der gewünschten Verbindungseigenschaften die Verbindung erneut her.  
  
## Product Category  
Zeigt die Produkteigenschaften für die aktuelle Verbindung an. Diese Eigenschaften beschreiben das Produkt, die Version, den Instanznamen und die Sortierung des Servers. Die Eigenschaften werden während der Installation von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] festgelegt.  
  
**Produktname**  
Der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Produktname.  
  
**Produktversion**  
Die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Produktversion.  
  
**Servername**  
Name des Computers, auf dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ausgeführt wird.  
  
**Instanzname**  
Der Instanzname des Servers. Die Standardinstanz ist leer.  
  
**Sprache**  
Sprachversion des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Produkts.  
  
**Sortierung**  
Die Sortierung des Servers.  
  
## Serverumgebungskategorie  
Zeigt die Serverumgebungseigenschaften für die aktuelle Verbindung in Bezug auf die Serverhardware und das Betriebssystem an. Diese Eigenschaften können mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] nicht konfiguriert werden.  
  
**Computername**  
Name des Servercomputers, auf dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ausgeführt wird.  
  
**Platform**  
Der Name und Hersteller des Betriebssystems sowie die CPU-Familie des Servers.  
  
**Betriebssystem**  
Auf dem Server installierte Version von [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] Windows.  
  
**Prozessoren**  
Anzahl der Prozessoren auf dem Server.  
  
**Arbeitsspeicher für das Betriebssystem**  
Der gesamte auf dem Server vorhandene physische Arbeitsspeicher in Megabytes.  
  
## Siehe auch  
[Eigenschaftenseiten in SQL Server Management Studio](../content/Property-Pages-in-SQL-Server-Management-Studio.md)  
[Verbinden Sie mit Server & #40; Anmeldeseite & #41; Datenbank-Engine](../content/Connect-to-Server--Login-Page--Database-Engine.md)  
  
