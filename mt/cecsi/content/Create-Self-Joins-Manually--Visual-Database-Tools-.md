---
title: "Manuelles Erstellen von Selbstjoins (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 910ed516-cb84-481b-95d0-cba3e89afdba
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
# Manuelles Erstellen von Selbstjoins (Visual Database Tools)
Sie können eine Tabelle mit sich selbst verknüpfen, auch wenn die Tabelle über keine reflexive Beziehung in der Datenbank verfügt. Sie können z. B. eine selbst\-Join in derselben Stadt lebenden Autoren suchen.  
  
Wie bei jedem Join eines\-Join erfordert mindestens zwei Tabellen. Der Unterschied besteht darin, dass Sie der Abfrage keine zweite Tabelle, sondern eine zweite Instanz derselben Tabelle hinzufügen. Auf diese Weise können Sie eine Spalte in der ersten Instanz der Tabelle mit derselben Spalte in der zweiten Instanz vergleichen, wodurch Sie die Werte einer Spalte miteinander vergleichen können. Die [Abfrage- und Sicht-Designer](../content/Query-and-View-Designer-Tools--Visual-Database-Tools-.md) der zweiten Instanz der Tabelle einen Alias zugewiesen.  
  
Z. B. bei der Erstellung eines\-zum Suchen aller autorenpaare in Berkeley verknüpfen, die Sie vergleichen die `city` Spalte in der ersten Instanz der Tabelle mit der `city` -Spalte in der zweiten Instanz. Die entsprechende Abfrage könnte folgendermaßen aussehen:  
  
```  
SELECT   
         authors.au_fname,   
         authors.au_lname,   
         authors1.au_fname AS Expr2,   
         authors1.au_lname AS Expr3  
      FROM   
         authors   
            INNER JOIN  
            authors authors1   
               ON authors.city   
                = authors1.city  
      WHERE  
         authors.city = 'Berkeley'  
```  
  
Erstellen eines\-Join erfordert oft mehrere Joinbedingungen. Die Gründe dafür werden aus dem Ergebnis der vorherigen Abfrage ersichtlich:  
  
```  
Cheryl Carson       Cheryl Carson  
   Abraham Bennet      Abraham Bennet  
   Cheryl Carson       Abraham Bennet  
   Abraham Bennet      Cheryl Carson  
```  
  
Die erste Zeile ist ohne Belang; sie gibt an, dass Cheryl Carson in derselben Stadt wie Cheryl Carson lebt. Die zweite Zeile wird ebenfalls nicht benötigt. Fügen Sie eine weitere Bedingung hinzu, durch die nur die Ergebniszeilen beibehalten werden, in denen die Autorennamen verschiedene Autoren bezeichnen, um diese überflüssigen Daten auszuschließen. Die entsprechende Abfrage könnte folgendermaßen aussehen:  
  
```  
SELECT   
         authors.au_fname,   
         authors.au_lname,   
         authors1.au_fname AS Expr2,   
         authors1.au_lname AS Expr3  
      FROM   
         authors   
            INNER JOIN  
            authors authors1   
               ON authors.city   
                = authors1.city  
               AND authors.au_id  
                <> authors1.au_id  
      WHERE  
         authors.city = 'Berkeley'  
```  
  
Das Resultset wurde verbessert:  
  
```  
Cheryl Carson       Abraham Bennet  
   Abraham Bennet      Cheryl Carson  
```  
  
Die zwei Ergebniszeilen sind jedoch redundant. Die erste Zeile gibt an, dass Carson in derselben Stadt wie Bennet lebt, und mit der zweiten Zeile wird angegeben, dass Bennet in derselben Stadt wie Carson lebt. Sie können Sie die zweite Joinbedingung von "ungleich" in "kleiner als" ändern, um diese Redundanz auszuschließen. Die entsprechende Abfrage könnte folgendermaßen aussehen:  
  
```  
SELECT   
         authors.au_fname,   
         authors.au_lname,   
         authors1.au_fname AS Expr2,   
         authors1.au_lname AS Expr3  
      FROM   
         authors   
            INNER JOIN  
            authors authors1   
               ON authors.city   
                = authors1.city  
               AND authors.au_id  
                < authors1.au_id  
      WHERE  
         authors.city = 'Berkeley'  
```  
  
Das Resultset sieht wie folgt aus:  
  
```  
Cheryl Carson       Abraham Bennet  
```  
  
### Erstellen eines\-manuell verknüpfen  
  
1.  Hinzufügen der [Diagrammbereich](../content/Diagram-Pane--Visual-Database-Tools-.md) der Tabelle oder\-bewertet Objekt Sie arbeiten möchten.  
  
2.  Hinzufügen dieselbe Tabelle erneut, sodass im Diagrammbereich angezeigt, der gleichen Tabelle oder wird\-bewertet Objekt im Diagrammbereich zweimal.  
  
    Der Abfrage- und Sicht-Designer weist der zweiten Instanz einen Alias zu, indem dem Tabellennamen eine laufende Nummer hinzugefügt wird. Darüber hinaus der Abfrage- und Ansicht-Designer eine Joinlinie zwischen den beiden Instanzen der Tabelle oder der Tabelle erstellt\-bewertet Objekt im Diagrammbereich.  
  
3.  Rechts\-Klicken Sie auf die Joinlinie, und wählen Sie **Eigenschaften** aus dem Kontextmenü.  
  
4.  Klicken Sie im Fenster Eigenschaften auf **Joinbedingung und-Typ** und klicken Sie auf die **Auslassungspunkte (...)** rechts neben der Eigenschaft.  
  
5.  In der [im Dialogfeld Join](../content/Join-Dialog-Box--Visual-Database-Tools-.md) den Vergleichsoperator zwischen den Primärschlüsseln nach Bedarf ändern. Sie können z. B. den Operator in "kleiner als" (<) ändern.  
  
6.  Erstellen Sie die zusätzliche Joinbedingung (z. B. authors.zip \= authors1.zip) durch Ziehen der Name der primären Joinspalte aus der ersten Instanz der Tabelle oder der Tabelle\-Werten Objekt und der entsprechenden Spalte der zweiten Instanz ablegen.  
  
7.  Geben Sie weitere Optionen für die Abfrage an (z. B. Ausgabespalten, Suchbedingungen und Sortierreihenfolge).  
  
## Siehe auch  
[Erstellen Sie Verknüpfungen automatisch & #40; Visual Database Tools & #41;](../content/Create-Self-Joins-Automatically--Visual-Database-Tools-.md)  
[Abfragen mit Joins & #40; Visual Database Tools & #41;](../content/Query-with-Joins--Visual-Database-Tools-.md)  
  
