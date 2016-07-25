---
title: "Erstellen von Updateabfragen (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 178b7b75-8078-4e61-b2a8-4719b9d8033d
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
# Erstellen von Updateabfragen (Visual Database Tools)
Mit einer Aktualisierungsabfrage können Sie in einem Vorgang den Inhalt mehrerer Zeilen ändern. Sie können beispielsweise in der Tabelle `titles` eine Updateabfrage verwenden, um den Preis aller Bücher eines bestimmten Herausgebers um 10 % zu erhöhen.  
  
Beim Erstellen einer Updateabfrage müssen folgende Angaben gemacht werden:  
  
-   Die zu aktualisierende Tabelle  
  
-   Die Spalten, deren Inhalt Sie aktualisieren möchten  
  
-   Der Wert oder Ausdruck, der zum Aktualisieren der einzelnen Spalten verwendet werden soll  
  
-   Suchbedingungen zum Definieren der zu aktualisierenden Zeilen  
  
Die folgende Abfrage aktualisiert beispielsweise die Tabelle `titles`, indem der Preis sämtlicher Titel eines Herausgebers um 10 % erhöht wird:  
  
```  
UPDATE titles  
SET price = price * 1.1  
WHERE (pub_id = '0766')  
```  
  
> [!CAUTION]  
> Eine ausgeführte Updateabfrage kann nicht rückgängig gemacht werden. Erstellen Sie vorsichtshalber vor Ausführung der Abfrage eine Sicherungskopie der Daten.  
  
### So erstellen Sie eine Updateabfrage  
  
1.  Fügen Sie dem Diagrammbereich die zu aktualisierende Tabelle hinzu.  
  
2.  Aus der **-Abfrage-Designer** zeigen Sie im Menü auf **Änderungstyp**, und klicken Sie dann auf **Update**.  
  
    > [!NOTE]  
    > Wenn mehr als eine Tabelle im Diagrammbereich angezeigt wird, wenn beim Starten der Update-Abfrage, die Abfrage und Sicht-Designer zeigt die [Zieltabelle für Dialogfeld](../content/Choose-Target-Table-for-Insert-Values-Dialog-Box--Visual-Database-Tools-.md) für den Namen der zu aktualisierenden Tabelle aufgefordert.  
  
3.  Aktivieren Sie im Diagrammbereich das Kontrollkästchen für die Spalten, für die Sie neue Werte eingeben wollen. Diese Spalten werden im Kriterienbereich angezeigt. Spalten werden nur aktualisiert, wenn sie der Abfrage hinzugefügt werden.  
  
4.  In der **neuen Wert** Spalte im Kriterienbereich geben den Aktualisierungswert für die Spalte. Sie können Literalwerte, Spaltennamen oder Ausdrücke eingeben. Der Wert muss dem Datentyp der zu aktualisierenden Spalte entsprechen (oder mit diesem kompatibel sein).  
  
    > [!CAUTION]  
    > Der Abfrage- und Sicht-Designer kann nicht überprüfen, ob ein Wert von der Länge her in die zu aktualisierende Spalte passt. Bei Eingabe eines zu langen Werts kann dieser ohne vorherige Warnung verkürzt werden. Wenn beispielsweise die Spalte `name` eine Länge von 20 Zeichen aufweist, Sie aber einen aus 25 Zeichen bestehenden Updatewert angeben, werden die letzten 5 Zeichen möglicherweise abgeschnitten.  
  
5.  Definieren der zu aktualisierenden Zeilen durch Eingabe von suchbedingungen in der **Filter** Spalte. Weitere Informationen finden Sie unter [Suchkriterien angeben & #40; Visual Database Tools & #41;](../content/Specify-Search-Criteria--Visual-Database-Tools-.md).  
  
    Wenn Sie keine Suchbedingung angeben, werden alle Zeilen der angegebenen Tabelle aktualisiert.  
  
    > [!NOTE]  
    > Wenn Sie dem Kriterienbereich eine Spalte zum Verwenden in einer Suchbedingung hinzufügen, wird sie vom Abfrage- und Sicht-Designer auch der Liste der zu aktualisierenden Spalten hinzugefügt. Wenn Sie eine Spalte für eine Suchbedingung verwenden, aber nicht aktualisieren möchten, deaktivieren Sie das Kontrollkästchen neben dem Spaltennamen in dem Rechteck darstellt, der Tabelle oder\-bewertet Objekt.  
  
Beim Ausführen einer Aktualisierungsabfrage werden keine Ergebnisse der [im Ergebnisbereich](../content/Results-Pane--Visual-Database-Tools-.md). Stattdessen wird eine Meldung mit der Anzahl der geänderten Zeilen ausgegeben.  
  
## Siehe auch  
[Unterstützte Abfragetypen & #40; Visual Database Tools & #41;](../content/Supported-Query-Types--Visual-Database-Tools-.md)  
[Entwerfen von Abfragen und Sichten Gewusst-wie-Themen & #40; Visual Database Tools & #41;](../content/Design-Queries-and-Views-How-to-Topics--Visual-Database-Tools-.md)  
[Durchführen Sie grundlegende Operationen mit Abfragen & #40; Visual Database Tools & #41;](../content/Perform-Basic-Operations-with-Queries--Visual-Database-Tools-.md)  
  
