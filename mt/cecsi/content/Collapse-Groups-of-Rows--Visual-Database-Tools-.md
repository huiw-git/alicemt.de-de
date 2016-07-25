---
title: "Reduzieren von Zeilengruppen (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7338dad0-965d-44ba-8c1a-b993acb7156d
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
# Reduzieren von Zeilengruppen (Visual Database Tools)
Sie können ein Abfrageergebnis erstellen, in dem jede Ergebniszeile einer kompletten Zeilengruppe aus den ursprünglichen Daten entspricht. Beim Reduzieren von Zeilengruppen sind folgende Punkte zu beachten:  
  
-   **Sie können doppelte Zeilen entfernen.** Einige Abfragen erstellen Resultsets mit mehreren identischen Zeilen. Sie können z. B. ein Resultset erstellen, in dem jede Zeile den Namen der Stadt und des Lands bzw. der Region für eine Stadt angibt, in der Autoren ansässig sind. Wenn jedoch mehrere Autoren in einer Stadt ansässig sind, werden mehrere identische Zeilen ausgegeben. Hierfür kann folgende SQL-Anweisung formuliert werden:  
  
    ```  
    SELECT city, state  
    FROM authors  
    ```  
  
    Das von der oben stehenden Abfrage generierte Resultset ist nicht sehr sinnvoll. Wenn in einer Stadt vier Autoren ansässig sind, enthält das Resultset vier identische Zeilen. Da das Resultset nur Spalten für die Stadt und das Land bzw. die Region enthält, können die identischen Zeilen nicht voneinander unterschieden werden. Ein Verfahren zur Vermeidung solcher doppelten Zeilen ist das Einbinden zusätzlicher Spalten, durch die die Zeilen eindeutig werden. Z. B., wenn Sie den Namen des Autors einschließen, jede Zeile werden verschiedene (keine zwei wie bereitgestellte\-mit dem Namen in einer Stadt lebenden Autoren). Hierfür kann folgende SQL-Anweisung formuliert werden:  
  
    ```  
    SELECT city, state, fname, minit, lname  
    FROM authors  
    ```  
  
    Diese Abfrage umgeht zwar das Problem, löst es jedoch nicht. Das Resultset enthält keine Duplikate, es handelt sich aber auch nicht mehr um ein Resultset, das Aussagen zu Städten liefert. Um sowohl die Duplikate im ursprünglichen Resultset zu entfernen als auch Informationen über Städte zu erhalten, können Sie eine Abfrage erstellen, die ausschließlich eindeutige Zeilen zurückgibt. Hierfür kann folgende SQL-Anweisung formuliert werden:  
  
    ```  
    SELECT DISTINCT city, state  
    FROM authors  
    ```  
  
    Ausführliche Informationen zum Ausschließen von Duplikaten finden Sie unter [Ausschließen doppelter Zeilen & #40; Visual Database Tools & #41;](../content/Exclude-Duplicate-Rows--Visual-Database-Tools-.md).  
  
-   **Sie können Berechnungen für Zeilengruppen durchführen.** Das heißt, Sie können Informationen in Zeilengruppen zusammenfassen. Sie können z. B. ein Resultset erstellen, in dem jede Zeile die Stadt, das Land bzw. die Region für die Stadt sowie einen in dieser Stadt ansässigen Autoren enthält sowie zusätzlich die Anzahl der in dieser Stadt lebenden Autoren. Hierfür kann folgende SQL-Anweisung formuliert werden:  
  
    ```  
    SELECT city, state, COUNT(*)  
    FROM authors  
    GROUP BY city, state  
    ```  
  
    Ausführliche Informationen zum Berechnen von Gruppen von Zeilen finden Sie unter [Zusammenfassen von Abfrageergebnissen & #40; Visual Database Tools & #41;](../content/Summarize-Query-Results--Visual-Database-Tools-.md) und [Sortieren und gruppieren Abfragen Ergebnisse & #40; Visual Database Tools & #41;](../content/Sort-and-Group-Query-Results--Visual-Database-Tools-.md).  
  
-   **Sie können Auswahlkriterien verwenden, um Gruppen von Zeilen aufzunehmen.** Sie können z. B. ein Resultset erstellen, in dem jede Zeile eine Stadt enthält, in der mehrere Autoren ansässig sind, außerdem das Land bzw. die Region für diese Stadt und zusätzlich die Anzahl der in dieser Stadt ansässigen Autoren. Hierfür kann folgende SQL-Anweisung formuliert werden:  
  
    ```  
    SELECT city, state, COUNT(*)  
    FROM authors  
    GROUP BY city, state  
    HAVING COUNT(*) > 1  
    ```  
  
    Weitere Informationen zum Anwenden von Auswahlkriterien auf Zeilengruppen finden Sie unter [Bedingungen für Gruppen & #40; angeben Visual Database Tools & #41;](../content/Specify-Conditions-for-Groups--Visual-Database-Tools-.md) und [Verwenden von HAVING- und WHERE-Klauseln in derselben Abfrage & #40; Visual Database Tools & #41;](../content/Use-HAVING-and-WHERE-Clauses-in-the-Same-Query--Visual-Database-Tools-.md).  
  
## Siehe auch  
[Geben Sie Suchkriterien & #40. Visual Database Tools & #41;](../content/Specify-Search-Criteria--Visual-Database-Tools-.md)  
[Entwerfen von Abfragen und Sichten Gewusst-wie-Themen & #40; Visual Database Tools & #41;](../content/Design-Queries-and-Views-How-to-Topics--Visual-Database-Tools-.md)  
  
