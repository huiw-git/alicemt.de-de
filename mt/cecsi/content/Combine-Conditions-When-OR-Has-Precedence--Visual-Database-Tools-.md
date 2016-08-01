---
title: "Kombinieren von Bedingungen, wenn OR Vorrang hat (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b30f5ac9-25e7-4163-80ed-44e4bccb455d
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
# Kombinieren von Bedingungen, wenn OR Vorrang hat (Visual Database Tools)
Wenn die mit OR verbundene Bedingungen den Vorrang vor den mit AND verbundenen Bedingungen haben sollen, muss die AND-Bedingung für jede OR-Bedingung wiederholt werden.  
  
Angenommen, Sie möchten alle Mitarbeiter suchen, die seit mehr als fünf Jahren für das Unternehmen und haben niedrigere\-Aufträge Ebene oder im Ruhestand sind. Diese Abfrage erfordert drei Bedingungen: eine einzelne Bedingung, die mit zwei weiteren Bedingungen durch AND verknüpft ist:  
  
-   Mitarbeiter, deren Einstellungsdatum mehr als fünf Jahre zurückliegt und  
  
-   Mitarbeiter mit einer Tätigkeitsstufe von 100 oder Mitarbeiter, deren Status "R" (Ruhestand) ist.  
  
Das folgende Verfahren illustriert die Erstellung einer derartigen Abfrage im Kriterienbereich.  
  
### So kombinieren Sie Bedingungen, wenn OR Vorrang hat  
  
1.  In der [im Kriterienbereich](../content/Criteria-Pane--Visual-Database-Tools-.md), fügen Sie die Datenspalten, die Sie suchen möchten. Wenn Sie dieselbe Spalte nach zwei oder mehr mit AND verbundenen Bedingungen durchsuchen möchten, müssen Sie den Namen der Datenspalte für jeden zu suchenden Wert einmal in das Datenblatt einfügen.  
  
2.  Erstellen Sie die Bedingung mit oder durch Eingabe der ersten in der **Filter** Spalte und zweiten (und alle weiteren) in Separate **oder** Spalten. Beispielsweise Bedingungen mit OR zum Durchsuchen der `job_lvl` und `status` Spalten geben Sie `= 100` in die **Filter** Spalte für `job_lvl` und `= 'R'` in der **oder** Spalte für `status`.  
  
    Wenn Sie diese Werte im Datenblatt eingeben, wird die folgende WHERE-Klausel in der Anweisung im SQL-Bereich erstellt:  
  
    ```  
    WHERE (job_lvl = 100) OR (status = 'R')  
    ```  
  
3.  Erstellen Sie die AND-Bedingung, indem Sie sie für jede OR-Bedingungen einmal eingeben. Nehmen Sie den Eintrag jeweils in der Datenblattspalte der entsprechenden OR-Bedingung vor. Beispielsweise, um eine AND-Bedingung hinzuzufügen, sucht die `hire_date` Spalte und wendet auf beide OR-Bedingungen, geben Sie `< '1/1/91'` in die Spalte Kriterien und der **oder** Spalte.  
  
    Wenn Sie diese Werte im Datenblatt eingeben, wird die folgende WHERE-Klausel in der Anweisung im SQL-Bereich erstellt:  
  
    ```  
    WHERE (job_lvl = 100) AND   
      (hire_date < '01/01/91' ) OR  
      (status = 'R') AND   
      (hire_date < '01/01/91' )  
    ```  
  
    > [!TIP]  
    > Sie können eine AND-Bedingung wiederholen, indem sie einmal, und klicken Sie dann mit Hinzufügen der **Ausschneiden** und **Einfügen** Befehle der **Bearbeiten** Menü für die anderen OR-Bedingungen kopieren.  
  
Die WHERE-Klausel, die vom Abfrage- und Sicht-Designer erstellt wird, entspricht der folgenden WHERE-Klausel, in der zum Festlegen des Vorrangs von OR vor AND Klammern verwendet werden:  
  
```  
WHERE (job_lvl = 100 OR status = 'R') AND  
   (hire_date < '01/01/91')  
```  
  
> [!NOTE]  
> Wenn Sie die suchbedingungen im unmittelbar im oben gezeigten Format eingeben der [SQL-Bereich](../content/SQL-Pane--Visual-Database-Tools-.md), aber nehmen Sie eine Änderung an die Abfrage im Diagramm- oder Kriterienbereich-Bereiche, die Abfrage und Sicht-Designer die SQL-Anweisung mit explizit auf beide OR-Bedingungen verteilte AND-Bedingung der Form entsprechend neu.  
  
## Siehe auch  
[Konventionen für das Kombinieren von Suchbedingungen im Kriterienbereich & #40; Visual Database Tools & #41;](../content/Conventions-for-Combining-Search-Conditions-in-the-Criteria-Pane--Visual-Database-Tools-.md)  
[Geben Sie Suchkriterien & #40. Visual Database Tools & #41;](../content/Specify-Search-Criteria--Visual-Database-Tools-.md)  
  
