---
title: "Konventionen f&#252;r das Kombinieren von Suchbedingungen im Kriterienbereich (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d4859be5-ff5b-48b2-a101-ad40c6dbcc68
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
# Konventionen f&#252;r das Kombinieren von Suchbedingungen im Kriterienbereich (Visual Database Tools)
Abfragen können eine beliebige Anzahl von Suchbedingungen enthalten, die mit beliebig vielen AND-Operatoren und OR-Operatoren verknüpft werden können. Eine Abfrage mit einer Kombination aus und und oder Klauseln kann sehr komplex, daher ist es hilfreich zu verstehen, wie eine solche Abfrage interpretiert wird bei der Ausführung und wie eine solche Abfrage dargestellt wird, in der [im Kriterienbereich](../content/Criteria-Pane--Visual-Database-Tools-.md) und [SQL-Bereich](../content/SQL-Pane--Visual-Database-Tools-.md).  
  
> [!NOTE]  
> Weitere Informationen zu suchbedingungen, die nur einen enthalten und OR-Operator finden Sie unter [Angeben mehrerer Suchbedingungen für eine Spalte & #40; Visual Database Tools & #41;](../content/Specify-Multiple-Search-Conditions-for-One-Column--Visual-Database-Tools-.md) und [Angeben mehrerer Suchbedingungen für mehrere Spalten & #40; Visual Database Tools & #41;](../content/Specify-Multiple-Search-Conditions-for-Multiple-Columns--Visual-Database-Tools-.md).  
  
Nachstehend erhalten Sie Informationen zu den folgenden Themen:  
  
-   Der Vorrang von AND und OR in Abfragen mit beiden Operatoren.  
  
-   Die logische Beziehung der Bedingungen in AND-Klauseln und OR-Klauseln.  
  
-   Die Darstellung von Abfragen, die AND und OR enthalten, durch den Abfrage- und Sicht-Designer im Kriterienbereich.  
  
In den Beispielen in den folgenden Abschnitten wird eine `employee`-Tabelle verwendet, die die Spalten `hire_date`, `job_lvl` und `status` enthält. In den Beispielen wird angenommen, dass Sie Informationen suchen, beispielsweise die Betriebszugehörigkeit eines Mitarbeiters (Einstellungsdatum), die Art der Tätigkeit des Mitarbeiters (Stellenbeschreibung) und den Mitarbeiterstatus (z. B. Ruhestand).  
  
## Vorrang von AND und OR  
Bei der Ausführung einer Abfrage werden zuerst die mit AND verknüpften Klauseln und anschließend die mit OR verknüpften Klauseln ausgewertet.  
  
> [!NOTE]  
> Der NOT-Operator hat gegenüber AND und OR Vorrang.  
  
Z. B. entweder Mitarbeiter suchen, die mit dem Unternehmen mehr als fünf Jahren in der unteren waren\-Aufträge oder Mitarbeiter mit der mittleren Ebene\-Ebene Aufträge ohne Berücksichtigung von Einstellungsdatum, können Sie eine WHERE-Klausel wie im folgenden erstellen:  
  
```  
WHERE   
   hire_date < '01/01/95' AND   
   job_lvl = 100 OR  
   job_lvl = 200  
```  
  
Zum Überschreiben des Standardvorrangs von AND gegenüber OR können Sie Klammern um bestimmte Bedingungen im SQL-Bereich setzen. Bedingungen in Klammern werden immer zuerst ausgewertet. Z. B. zum Suchen, die alle Mitarbeiter, die mit dem Unternehmen wurden mehr als fünf Jahre in einem senken oder mittleren\-Ebene Aufträge, können Sie eine WHERE-Klausel wie im folgenden erstellen:  
  
```  
WHERE   
   hire_date < '01/01/95' AND   
   (job_lvl = 100 OR job_lvl = 200)  
```  
  
> [!TIP]  
> Es wird empfohlen, aus Gründen der Übersichtlichkeit beim Kombinieren von AND-Klauseln und OR-Klauseln immer Klammern zu setzen, auch wenn der Standardvorrang gilt.  
  
## Verwenden von AND mit mehreren OR-Klauseln  
Wenn Sie wissen, wie AND-Klauseln und OR-Klauseln beim Kombinieren miteinander verknüpft werden, erleichtert dies das Erstellen und Verstehen komplexer Abfragen im Abfrage- und Sicht-Designer.  
  
Wenn Sie mehrere Bedingungen mit AND verknüpfen, gilt der erste Satz der mit AND verknüpften Bedingungen für alle Bedingungen im zweiten Satz. Das heißt, dass eine Bedingung, die durch AND mit einer anderen Bedingung verknüpft ist, an alle Bedingungen im zweiten Satz verteilt wird. Die folgende schematische Darstellung enthält eine mit einem Satz von OR-Bedingungen verknüpfte AND-Bedingung:  
  
```  
A AND (B OR C)  
```  
  
Die Darstellung ist logisch equivalent zu der folgenden schematischen Darstellung, die zeigt, wie sich die AND-Bedingung zum zweiten Satz von Bedingungen verhält:  
  
```  
(A AND B) OR (A AND C)  
```  
  
Dieses Distributivprinzip beeinflusst auch die Verwendung des Abfrage- und Sicht-Designers. Angenommen, dass Sie für alle Mitarbeiter suchen, die mit mehr als fünf Jahren in einer unteren oder mittleren Unternehmen wurden\-Ebene Aufträge. Geben Sie die folgende WHERE-Klausel im SQL-Bereich in die Anweisung ein:  
  
```  
WHERE (hire_date < '01/01/95' ) AND   
   (job_lvl = 100 OR job_lvl = 200)  
```  
  
Die mit AND verknüpfte Klausel gilt für beide mit OR verknüpften Klauseln. Sie können dies auch durch Wiederholen der AND-Bedingung für jede Bedingung in der OR-Klausel ausdrücken. Die folgende Anweisung ist genauer (und länger) als die vorhergehende Anweisung, ist jedoch logisch equivalent:  
  
```  
WHERE    (hire_date < '01/01/95' ) AND  
  (job_lvl = 100) OR   
  (hire_date < '01/01/95' ) AND   
  (job_lvl = 200)  
```  
  
Die Distribution von AND-Klauseln zu verknüpften OR-Klauseln kann immer angewendet werden, unabhängig von der Anzahl von einzelnen Bedingungen. Angenommen, Sie höheren oder mittleren möchten\-Ebene Mitarbeiter, die seit mehr als fünf Jahren für das Unternehmen oder im Ruhestand sind. Die entsprechende WHERE-Klausel kann folgendermaßen lauten:  
  
```  
WHERE   
   (job_lvl = 200 OR job_lvl = 300) AND  
   (hire_date < '01/01/95' ) OR (status = 'R')  
```  
  
Nachdem die mit AND verknüpften Bedingungen verteilt wurden, ergibt sich folgende WHERE-Klausel:  
  
```  
WHERE   
   (job_lvl = 200 AND hire_date < '01/01/95' ) OR  
   (job_lvl = 200 AND status = 'R') OR  
   (job_lvl = 300 AND hire_date < '01/01/95' ) OR  
   (job_lvl = 300 AND status = 'R')  
```  
  
## Darstellung mehrerer AND-Klauseln und OR-Klauseln im Kriterienbereich  
Der Abfrage- und Ansicht-Designer stellt die suchbedingungen in der [im Kriterienbereich](../content/Criteria-Pane--Visual-Database-Tools-.md). Bei mehreren mit AND und OR verknüpften Klauseln kann diese Darstellung im Kriterienbereich jedoch abweichen. Darüber hinaus, wenn Sie die Abfrage im Kriterienbereich ändern oder [Diagrammbereich](../content/Diagram-Pane--Visual-Database-Tools-.md), möglicherweise, dass die SQL-Anweisung geändert wurde, was Sie eingegeben haben.  
  
Diese Regeln legen grundsätzlich fest, wie AND- und OR-Klauseln im Kriterienbereich angezeigt werden:  
  
-   Alle mit AND verknüpften Bedingungen werden in der **Filter** Spalte oder in derselben **oder** Spalte.  
  
-   Alle mit OR verknüpften Bedingungen werden in separaten **oder** Spalten.  
  
-   Wenn das logische Ergebnis einer Kombination von AND- und OR-Klauseln die Verteilung von AND in verschiedene OR-Klauseln ist, wird dies im Kriterienbereich entsprechend angezeigt, indem die AND-Klausel so oft wie erforderlich wiederholt wird.  
  
Sie könnten z. B. im SQL-Bereich eine Suchbedingung nach folgendem Muster erstellen. Dabei haben zwei mit AND verknüpfte Klauseln Vorrang gegenüber einer dritten mit OR verknüpften Klausel:  
  
```  
WHERE (hire_date < '01/01/95' ) AND   
  (job_lvl = 100) OR   
  (status = 'R')  
```  
  
Diese WHERE-Klausel wird vom Abfrage- und Sicht-Designer folgendermaßen im Kriterienbereich dargestellt:  
  
![OR-Klauselrangfolge im Kriterienbereich](../content/media/vs_criteriapane1.png "vs_criteriapane1")  
  
Wenn die verknüpfte OR-Klausel Vorrang vor einer AND-Klausel erhält, wird die AND-Klausel für jede OR-Klausel wiederholt. Dadurch wird die AND-Klausel an jede OR-Klausel verteilt. Sie können im SQL-Bereich z. B. folgende WHERE-Klausel erstellen:  
  
```  
WHERE (hire_date < '01/01/95' ) AND   
  ( (job_lvl = 100) OR   
  (status = 'R') )  
```  
  
Diese WHERE-Klausel wird vom Abfrage- und Sicht-Designer folgendermaßen im Kriterienbereich dargestellt:  
  
![Mehrere AND- und OR-Klauseln im Kriterienbereich](../content/media/vs_criteriapane2.png "vs_criteriapane2")  
  
Wenn die verknüpften OR-Klauseln nur eine Datenspalte enthalten, kann der Abfrage- und Sicht-Designer die gesamte OR-Klausel in eine Zelle des DatenBlatts einfügen, sodass die AND-Klausel nicht ständig wiederholt werden muss. Sie können im SQL-Bereich z. B. folgende WHERE-Klausel erstellen:  
  
```  
WHERE (hire_date < '01/01/95' ) AND   
  ((status = 'R') OR (status = 'A'))  
```  
  
Diese WHERE-Klausel wird vom Abfrage- und Sicht-Designer folgendermaßen im Kriterienbereich dargestellt:  
  
![Im Kriterienbereich definierte verknüpfte OR-Klauseln](../content/media/vs_criteriapane3.png "vs_criteriapane3")  
  
Wenn Sie die Abfrage ändern (z. B. durch Ändern eines der Werte im Kriterienbereich), erstellt der Abfrage- und Sicht-Designer die SQL-Anweisung im SQL-Bereich neu. Die neu erstellte SQL-Anweisung stimmt eher mit der Anzeige im Kriterienbereich als mit der ursprünglichen Anweisung überein. Wenn der Kriterienbereich z. B. verteilte AND-Klauseln enthält, wird die Anweisung im SQL-Bereich mit eindeutig verteilten AND-Klauseln erstellt. Ausführliche Informationen finden Sie weiter oben unter "Verwenden von AND mit mehreren OR-Klauseln".  
  
## Siehe auch  
[Geben Sie Suchkriterien & #40. Visual Database Tools & #41;](../content/Specify-Search-Criteria--Visual-Database-Tools-.md)  
  
