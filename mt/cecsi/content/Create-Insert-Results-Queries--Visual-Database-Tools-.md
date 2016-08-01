---
title: "Erstellen von Abfragen zum Einf&#252;gen von Ergebnissen (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8770d630-09cc-47ec-a0e9-e9de2d7bbc89
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
# Erstellen von Abfragen zum Einf&#252;gen von Ergebnissen (Visual Database Tools)
Mit einer Abfrage zum Einfügen von Ergebnissen können Sie Zeilen aus einer Tabelle in eine andere oder innerhalb einer Tabelle kopieren. Aus der Tabelle `titles` können Sie beispielsweise mit einer Abfrage zum Einfügen von Ergebnissen Informationen über alle Titel eines Herausgebers in eine zweite Tabelle kopieren, die dem betreffenden Herausgeber zur Verfügung gestellt werden kann. Das Erstellen einer Abfrage zum Einfügen von Ergebnissen ähnelt dem Erstellen von Abfragen zum Erstellen von Tabellen. Im Unterschied dazu werden jedoch Zeilen in eine vorhandene Tabelle kopiert.  
  
> [!TIP]  
> Sie können Zeilen auch durch Ausschneiden und Einfügen von einer Tabelle in eine andere kopieren. Erstellen Sie eine Abfrage für jede Tabelle, und führen Sie die Abfragen aus. Kopieren Sie die gewünschten Zeilen von einem Ergebnisdatenblatt in ein anderes.  
  
Beim Erstellen einer Abfrage zum Einfügen von Ergebnissen müssen folgende Angaben gemacht werden:  
  
-   Die Datenbanktabelle, in die Zeilen kopiert werden sollen (die Zieltabelle)  
  
-   Die Tabelle oder Tabellen, aus der Zeilen kopiert werden sollen (die Quelltabelle) Die Quelltabelle oder -tabellen werden Teil einer Unterabfrage. Wenn Sie innerhalb einer Tabelle kopieren, ist die Quelltabelle auch die Zieltabelle.  
  
-   Die Spalten der Quelltabelle, deren Inhalt Sie kopieren möchten  
  
-   Die Spalten der Zieltabelle, in die die Daten kopiert werden sollen  
  
-   Suchbedingungen zum Definieren der zu kopierenden Zeilen  
  
-   Die Sortierreihenfolge, wenn die Zeilen in einer besonderen Reihenfolge kopiert werden sollen  
  
-   Gruppierungsoptionen, wenn Sie nur Kurzinformationen kopieren möchten.  
  
Beispielsweise kopiert die folgende Abfrage Titelinformationen aus der Tabelle `titles` in eine Archivtabelle mit dem Namen `archivetitles`. Die Abfrage kopiert den Inhalt von vier Spalten für alle Titel eines bestimmten Herausgebers:  
  
```  
INSERT INTO archivetitles   
   (title_id, title, type, pub_id)  
SELECT title_id, title, type, pub_id  
FROM titles  
WHERE (pub_id = '0766')  
```  
  
> [!NOTE]  
> Verwenden Sie eine Abfrage zum Einfügen von Werten, um Werte in eine neue Zeile einzufügen.  
  
Sie können den Inhalt ausgewählter Spalten oder aller Spalten einer Zeile kopieren. In beiden Fällen müssen die kopierten Daten mit den Spalten der Zeilen kompatibel sein, in die sie eingefügt werden. Wenn Sie z. B. den Inhalt einer Spalte wie `price` kopieren, müssen von der Spalte in der Zeile, in die kopiert wird, numerische Daten mit Dezimalstellen angenommen werden. Beim Kopieren einer vollständigen Zeile müssen in der Zieltabelle kompatible Spalten in derselben physischen Position wie in der Quelltabelle vorhanden sein.  
  
Wenn Sie eine Abfrage zum Einfügen von Ergebnissen erstellen, ändert sich der Kriterienbereich und zeigt die für das Kopieren von Daten verfügbaren Optionen an. Eine Spalte Anfügen wird hinzugefügt, in der Sie die Spalten angeben können, in die Daten kopiert werden sollen.  
  
> [!CAUTION]  
> Eine ausgeführte Abfrage zum Einfügen von Ergebnissen kann nicht rückgängig gemacht werden. Erstellen Sie vorsichtshalber vor Ausführung der Abfrage eine Sicherungskopie der Daten.  
  
### So erstellen Sie eine Abfrage zum Einfügen von Ergebnissen  
  
1.  Erstellen Sie eine neue Abfrage, und fügen Sie die Tabelle hinzu, aus der Zeilen kopiert werden sollen (die Quelltabelle). Wenn Sie Zeilen innerhalb einer Tabelle kopieren, können Sie die Quelltabelle als Zieltabelle hinzufügen.  
  
2.  Zeigen Sie im Menü **Abfrage-Designer** auf **Typ ändern**, und klicken Sie dann auf **Ergebnisse einfügen**.  
  
3.  In der [Zieltabelle für legen Sie im Dialogfeld](../content/Choose-Target-Table-for-Insert-Results-Dialog-Box--Visual-Database-Tools-.md), wählen Sie die Tabelle, die Zeilen kopiert werden sollen (die Zieltabelle).  
  
    > [!NOTE]  
    > Der Abfrage- und Sicht-Designer kann nicht im Voraus bestimmen, welche Tabellen und Sichten aktualisiert werden können. Aus diesem Grund die **Tabellenname** Liste der **-Tabelle für Anfügeabfrage auswählen** Dialogfeld zeigt alle verfügbaren Tabellen und Sichten in der Datenverbindung abgefragt werden, auch wenn Sie, dass möglicherweise keine Zeilen kopiert werden können.  
  
4.  In dem Rechteck darstellt, der Tabelle oder\-bewertet Objekt, das die Namen der Spalten, deren Inhalt Sie kopieren möchten. Um vollständige Zeilen zu kopieren, wählen Sie **\&#42; (Alle Spalten)**.  
  
    Der Abfrage- und Ansicht-Designer fügt die ausgewählten Spalten an die **Spalte** der Criteriapane Spalte.  
  
5.  In der **Append** Spalte im Kriterienbereich wählen eine Zielspalte in der Zieltabelle für jede Spalte, die Sie kopieren. Wählen Sie *Tablename.\&#42;* Wenn Sie vollständige Zeilen kopieren. Die Spalten der Zieltabelle und der Quelltabelle müssen dieselben (oder kompatible) Datentypen aufweisen.  
  
6.  Geben Sie eine Sortierreihenfolge an, falls Sie die Zeilen in einer bestimmten Reihenfolge kopieren möchten. Weitere Informationen finden Sie unter [& #40; sortieren und Gruppieren von Abfrageergebnissen Visual Database Tools & #41;](../content/Sort-and-Group-Query-Results--Visual-Database-Tools-.md).  
  
7.  Geben Sie die zu kopierenden Zeilen durch Eingabe von suchbedingungen in der **Filter** Spalte. Weitere Informationen finden Sie unter [Suchkriterien angeben & #40; Visual Database Tools & #41;](../content/Specify-Search-Criteria--Visual-Database-Tools-.md).  
  
    Wenn Sie keine Suchbedingung festlegen, werden alle Zeilen der Quelltabelle in die Zieltabelle kopiert.  
  
    > [!NOTE]  
    > Wenn Sie dem Kriterienbereich eine zu durchsuchende Spalte hinzufügen, wird diese vom Abfrage- und Sicht-Designer ebenfalls in die Liste der zu kopierenden Spalten aufgenommen. Wenn Sie eine Spalte für eine Suche verwenden, aber nicht kopieren möchten, deaktivieren Sie das Kontrollkästchen neben dem Spaltennamen in dem Rechteck darstellt, der Tabelle oder\-bewertet Objekt.  
  
8.  Geben Sie Gruppierungsoptionen an, wenn Sie Kurzinformationen kopieren möchten. Weitere Informationen finden Sie unter [Zusammenfassen von Abfrageergebnissen & #40; Visual Database Tools & #41;](../content/Summarize-Query-Results--Visual-Database-Tools-.md).  
  
Beim Ausführen einer Abfrage zum Einfügen von Ergebnissen werden keine Ergebnisse der [im Ergebnisbereich](../content/Results-Pane--Visual-Database-Tools-.md). Stattdessen wird eine Meldung mit der Anzahl der kopierten Zeilen ausgegeben.  
  
## Siehe auch  
[Typen von Abfragen & #40. Visual Database Tools & #41;](../content/Types-of-Queries--Visual-Database-Tools-.md)  
[Entwerfen von Abfragen und Sichten Gewusst-wie-Themen & #40; Visual Database Tools & #41;](../content/Design-Queries-and-Views-How-to-Topics--Visual-Database-Tools-.md)  
  
