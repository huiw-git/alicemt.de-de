---
title: "Grundlegendes zur SQL Server Management Studio-Fensterverwaltung"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bebf8383-dcaf-466e-84f5-63b81c9cfe52
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
# Grundlegendes zur SQL Server Management Studio-Fensterverwaltung
Die Toolfenster in [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] ein funktionsreiches, flexible und effiziente System, das Ihnen ermöglicht, sind:  
  
-   Maximieren des Benutzerarbeitsbereichs für Entwicklungs- und Verwaltungsaufgaben.  
  
-   Reduzieren der Anzahl von nicht verwendeten Fenstern, die gleichzeitig angezeigt werden.  
  
-   Einfaches Anpassen der Benutzerumgebung.  
  
Das Bearbeiten von Fenstern ist für die [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)]-Umgebung äußerst wichtig. Die Benutzer können auf einfache Weise auf häufig verwendete Tools und Fenster zugreifen. Die Benutzer können steuern, wie viel Platz sie den unterschiedlichen Informationen zuordnen möchten, und die Umgebung maximiert entsprechend den verfügbaren Platz zur Bearbeitung von Abfragen. Fenster können auf dem Bildschirm an verschiedene Positionen verschoben werden. Viele Fenster können aus dem [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)]-Rahmen abgedockt und herausgezogen werden. Dies ist vor allem nützlich, wenn Sie mehr als einen Bildschirm verwenden.  
  
Um den Bearbeitungsbereich bei gleichzeitiger Beibehaltung der Funktionalität zu erweitern, ist in allen Fenstern eine Funktion zum automatischen Ausblenden vorhanden, mit der das Fenster als Registerkarte auf einer Leiste am Rand der [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)]-Hauptumgebung angezeigt wird. Wenn der Zeiger über eine dieser Registerkarten bewegt wird, wird das entsprechende Fenster angezeigt. Automatische ausblenden ein Fensters gewechselt werden kann, indem Sie auf die **automatisch im Hintergrund** Schaltfläche, dargestellt durch einen PIN in der oberen\-rechte Ecke des Fensters. Es gibt auch eine **Alle automatisch ausblenden** option die **Fenster** Menü.  
  
Einige Komponenten lassen sich sowohl im Registerformatmodus konfigurieren, in dem Komponenten als Registerkarten an derselben Andockposition angezeigt werden, als auch im MDI-Modus (Multiple Document Interface), in dem jedes Dokument in einem eigenen Fenster angezeigt wird. So konfigurieren Sie diese Funktion auf die **Tools** Menü klicken Sie auf **Optionen**, klicken Sie auf **Umgebung**, und klicken Sie dann auf **Allgemeine**.  
  
> [!IMPORTANT]  
> Wenn für einen Anmeldenamen (oder den Benutzer einer eigenständigen Datenbank) eine Verbindung hergestellt und dieser authentifiziert wird, werden von der Verbindung Identitätsinformationen zum Anmeldenamen gespeichert. Bei einer Anmeldung unter Verwendung der Windows-Authentifizierung umfassen die Informationen Angaben zur Mitgliedschaft in Windows-Gruppen. Die Identität der Anmeldung bleibt für die Dauer der Verbindung authentifiziert. Um Identitätsänderungen zu erzwingen, z. B. das Zurücksetzen eines Kennworts oder eine Änderung der Windows-Gruppenmitgliedschaft, muss die Anmeldung von der Authentifizierungsstelle (Windows oder [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]) abgemeldet und erneut angemeldet werden. Ein Mitglied der **Sysadmin** feste Serverrolle oder eine beliebige Anmeldung mit der **ALTER ANY CONNECTION** Berechtigung können die **KILL** Befehl aus, um eine Verbindung und eine Anmeldung Verbindung zu erzwingen. [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] Verbindungsinformationen können wiederverwendet werden, wenn mehrere Verbindungen zu Objekt-Explorer und Abfrage-Editor zu öffnen. Schließen Sie alle Verbindungen, um eine erneute Verbindung zu erzwingen.  
  
> [!IMPORTANT]  
> Wenn für eine Anmeldung (oder den Benutzer einer eigenständigen Datenbank) eine Verbindung hergestellt und diese authentifiziert wird, werden von der Verbindung Identitätsinformationen zur Anmeldung zwischengespeichert. Bei einer Anmeldung unter Verwendung der Windows-Authentifizierung umfassen die Informationen Angaben zur Mitgliedschaft in Windows-Gruppen. Die Identität der Anmeldung bleibt für die Dauer der Verbindung authentifiziert. Um Identitätsänderungen zu erzwingen, z. B. das Zurücksetzen eines Kennworts oder eine Änderung der Windows-Gruppenmitgliedschaft, muss die Anmeldung von der Authentifizierungsstelle (Windows oder [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]) abgemeldet und erneut angemeldet werden. Ein Mitglied der **Sysadmin** feste Serverrolle oder eine beliebige Anmeldung mit der **ALTER ANY CONNECTION** Berechtigung können die **KILL** Befehl aus, um eine Verbindung und eine Anmeldung Verbindung zu erzwingen. [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] Verbindungsinformationen können wiederverwendet werden, wenn mehrere Verbindungen zu Objekt-Explorer und Abfrage-Editor zu öffnen. Schließen Sie alle Verbindungen, um eine erneute Verbindung zu erzwingen.  
  
## Siehe auch  
[Verwenden von SQL Server Management Studio](../content/Use-SQL-Server-Management-Studio.md)  
[Die SQL Server Management Studio-Umgebung](../content/The-SQL-Server-Management-Studio-Environment.md)  
  
