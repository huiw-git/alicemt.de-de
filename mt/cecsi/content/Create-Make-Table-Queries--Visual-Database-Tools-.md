---
title: "Erstellen von Tabellenerstellungsabfragen (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4493cffa-7b2d-4c24-8ef0-d49329198972
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
# Erstellen von Tabellenerstellungsabfragen (Visual Database Tools)
Mit einer Tabellenerstellungsabfrage können Sie Zeilen in eine neue Tabelle kopieren. Dies ist hilfreich, wenn Datenteilmengen als Arbeitsgrundlage erstellt oder der Inhalt einer Tabelle von einer Datenbank in eine andere kopiert werden soll. Eine Tabellenerstellungsabfrage ähnelt einer Abfrage zum Einfügen von Ergebnissen. Jedoch wird im Unterschied dazu eine neue Tabelle erstellt, in die Zeilen kopiert werden sollen.  
  
Beim Erstellen einer Tabellenerstellungsabfrage müssen folgende Angaben gemacht werden:  
  
-   Der Name der neuen Datenbanktabelle (der Zieltabelle)  
  
-   Die Tabelle oder Tabellen, aus der Zeilen kopiert werden sollen (die Quelltabelle) Das Kopieren ist aus einer einzelnen oder aus verknüpften Tabellen möglich.  
  
-   Die Spalten der Quelltabelle, deren Inhalt Sie kopieren möchten  
  
-   Die Sortierreihenfolge, wenn die Zeilen in einer besonderen Reihenfolge kopiert werden sollen  
  
-   Suchbedingungen zum Definieren der zu kopierenden Zeilen  
  
-   Gruppierungsoptionen, wenn Sie nur Kurzinformationen kopieren möchten.  
  
Die folgende Abfrage erstellt beispielsweise eine neue Tabelle namens `uk`\_`customers` und kopiert Informationen aus der `customers` Tabelle:  
  
```  
SELECT *   
INTO uk_customers  
FROM customers  
WHERE country = 'UK'  
```  
  
Folgende Bedingungen müssen erfüllt sein, damit eine Tabellenerstellungsabfrage erfolgreich verwendet werden kann:  
  
-   Die Datenbank muss die SELECT...INTO-Syntax unterstützen.  
  
-   Sie müssen über eine Berechtigung zum Erstellen von Tabellen in der Zieldatenbank verfügen.  
  
### So erstellen Sie eine Tabellenerstellungsabfrage  
  
1.  Fügen Sie dem Diagrammbereich die Quelltabellen hinzu.  
  
2.  Aus der **-Abfrage-Designer** auf **Änderungstyp**, und klicken Sie dann auf **Make Table**.  
  
3.  In der **Tabelle** Dialogfeld Geben Sie den Namen der Zieltabelle. Der Abfrage- und Sicht-Designer überprüft nicht, ob der Name bereits verwendet wird oder ob Sie über eine Berechtigung zum Erstellen der Tabelle verfügen.  
  
    Geben Sie zum Erstellen einer Zieltabelle in einer anderen Datenbank einen vollständigen Tabellennamen an, der den Namen der Zieldatenbank, den Besitzer (falls erforderlich) und den Namen der Tabelle enthält.  
  
4.  Legen Sie die zu kopierenden Spalten fest, indem Sie diese der Abfrage hinzufügen. Weitere Informationen finden Sie unter [Hinzufügen von Spalten zu Abfragen & #40; Visual Database Tools & #41;](../content/Add-Columns-to-Queries--Visual-Database-Tools-.md). Spalten werden nur kopiert, wenn sie der Abfrage hinzugefügt werden. Um vollständige Zeilen zu kopieren, wählen Sie **\&#42; (Alle Spalten)**.  
  
    Der Abfrage- und Ansicht-Designer fügt die ausgewählten Spalten an die **Spalte** Spalte im Kriterienbereich.  
  
5.  Geben Sie eine Sortierreihenfolge an, falls Sie die Zeilen in einer bestimmten Reihenfolge kopieren möchten. Weitere Informationen finden Sie unter **Sortieren und Gruppieren von Abfrageergebnissen**.  
  
6.  Geben Sie die zu kopierenden Zeilen durch Eingabe von Suchbedingungen an. Weitere Informationen finden Sie unter [Suchkriterien angeben & #40; Visual Database Tools & #41;](../content/Specify-Search-Criteria--Visual-Database-Tools-.md).  
  
    Wenn Sie keine Suchbedingung festlegen, werden alle Zeilen der Quelltabelle in die Zieltabelle kopiert.  
  
    > [!NOTE]  
    > Wenn Sie dem Kriterienbereich eine zu durchsuchende Spalte hinzufügen, wird diese vom Abfrage- und Sicht-Designer ebenfalls in die Liste der zu kopierenden Spalten aufgenommen. Wenn Sie eine Spalte für eine Suche verwenden, aber nicht kopieren möchten, deaktivieren Sie das Kontrollkästchen neben dem Spaltennamen in dem Rechteck darstellt, der Tabelle oder\-strukturiertes Objekt.  
  
7.  Geben Sie Gruppierungsoptionen an, wenn Sie Kurzinformationen kopieren möchten. Weitere Informationen finden Sie unter [Zusammenfassen von Abfrageergebnissen & #40; Visual Database Tools & #41;](../content/Summarize-Query-Results--Visual-Database-Tools-.md).  
  
Wenn Sie eine Make Table-Abfrage ausführen, werden keine Ergebnisse der [im Ergebnisbereich](../content/Results-Pane--Visual-Database-Tools-.md). Stattdessen wird eine Meldung mit der Anzahl der kopierten Zeilen ausgegeben.  
  
## Siehe auch  
[Entwerfen von Abfragen und Sichten Gewusst-wie-Themen & #40; Visual Database Tools & #41;](../content/Design-Queries-and-Views-How-to-Topics--Visual-Database-Tools-.md)  
[Typen von Abfragen & #40. Visual Database Tools & #41;](../content/Types-of-Queries--Visual-Database-Tools-.md)  
  
