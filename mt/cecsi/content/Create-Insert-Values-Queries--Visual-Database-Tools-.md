---
title: "Erstellen von Abfragen zum Einf&#252;gen von Werten (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2d4b2f6d-cc09-434b-8a0e-ccce40628064
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
# Erstellen von Abfragen zum Einf&#252;gen von Werten (Visual Database Tools)
Mit einer Abfrage zum Einfügen von Werten können Sie in der aktuellen Tabelle eine neue Zeile erstellen. Beim Erstellen einer Abfrage zum Einfügen von Werten müssen folgende Angaben gemacht werden:  
  
-   Die Datenbanktabelle, der die Zeile hinzugefügt werden soll  
  
-   Die Spalten, deren Inhalt Sie hinzufügen möchten  
  
-   Der in die einzelnen Spalten einzufügende Wert oder Ausdruck  
  
Die folgende Abfrage fügt beispielsweise eine Zeile in die Tabelle `titles` ein, die Werte für den Titel, den Typ, den Herausgeber und den Preis angibt:  
  
```  
INSERT INTO titles  
         (title_id, title, type, pub_id, price)  
VALUES   ('BU9876', 'Creating Web Pages', 'business', '1389', '29.99')  
```  
  
Beim Erstellen einer Abfrage zum Einfügen von Werten ändert sich der Kriterienbereich entsprechend und zeigt die beiden Optionen an, die zum Einfügen einer neuen Zeile verfügbar sind: den Spaltennamen und den einzufügenden Wert.  
  
> [!CAUTION]  
> Eine ausgeführte Abfrage zum Einfügen von Werten kann nicht mehr rückgängig gemacht werden. Erstellen Sie vorsichtshalber vor Ausführung der Abfrage eine Sicherungskopie der Daten.  
  
### So erstellen Sie eine Abfrage zum Einfügen von Werten  
  
1.  Fügen Sie dem Diagrammbereich die zu aktualisierende Tabelle hinzu.  
  
2.  Aus der **-Abfrage-Designer** zeigen Sie im Menü auf **Änderungstyp**, und klicken Sie dann auf **Einfügen von Werten**.  
  
    > [!NOTE]  
    > Wenn mehr als eine Tabelle im Diagrammbereich angezeigt wird, wenn beim Starten der Werte einfügen-Abfrage die Abfrage und Sicht-Designer zeigt die [Zieltabelle für Dialogfeld](../content/Choose-Target-Table-for-Insert-Values-Dialog-Box--Visual-Database-Tools-.md) für den Namen der zu aktualisierenden Tabelle aufgefordert.  
  
3.  Aktivieren Sie im Diagrammbereich das Kontrollkästchen für die Spalten, für die Sie neue Werte eingeben wollen. Diese Spalten werden im Kriterienbereich angezeigt. Spalten werden nur aktualisiert, wenn sie der Abfrage hinzugefügt werden.  
  
4.  In der **neuen Wert** Spalte im Kriterienbereich geben den neuen Wert für die Spalte. Sie können Literalwerte, Spaltennamen oder Ausdrücke eingeben. Der Wert muss dem Datentyp der zu aktualisierenden Spalte entsprechen (oder mit diesem kompatibel sein).  
  
    > [!CAUTION]  
    > Der Abfrage- und Sicht-Designer kann nicht überprüfen, ob die Länge eines Werts die zulässige Länge der Spalte überschreitet. Bei Eingabe eines zu langen Werts kann dieser ohne vorherige Warnung verkürzt werden. Wenn beispielsweise die Spalte `name` eine Länge von 20 Zeichen aufweist, Sie aber einen aus 25 Zeichen bestehenden einzufügenden Wert angeben, werden die letzten 5 Zeichen möglicherweise abgeschnitten.  
  
Beim Ausführen einer Abfrage zum Einfügen von Werten werden keine Ergebnisse der [im Ergebnisbereich](../content/Results-Pane--Visual-Database-Tools-.md). Stattdessen wird eine Meldung mit der Anzahl der geänderten Zeilen ausgegeben.  
  
## Siehe auch  
[Unterstützte Abfragetypen & #40; Visual Database Tools & #41;](../content/Supported-Query-Types--Visual-Database-Tools-.md)  
[Entwerfen von Abfragen und Sichten Gewusst-wie-Themen & #40; Visual Database Tools & #41;](../content/Design-Queries-and-Views-How-to-Topics--Visual-Database-Tools-.md)  
[Durchführen Sie grundlegende Operationen mit Abfragen & #40; Visual Database Tools & #41;](../content/Perform-Basic-Operations-with-Queries--Visual-Database-Tools-.md)  
  
