---
title: "Hinzuf&#252;gen von Tabellen zu Abfragen (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6551aa7e-31a1-4636-852a-819bc53d658b
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
# Hinzuf&#252;gen von Tabellen zu Abfragen (Visual Database Tools)
Wenn Sie eine Abfrage erstellen, rufen Sie Daten aus einer Tabelle oder anderen Objekten mit Tabellenstruktur wie Tabellen, Sichten und bestimmten Benutzer\-benutzerdefinierte Funktionen. Mit dieser Objekte in der Abfrage arbeiten möchten, fügen Sie die Objekte der **Diagrammbereich**.  
  
### Hinzufügen einer Tabelle oder Tabellen\-bewertet Objekt zu einer Abfrage  
  
1.  In der **Diagrammbereich** des Abfrage- und Sicht-Designer, mit der rechten Maustaste\-Klicken Sie auf den Hintergrund, und wählen Sie **Tabelle hinzufügen** aus dem Kontextmenü.  
  
2.  In der **Tabelle hinzufügen** Dialogfeld Wählen Sie die Registerkarte für den Typ des Objekts, die Sie der Abfrage hinzufügen möchten.  
  
3.  Doppelklicken Sie in der Liste der Elemente\-Klicken Sie auf jedes Element, das Sie hinzufügen möchten.  
  
4.  Wenn Sie das Hinzufügen abgeschlossen haben, klicken Sie auf **Schließen**.  
  
    Die Abfrage- und Sicht-Designer-Updates der **Diagrammbereich**, **im Kriterienbereich**, und **SQL-Bereich** entsprechend.  
  
Tabellen und Sichten werden der Abfrage automatisch hinzugefügt, wenn Sie in der Anweisung im SQL-Bereich einen entsprechenden Verweis einfügen.  
  
Der Abfrage- und Ansicht-Designer zeigt keine Datenspalten für eine Tabelle oder eine Tabelle\-strukturiertes Objekt, wenn Sie keinen erforderlichen Zugriffsrechte verfügen oder wenn der Anbieter Informationen zurückgeben kann. In diesem Fall nur eine Titelleiste und das \* (alle Spalten)-Kontrollkästchen für die Tabelle oder die Tabelle angezeigt werden\-bewertet Objekt.  
  
### So fügen Sie einer neuen Abfrage eine vorhandene Abfrage hinzu  
  
1.  Stellen Sie sicher, dass die **SQL-Bereich** wird angezeigt, in der neuen Abfrage, die Sie erstellen.  
  
2.  In der **SQL-Bereich**, geben Sie eine öffnende und schließende Klammer () nach dem Wort aus.  
  
3.  Öffnen Sie für die vorhandene Abfrage den Abfrage-Designer. (Es sind nun zwei Instanzen des Abfrage-Designers geöffnet.)  
  
4.  Anzeigen der **SQL-Bereich** für die innere, d. h. die vorhandene Abfrage Sie einschließen, in die neue, äußere Abfrage.  
  
5.  Markieren Sie den Text in der **SQL-Bereich**, und kopieren Sie ihn in die Zwischenablage.  
  
6.  Klicken Sie in der **SQL-Bereich** der neuen Abfrage, positionieren Sie den Cursor zwischen den eingefügten Klammern, und fügen Sie den Inhalt der Zwischenablage.  
  
7.  Bleiben Sie in der **SQL-Bereich**, fügen Sie einen Alias nach der schließenden Klammer.  
  
## Siehe auch  
[Erstellen von Tabellenaliasen & #40. Visual Database Tools & #41;](../content/Create-Table-Aliases--Visual-Database-Tools-.md)  
[Entfernen von Tabellen aus Abfragen & #40; Visual Database Tools & #41;](../content/Remove-Tables-from-Queries--Visual-Database-Tools-.md)  
[Geben Sie Suchkriterien & #40. Visual Database Tools & #41;](../content/Specify-Search-Criteria--Visual-Database-Tools-.md)  
[Zusammenfassen von Abfrageergebnissen & #40; Visual Database Tools & #41;](../content/Summarize-Query-Results--Visual-Database-Tools-.md)  
[Durchführen Sie grundlegende Operationen mit Abfragen & #40; Visual Database Tools & #41;](../content/Perform-Basic-Operations-with-Queries--Visual-Database-Tools-.md)  
  
