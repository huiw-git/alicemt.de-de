---
title: "Aufheben der Unterdr&#252;ckung von Warnungen f&#252;r das Ausf&#252;hren von benutzerdefinierten Berichten"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0deed900-c910-4d12-aac0-6ab9e39eb068
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
# Aufheben der Unterdr&#252;ckung von Warnungen f&#252;r das Ausf&#252;hren von benutzerdefinierten Berichten
Für benutzerdefinierte Berichte gibt es zwei Warndialogfelder. In diesem Thema wird beschrieben, wie die Unterdrückung der Anzeige dieser Felder in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] mit [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] aufgehoben werden kann.  
  
In der Standardeinstellung die **benutzerdefinierten Bericht ausführen** das Dialogfeld wird angezeigt, bevor Sie ein benutzerdefinierter Bericht ausgeführt wird. Bei Auswahl der **Sie diese Warnung nicht mehr anzeigen** Kontrollkästchen, das Dialogfeld wird nicht mehr angezeigt. Ebenfalls standardmäßig die **benutzerdefinierten Bericht ausführen** das Dialogfeld wird angezeigt, wenn Sie einen benutzerdefinierten Bericht öffnen, und klicken Sie dann auf einen Link, um einen anderen benutzerdefinierten Bericht öffnen. Dieses Dialogfeld zeigt den Pfad ausfüllen der verbundene\-durch benutzerdefinierte Berichtsdatei. Bei Auswahl der **Sie diese Warnung nicht mehr anzeigen** Kontrollkästchen, das Dialogfeld wird nicht mehr angezeigt.  
  
## <a name="SSMSProcedure"></a>Verwendung von SQL Server Management Studio  
  
#### So heben Sie die Unterdrückung des Warndialogfelds für den benutzerdefinierten Hauptbericht auf  
  
1.  Herstellen einer Verbindung mit <*Server*>\\<*Freigabe*>|<*Laufwerk*>\\Documents and Settings\\<UserProfile>\\Anwendungsdaten\\Microsoft\\Microsoft SQL Server\\130\\Tools\\Shell\\zunächst.  
  
2.  Rechts\-Klicken Sie auf **reports.xml**, und klicken Sie dann auf **Bearbeiten**.  
  
3.  Änderung**<SuppressWarning>true <\/SuppressWarning > zu <SuppressWarning>false <\/SuppressWarning >**.  
  
4.  Starten Sie [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] neu.  
  
#### Zum Unterdrücken der verbundene\-über benutzerdefinierten Bericht Warnung (Dialogfeld)  
  
1.  Herstellen einer Verbindung mit <*Server*>\\<*Freigabe*>|<*Laufwerk*>\\Documents and Settings\\<UserProfile>\\Anwendungsdaten\\Microsoft\\Microsoft SQL Server\\130\\Tools\\Shell\\zunächst.  
  
2.  Rechts\-Klicken Sie auf **reports.xml**, und klicken Sie auf **Bearbeiten**.  
  
3.  Änderung **<SuppressDrillthroughWarning>true <\/SuppressDrillthroughWarning > zu <SuppressDrillthroughWarning>false <\/SuppressDrillthroughWarning >**.  
  
4.  Starten Sie [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] neu.  
  
## Siehe auch  
[Benutzerdefinierte Berichte in Management Studio](../content/Custom-Reports-in-Management-Studio.md)  
[Hinzufügen eines benutzerdefinierten Berichts zu Management Studio](../content/Add-a-Custom-Report-to-Management-Studio.md)  
[Verwenden benutzerdefinierter Berichte mit Eigenschaften von Objekt-Explorer-Knoten](../content/Use-Custom-Reports-with-Object-Explorer-Node-Properties.md)  
  
