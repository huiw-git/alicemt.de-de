---
title: "Optionen (Umgebung - Schriftarten und Farben Seite)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ea3aa222-538d-485f-99dc-01eb02cdcfea
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
# Optionen (Umgebung - Schriftarten und Farben Seite)
Die **Optionen** Dialogfeld können Sie eine benutzerdefinierte Schriftarten und Farbschemas für verschiedene Elemente der Benutzeroberfläche in herstellen [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)]. Auf der **Tools** Menü klicken Sie auf **Optionen** Erweitern Sie den **Umgebung** Ordner, und wählen Sie **Schriftarten und Farben**.  
  
Änderungen am Farbschema werden nicht in der Sitzung wirksam, in der Sie sie vornehmen. Sie können Farbänderungen auswerten, indem Sie eine andere Instanz von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] öffnen und die Bedingungen erstellen, unter denen Sie die Anwendung Ihrer Änderungen erwarten.  
  
## Liste der Benutzeroberflächenelemente  
**Einstellungen anzeigen für**  
Führt alle Elemente der Benutzeroberfläche auf, für die Sie das Schriftart- und Farbschema ändern können. Nach dem Auswählen eines Elements aus dieser Liste können Sie farbeinstellungen für das ausgewählte Element im anpassen **Elemente anzeigen**.  
  
|Begriff|Definition|  
|--------|--------------|  
|Text-Editor|Änderungen an den Anzeigeeinstellungen für Schriftart, Größe und Farbe für den Text-Editor wirken sich auf die Darstellung von Text in Ihrem Standard-Text-Editor aus. In einem Text-Editor außerhalb von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] geöffnete Dokumente sind von diesen Einstellungen nicht betroffen.|  
|Drucker|Änderungen an den Anzeigeeinstellungen für Schriftart, Größe und Farbe für den Drucker wirken sich auf die Darstellung von Text in gedruckten Dokumenten aus.<br /><br />Hinweis: Sie können eine andere Standardschriftart für den Druck, die für die Anzeige im Text-Editor auswählen. Dies kann hilfreich sein, beim Drucken von Code, der sowohl einzelne enthält\-Byte und Double\-Byte-Zeichen.|  
|\[Alle Texttoolfenster **]**|Änderungen an den Anzeigeeinstellungen für Schriftart, Größe und Farbe für dieses Element wirken sich auf die Darstellung von Text in Toolfenstern aus, die in [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] über Ausgabebereiche verfügen. Z. B. Ausgabefenster, TextResults Fenster und So weiter.<br /><br />Hinweis: Änderungen an den Text der \[Alle Texttoolfenster] Elemente werden nicht wirksam, während der Sitzung, in dem Sie Sie vornehmen. Solche Änderungen können Sie auswerten, indem Sie eine andere Instanz von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] öffnen.|  
|Fenster Suchergebnisse|Änderungen an den Schriftschnitt, Größe und Farbe der Anzeigeoptionen für dieses Element wirken sich der Text im Fenster FindResults.|  
|Ausgabefenster|Änderungen an den Anzeigeeinstellungen für Schriftart, Größe und Farbe für dieses Element wirken sich auf die Darstellung von Text im Ausgabefenster aus.|  
|Rasterergebnisse|Änderungen an den Schriftschnitt, Größe und Farbe der Anzeigeoptionen für dieses Element wirken sich der Text in der **Rasterergebnisse** im Abfrage-Fenster.|  
|Ausführungsplan|Änderungen an den Schriftschnitt, Größe und Farbe der Anzeigeoptionen für dieses Element wirken sich der Text im Ausführungsplan von [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] und [!INCLUDE[ssEW](../content/includes/ssEW_md.md)] Abfragen.|  
|Textergebnis|Änderungen an den Schriftschnitt, Größe und Farbe der Anzeigeoptionen für dieses Element wirken sich der Text in der **Textergebnisse** Bereich des Fensters Abfrage.|  
|Business Intelligence-Designer|Änderungen an den Schriftschnitt, Größe und Farbe der Anzeigeoptionen für dieses Element wirken sich der Text in der BusinessIntelligenceDesignerswindow.|  
  
**Standard verwenden**  
Die **Standard verwenden** Schaltfläche setzt den Wert für die Schriftart und Farbe Werte in der Liste Element, das Sie ausgewählt, die von der **Einstellungen anzeigen für** Liste.  
  
**Schriftart (Fett bedeutet mit fester\-Breite formatiert)**  
Führt alle Schriftarten auf, die auf Ihrem System installiert sind. Wenn diese Dropdownliste\--Liste zuerst geöffnet wird, die aktuelle Schriftart für das Element, das Sie ausgewählt haben, aus der **Einstellungen anzeigen für** Liste ausgewählt ist. Feste Schriftarten – die im Editor einfacher auszurichten sind - werden in Fettschrift angezeigt.  
  
**Schriftgrad**  
Führt die verfügbaren Schriftgrade für die ausgewählte Schriftart auf. Ändern der Größe der Schriftart wirkt sich auf alle **Elemente anzeigen** Einträge für eine **Einstellungen anzeigen für** Auswahl.  
  
**Elemente anzeigen**  
Führt die Elemente auf, für die Sie die Vordergrund- und Hintergrundfarbe ändern können.  
  
> [!NOTE]  
> **T**standardanzeigeelement ist Text. Anzeigeelementen des Typs Text zugewiesene Eigenschaften werden von Eigenschaften, die anderen Anzeigeelementen zugewiesen wurden, überschrieben. Beispielsweise, wenn Sie die Farbe Blau zuweisen **Text** und die Farbe Grün, alle Bezeichner in grün angezeigt. In diesem Beispiel überschreiben die Eigenschaften für Bezeichner die Eigenschaften für Text.  
  
Zu den Anzeigeelementen gehören unter anderem:  
  
-   Indikatorrand: Der Rand auf der linken Seite des Code-Editors, auf dem Breakpoints und Lesezeichensymbole angezeigt werden.  
  
-   Reduzierbarer Text: Ein Block mit Text oder Code, der in und aus dem CodeEditor (nur XML)-Ansicht gewechselt werden kann.  
  
**Elementvordergrund**  
Listet die verfügbaren Farben auf, die für das ausgewählte Element im Vordergrund **Elemente anzeigen**. Weil einige Elemente in Beziehung zueinander stehen, sollte ein einheitliches Anzeigeschema beibehalten werden. Beispielsweise wird bei Änderung der Vordergrundfarbe von Text auch die Vordergrundfarbe für Elemente des Typs Zeichenfolge geändert.  
  
**Benutzerdefiniert**  
Zeigt die **Farbe** Dialogfeld, in dem Sie eine benutzerdefinierte Farbe für das ausgewählte Element im Festlegen der **Elemente anzeigen** Liste.  
  
> [!NOTE]  
> Ihre Möglichkeiten, benutzerdefinierte Farben zu definieren, werden möglicherweise durch die Farbeinstellungen für Ihr Computerdisplay eingeschränkt. Beispielsweise, wenn Ihr Computer 256 Farben festgelegt ist und Sie eine benutzerdefinierte Farbe auswählen die **Farbe** Klicken Sie im Dialogfeld [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] entscheidet sich für den nächsten verfügbaren Wert in **Grundfarben** als Standard, und zeigt die Farbe Schwarz in der **Farbe** (Dialogfeld).  
  
**Elementhintergrund**  
Bietet eine Farbpalette aus dem können Sie eine Hintergrundfarbe für das ausgewählte Element im **Elemente anzeigen**. Weil einige Elemente in Beziehung zueinander stehen, sollte ein einheitliches Anzeigeschema beibehalten werden. Beispielsweise wird bei Änderung der Hintergrundfarbe von Text auch die Hintergrundfarbe für Elemente des Typs SQL-Zeichenfolge geändert.  
  
**Benutzerdefiniert**  
Zeigt die **Farbe** Dialogfeld, in dem Sie eine benutzerdefinierte Farbe für das ausgewählte Element im Festlegen der **Elemente anzeigen** Liste.  
  
**Fett**  
Wählen Sie dieses Kontrollkästchen, um den Text des ausgewählten Displayitems in Fettschrift angezeigt. Text in Fettschrift ist in einem Editor einfacher zu identifizieren.  
  
**Beispiel**  
Zeigt ein Beispiel für die Schriftart, Größe und Farbschema für die ausgewählten Werte in **Einstellungen anzeigen für** und **Elemente anzeigen**. In diesem Textfeld können Sie beim Ausprobieren der verschiedenen Formatierungsoptionen eine Vorschau der Ergebnisse anzeigen.  
  
## Siehe auch  
[Farbcodierung in Code-Editoren](assetId:///802882dc-c997-4e3f-8a01-994bb43169ae)  
[Optionen (Texteditor/Registerkarte 'Editor' und Statusleiste)](assetId:///e4815678-7885-4631-878f-c6a2b857ee05)  
  
