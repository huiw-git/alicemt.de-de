---
title: "Detailbereich des Objekt-Explorers"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b963e3c2-dc9e-4d38-bd28-2e00fe9e0e47
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
# Detailbereich des Objekt-Explorers
Details zum Objekt-Explorer, eine Komponente von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)], stellt eine tabellarische Ansicht aller Objekte im Server sowie eine Benutzeroberfläche zu deren Verwaltung bereit. Die Funktionen des Objekt-Explorers variiert abhängig vom Typ des Servers, aber im Allgemeinen die Entwicklungsfunktionen für Datenbanken und die Verwaltungsfunktionen für alle Servertypen.  
  
Die Details zum Objekt-Explorer-Fenster wird nur angezeigt, in dem [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)] standardmäßig. Wenn Sie Objekt-Explorer sehen können die **Ansicht** Menü klicken Sie auf **Details zum Objekt-Explorer** oder drücken Sie **F7**.  
  
> [!NOTE]  
> [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)] präsentiert von Datumsangaben mit dem Microsoft Windows Regions- und Sprachoptionen in Kraft bei [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)] wurde gestartet. Starten Sie [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)] neu, um die neuen Einstellungen wiederzugeben.  
  
## Details zum Objekt-Explorer  
Details zum Objekt-Explorer kann verwendet werden, um durch Ordner und Objekte navigieren Sie auf Ihrem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Instanz. Auf 32\--bit-Betriebssystemen, Objekt-Explorer können nur 64.000 Objekte anzeigen. Um auf zusätzliche Objekte zuzugreifen, muss ein Symbol ausgewählt werden.  
  
Details zum Objekt-Explorer verfügt über eine Symbolleiste, die die in der folgenden Tabelle beschriebenen Symbole enthält. Die Symbole sind nur verfügbar, wenn die entsprechenden Aktionen anwendbar sind.  
  
|Symbol|Aktion|  
|--------|----------|  
|**Zurück**|Wechselt zu den vorherigen in Details zum Objekt-Explorer angezeigten Elementen. Re\-eine Suche ausgeführt wird, wenn die vorherige Anzeige das Ergebnis eines Suchvorgangs ist.|  
|**Vorwärts**|Wechselt zum nächsten Bildschirm, nachdem ein **wieder** ausgewählt ist.|  
|**Nach oben**|Wechselt zum übergeordneten Objekt oder Ordner.|  
|**Synchronisieren**|Legt den Fokus von Objekt-Explorer auf das in Details zum Objekt-Explorer ausgewählte Objekt fest.|  
|**Filter**|Zeigt, soweit verfügbar, eine konfigurierbare Teilmenge von Objekten an.|  
|**Aktualisieren**|Aktualisiert die Anzeige in Details zum Objekt-Explorer.|  
|**Suchen**|Stellt einen Bereich bereit, um einen Suchbegriff für bestimmte Datenbankobjekte einzugeben.|  
  
### Spaltenheaderauswahl  
Details zum Objekt-Explorer verfügt über auswählbare Spalten. Sie können mit der rechten\-Klicken Sie auf eine Spaltenüberschrift, und überprüfen Sie die Elemente, die Sie anzeigen möchten. Ihre Auswahl wird für alle Objekte, durch die Sie navigieren, beibehalten. Die Auswahl wird für jeden Benutzer individuell beibehalten, wenn [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] beendet und neu gestartet wird.  
  
> [!CAUTION]  
> Wenn bei einigen Objekttypen (wie z.&amp;#160;B. Datenbanken) alle Spalten angezeigt werden, kann das Rendering der Anzeige bei großen Objektsätzen geringfügig verlangsamt werden.  
  
### Sortieren  
Wenn Sie auf einen Spaltenheader einmal klicken, erfolgt eine Sortierung nach dieser Spalte. Klicken erneut auf den gleichen Header reverse\-nach dieser Spalte sortiert. Die Sortierauswahl wird für jeden Benutzer für alle Objekte und Ordner sowie für den Neustart von [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)] beibehalten.  
  
### Filterung  
Bestimmte Listen von Objekten angezeigt, die im Objekt-Explorer Detail können gefiltert werden, mithilfe der **Filter** Symbol auf der Symbolleiste Details zum Objekt-Explorer. Das Symbol wird aktiviert, wenn eine Filterung möglich ist.  
  
### Detailbereich  
Am unteren Rand von Details zum Objekt-Explorer befindet sich ein Bereich, in dem bestimmte Details des ausgewählten Objekts angezeigt werden. Bei einer Mehrfachauswahl von Objekten wird nur die Anzahl der Objekte angezeigt. Wenn Sie im Bereich Elemente ausgewählt sind, klicken Sie auf die **Kopieren** Symbol, um den angezeigten Text in die Zwischenablage zu kopieren.  
  
Mit der NACH-UNTEN-TASTE wird die Auswahl in das nächste Listenelement verschoben. Mit der NACH-OBEN-TASTE wird die Auswahl in das vorherige Listenelement verschoben. Wenn Sie die Pfeiltaste gedrückt halten, können Sie die Elemente schneller durchlaufen. Die Auswahl wird am Anfang oder Ende der Eigenschaftenliste angehalten.  
  
Wenn Sie das erste Zeichen eines Eigenschaftennamens eingeben, wird die Auswahl in die nächste Eigenschaft verschoben, die mit diesem Zeichen beginnt.  
  
Wenn Eigenschaften in mehreren Spalten angeordnet werden, bewegen Sie ein Element mithilfe der NACH-LINKS-TASTE und NACH-RECHTS-TASTE in angrenzende Spalten.  
  
Um Eigenschaftswerte in die Zwischenablage zu kopieren, verwenden Sie die folgenden Tastenkombinationen:  
  
-   STRG\+C kopiert den Wert der Eigenschaft.  
  
-   STRG\+UMSCHALT\+C kopiert den Eigenschaftennamen und den Wert der Eigenschaft mit einem Trennzeichen Registerkarte.  
  
Drücken Sie die Rechte\-Klicken Sie im Menü im Bereich Details zum Objekt-Explorer kopieren Sie alle Eigenschaften oder alle Eigenschaften und Namen in die Zwischenablage.  
  
Um einen Eigenschaftswert anzuzeigen, wenn er die Breite des Felds überragt, zeigen Sie mit dem Mauscursor auf den Wert oder legen den Benutzeroberflächenfokus auf den Eigenschaftswert fest, um eine QuickInfo mit dem gesamten Eigenschaftswert zu aktivieren. Barrierefreie Sprachausgaben melden den vollständigen Eigenschaftswert, wenn der Benutzer auf den langen Eigenschaftswert fokussiert.  
  
Wenn die Anzahl von Eigenschaften im Eigenschaftenbereich die Anzahl übersteigt, die in den Inhaltsbereich passt, wird auf der rechten Seite des Eigenschaftenbereichs eine Bildlaufleiste angezeigt. Passen Sie die Ansicht der Eigenschaftswerte im Inhaltsbereich mithilfe der Bildlaufleiste ein.  
  
### Mehrfachauswahl von Objekten  
Details zum Objekt-Explorer unterstützt die Mehrfachauswahl von Objekten. Beispielsweise, wenn Sie Tabellen im Objekt-Explorer aus, und klicken Sie dann im Fenster Details zum Objekt-Explorer auswählen, wenn Sie halten die **STRG** Key, Sie können mehrere Tabellen auswählen, nach rechts\-darauf klicken, und wählen Sie **Löschen** oder **Skript für Tabelle als** auf alle ausgewählten Tabellen sofort zu reagieren. Mit den standardmäßigen Befehlen zum Kopieren wird der angezeigte Text in die Zwischenablage kopiert.  
  
## SQL Server-Objektsuche  
Platzhalter  
  
-   Standardmäßige Platzhalterzeichen werden unterstützt. Z. B. Suchen nach **dm\_os % Counters** gibt sowohl dm\_os\_Speicher\_Cache\_Leistungsindikatoren und dm\_os\_Leistung\_Leistungsindikatoren. Weitere Informationen finden Sie unter [Gewusst wie: Suchen mit Platzhaltern](assetId:///449600f8-cc87-4b3f-878a-59c158a88a40).  
  
Suchbereich  
  
-   Jede Suche ist auf den aktuellen Fokus in der Strukturansicht des Objekt-Explorers begrenzt. Z. B. wenn der Fokus des Objekt-Explorer auf eine Datenbank ist, suchen Sie nach **dm\_os % Counters** dm gibt\_os\_Speicher\_Cache\_Leistungsindikatoren und dm\_os\_Leistung\_Leistungsindikatoren in dieser Datenbank. Befindet sich der Fokus des Objekt-Explorers auf dem Knoten Datenbanken, werden alle Datenbanken durchsucht und mehrere Instanzen der dynamischen Sichten zurückgegeben.  
  
Große Objektsätze  
  
-   Das Durchsuchen von großen Objektsätzen kann einige Zeit in Anspruch nehmen und die Serverleistung verringern.  
  
## Siehe auch  
[Objekt-Explorer](../content/Object-Explorer.md)  
  
