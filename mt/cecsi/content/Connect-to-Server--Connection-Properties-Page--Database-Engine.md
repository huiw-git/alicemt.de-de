---
title: "Verbinden mit SQL Server-Datenbankmodul (Eigenschaftenseite Verbindung)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: edc1143c-6a47-4b02-92ab-441bdea8ea8a
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
# Verbinden mit SQL Server-Datenbankmodul (Eigenschaftenseite Verbindung)
Mit dieser Registerkarte können Optionen anzuzeigen oder anzugeben beim Verbinden mit einer Instanz von [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)] registrieren [!INCLUDE[ssDE](../content/includes/ssDE_md.md)] in **registrierte Server**. **Verbinden** und **Optionen** nur in diesem Dialogfeld angezeigt, wenn eine Verbindung zu einer Instanz von Herstellen der [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]. **Test** und **Speichern** nur in diesem Dialogfeld angezeigt, bei der Registrierung [!INCLUDE[ssDE](../content/includes/ssDE_md.md)].  
  
## Optionen  
**Verbindung mit Datenbank herstellen**  
Wählen Sie eine Datenbank aus der Liste aus, zu der eine Verbindung hergestellt werden soll. Wenn Sie die Option **<default>**, Sie werden auf die Standarddatenbank für den Server verbunden werden. Wenn Sie die Option **<Browse server>**, können Sie den Server für die Datenbank für die Verbindung durchsuchen.  
  
Beim Verbinden mit einer Instanz von der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Datenbankmodul über [!INCLUDE[ssSDSfull](../content/includes/ssSDSfull_md.md)], verwenden Sie [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Authentifizierung, und geben Sie eine Datenbank in der **mit Server verbinden** Dialogfelds die **Verbindungseigenschaften** Registerkarte. Wählen Sie aus der **Verbindung verschlüsseln** Kontrollkästchen.  
  
In der Standardeinstellung [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] wird eine Verbindung mit **master**. Wenn Sie eine Benutzerdatenbank angeben, wird im Objekt-Explorer nur diese Datenbank mit den zugehörigen Objekten angezeigt. Wenn Sie mit verbinden **master**, werden alle Datenbanken angezeigt. Weitere Informationen finden Sie unter der [Übersicht für Windows Azure SQL-Datenbank](http://go.microsoft.com/fwlink/?LinkId=163948).  
  
**Netzwerkprotokoll**  
Wählen Sie ein Protokoll aus der Liste aus. Die verfügbaren Clientprotokolle sind diejenigen, die Sie mithilfe der Netzwerkkonfiguration des Clients in der Computerverwaltung konfiguriert haben.  
  
**Netzwerkpaketgröße**  
Geben Sie die Größe der zu sendenden Netzwerkpakete ein. Der Standardwert ist 4096 Bytes.  
  
**Verbindungstimeout**  
Geben Sie an, wie lange (in Sekunden) versucht werden soll, eine Verbindung herzustellen, bevor ein Timeout eintritt. Der Standardwert ist 15 Sekunden.  
  
**Ausführungstimeout**  
Geben Sie an, wie lange (in Sekunden) auf den Abschluss eines Tasks auf dem Server gewartet werden soll. Der Standardwert ist 0 (null) Sekunden, womit keine Zeit\-heraus.  
  
**Verbindung verschlüsseln**  
Erzwingt die Verschlüsselung der Verbindung.  
  
**Benutzerdefinierte Farbe verwenden**  
Wählen Sie diese Option aus, um die Hintergrundfarbe für die Statusleiste in einem [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]-Abfrage-Editor-Fenster anzugeben. Um die Farbe anzugeben, klicken Sie auf **wählen**. In der **Farbe** Dialogfeld Wählen Sie eine vordefinierte Farbe aus der **Grundfarben** Raster oder klicken Sie auf **Farben definieren** definieren und eine benutzerdefinierte Farbe verwenden.  
  
-   Wenn Sie eine Farbe für einen Servereintrag im Angeben der **Objekt-Explorer** Bereich ist, wird diese Farbe verwendet, wenn Sie ein Abfrage-Editor-Fenster zu öffnen. Öffnen Sie eine Abfrage-Editorfenster, entweder direkt\-Klicken Sie auf den Servereintrag, und wählen Sie **neue Abfrage**; oder, wenn die **Objekt-Explorer** Bereich aktiv und auf diesen Server fokussiert ist, klicken Sie auf **neue Abfrage** auf der Symbolleiste.  
  
-   Wenn Sie eine Farbe für einen Servereintrag im Angeben der **registrierte Server** Bereich ist, wird diese Farbe verwendet, wenn Sie ein Abfrage-Editor-Fenster zu öffnen. Öffnen Sie eine Abfrage-Editorfenster, entweder direkt\-Klicken Sie auf den Servereintrag, und wählen Sie **neue Abfrage**; oder, wenn die **registrierte Server** Bereich aktiv und auf diesen Server fokussiert ist, klicken Sie auf **neue Abfrage** auf der Symbolleiste.  
  
-   Auf der **Datei** Menü, wenn Sie auf **Neu** und anschließend **Datenbankmodul-Abfrage**, die Farbe, mit der Angabe in der **mit Server verbinden** Dialogfeld gilt für diese Abfrage-Editor-Fenster.  
  
**Alles zurücksetzen**  
Ersetzt alle manuell eingegebenen Verbindungseigenschaftswerte durch die Standardwerte.  
  
**Connect**  
Versucht, mithilfe der aufgelisteten Werte eine Verbindung herzustellen.  
  
**Optionen**  
Klicken Sie hier, um die Anzeige des Dialogfelds zu ändern und die zusätzlichen Serververbindungsoptionen, z. B. Speichern des Kennworts, auszublenden.  
  
**Test**  
Bei der Registrierung [!INCLUDE[ssDE](../content/includes/ssDE_md.md)] in **registrierte Server**, klicken Sie hier, um die Verbindung zu testen.  
  
**Speichern**  
Speichert die Einstellungen in **registrierte Server**.  
  
## Siehe auch  
[Verbindungseigenschaften (Dialogfeld)](../content/Connection-Properties-Dialog-Box.md)  
  
