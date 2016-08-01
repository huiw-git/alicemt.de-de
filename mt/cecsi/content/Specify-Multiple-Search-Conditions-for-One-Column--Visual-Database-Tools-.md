---
title: "Geben Sie mehrerer Suchbedingungen f&#252;r eine Spalte (Visual Database Tools an)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2c006e36-56b1-4992-89b4-c6c0b19808f3
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
# Geben Sie mehrerer Suchbedingungen f&#252;r eine Spalte (Visual Database Tools an)
In einigen Fällen empfiehlt es sich um eine Anzahl von Suchkriterien auf dieselbe Datenspalte anwenden. Angenommen, sollten Sie Folgendes beachten:  
  
-   Suchen Sie nach mehreren verschiedenen Namen in einer `employee` Tabelle oder für Mitarbeiter, die sich in verschiedenen Gehaltsgruppen. Diese Art von Suche erfordert eine OR-Bedingung.  
  
-   Suche nach einem Buchtitel Titel beginnt mit dem Wort "The" und enthält das Wort "Koch". Diese Art von Suche erfordert eine AND-Bedingung.  
  
> [!NOTE]  
> Die Informationen in diesem Thema gelten um Startbedingungen in WHERE- und HAVING-Klausel einer Abfrage zu suchen. Die Beispiele beziehen sich auf das Erstellen von WHERE-Klauseln, die Prinzipien gelten jedoch für beide Arten von Suchkriterien.  
  
Um nach verschiedenen Werten in derselben Spalte suchen, geben Sie eine OR-Bedingung. Um Werte zu suchen, die verschiedene Kriterien erfüllen, geben Sie eine AND-Bedingung.  
  
## Angeben einer OR Bedingung  
Mit einer OR-Bedingung können Sie mehrere alternative Werte für die Suche in einer Spalte angeben. Diese Option erweitert den Bereich der Suche und mehr Zeilen als bei der Suche nach einem einzigen Wert zurückgegeben.  
  
> [!TIP]  
> Sie können den IN-Operator häufig stattdessen nach mehreren Werten in derselben Spalte suchen verwenden.  
  
#### Angeben eine OR-Bedingung  
  
1.  In der [im Kriterienbereich](../content/Criteria-Pane--Visual-Database-Tools-.md), die zu durchsuchende Spalte hinzufügen.  
  
2.  In der **Filter** Spalte für die Datenspalte, die Sie gerade hinzugefügt, die erste Bedingung.  
  
3.  In der **oder** Spalte für dieselbe Datenspalte die zweite Bedingung angeben.  
  
Der Abfrage- und Ansicht-Designer erstellt eine WHERE-Klausel mit einer OR-Bedingung wie z. B. die folgenden:  
  
```  
SELECT fname, lname  
FROM employees  
WHERE (salary < 30000) OR (salary > 100000)  
```  
  
## Angeben einer AND-Bedingung  
Mit einer AND-Bedingung können Sie angeben, dass die Werte in einer Spalte zwei (oder mehr) Bedingungen für die Zeile im Resultset aufzunehmenden erfüllen müssen. Diese Option schränkt den Bereich der Suche und normalerweise weniger Zeilen als bei der Suche nach einem einzigen Wert zurückgegeben.  
  
> [!TIP]  
> Wenn Sie einen Bereich von Werten suchen, können Sie den Operator BETWEEN verwenden, anstatt eine Verknüpfung von zwei Bedingungen mit and.  
  
#### Angeben eine AND-Bedingung  
  
1.  Fügen Sie die zu durchsuchende Spalte im Kriterienbereich hinzu.  
  
2.  In der **Filter** Spalte für die Datenspalte, die Sie gerade hinzugefügt, die erste Bedingung.  
  
3.  Fügen Sie dieselbe Datenspalte im Kriterienbereich noch einmal, platzieren Sie sie in einer leeren Zeile des Rasters.  
  
4.  In der **Filter** Spalte für die zweite Instanz der Datenspalte die zweite Bedingung angeben.  
  
Der Abfrage-Designer erstellt eine WHERE-Klausel mit einer AND-Bedingung wie z. B. die folgenden:  
  
```  
SELECT title_id, title  
FROM titles  
WHERE (title LIKE '%Cook%') AND   
  (title LIKE '%Recipe%')  
```  
  
## Siehe auch  
[Konventionen für das Kombinieren von Suchbedingungen im Kriterienbereich & #40; Visual Database Tools & #41;](../content/Conventions-for-Combining-Search-Conditions-in-the-Criteria-Pane--Visual-Database-Tools-.md)  
[Geben Sie Suchkriterien & #40. Visual Database Tools & #41;](../content/Specify-Search-Criteria--Visual-Database-Tools-.md)  
  
