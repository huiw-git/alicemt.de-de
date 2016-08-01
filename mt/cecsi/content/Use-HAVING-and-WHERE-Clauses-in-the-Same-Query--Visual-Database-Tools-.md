---
title: "Verwenden von HAVING- und WHERE-Klauseln in derselben Abfrage (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1e07cf56-b4b7-4c49-8ddd-c276812a7148
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
# Verwenden von HAVING- und WHERE-Klauseln in derselben Abfrage (Visual Database Tools)
In einigen Fällen kann es sinnvoll sein, einzelne Zeilen aus Gruppen auszuschließen (mit einer WHERE-Klausel), bevor eine Bedingung auf Gruppen als Ganzes (mithilfe der HAVING-Klausel) angewendet wird.  
  
Die HAVING-Klausel ähnelt der WHERE-Klausel, gilt jedoch nur für Gruppen als Ganzes (d. h. für die Zeilen im Resultset, die Gruppen darstellen), während die WHERE-Klausel auf einzelne Zeilen angewendet wird. Eine Abfrage kann sowohl eine WHERE-Klausel als auch eine HAVING-Klausel enthalten. Dabei trifft Folgendes zu:  
  
-   Die WHERE-Klausel auf die einzelnen Zeilen in der Tabelle oder Tabellen zuerst angewendet wird\-Objekte im Bereich Diagramm bewertet. Gruppiert werden nur die Zeilen, die die Bedingungen der WHERE-Klausel erfüllen.  
  
-   Die HAVING-Klausel wird dann im Resultset auf die Zeilen angewendet. Nur die Gruppen werden in das Abfrageergebnis aufgenommen, die die HAVING-Bedingungen erfüllen. Die HAVING-Klausel kann nur auf Spalten angewendet werden, die auch Teil einer GROUP BY-Klausel oder einer Aggregatfunktion sind.  
  
Angenommen, Sie verknüpfen die Tabellen `titles` und `publishers`, um eine Abfrage zu erstellen, in der der durchschnittliche Buchpreis für eine Gruppe von Herstellern angezeigt wird. Der Durchschnittspreis soll jedoch nur für eine bestimmte Gruppe von Herausgebern angezeigt werden, beispielsweise nur für die Herausgeber in Kalifornien. Außerdem sollen nur Durchschnittspreise über 10,00 $ in der Ausgabe angezeigt werden.  
  
Die erste Bedingung können Sie mithilfe einer WHERE-Klausel aufbauen, durch die Hersteller, die nicht aus Kalifornien stammen, vor der Berechnung der Durchschnittspreise verworfen werden. Die zweite Bedingung erfordert eine HAVING-Klausel, da sie auf den Ergebnissen einer Gruppierung und Zusammenfassung von Daten aufbaut. Die resultierende SQL-Anweisung könnte folgendermaßen aussehen:  
  
```  
SELECT titles.pub_id, AVG(titles.price)  
FROM titles INNER JOIN publishers  
   ON titles.pub_id = publishers.pub_id  
WHERE publishers.state = 'CA'  
GROUP BY titles.pub_id  
HAVING AVG(price) > 10  
```  
  
Sie können im Kriterienbereich sowohl HAVING-Klauseln als auch WHERE-Klauseln erstellen. Wenn Sie eine Suchbedingung für eine Spalte angeben, wird diese Bedingung standardmäßig zu einem Bestandteil der HAVING-Klausel. Sie können die Bedingung jedoch auch in eine WHERE-Klausel ändern.  
  
Für dieselbe Spalte kann sowohl eine WHERE-Klausel als auch eine HAVING-Klausel erstellt werden. Dazu müssen Sie die Spalte zunächst zweimal im Kriterienbereich einfügen und dann eine Instanz als Teil der HAVING-Klausel und die andere Instanz als Teil der WHERE-Klausel angeben.  
  
### So legen Sie eine WHERE-Bedingung in einer Aggregatabfrage fest  
  
1.  Geben Sie die Gruppen für die Abfrage an. Weitere Informationen finden Sie unter [Gruppieren von Zeilen in Abfrageergebnissen &#40; Visual Database Tools &#41;](../content/Group-Rows-in-Query-Results--Visual-Database-Tools-.md).  
  
2.  Fügen Sie dem Kriterienbereich die Spalte hinzu, auf der die WHERE-Bedingung basieren soll, sofern diese dort nicht bereits vorhanden ist.  
  
3.  Deaktivieren der **Ausgabe** Spalte, wenn die Datenspalte Teil der GROUP BY-Klausel oder in einer Aggregatfunktion enthalten ist.  
  
4.  In der **Filter** Spalte, die WHERE-Bedingung angeben. Der Abfrage- und Sicht-Designer fügt der HAVING-Klausel der SQL-Anweisung die Bedingung hinzu.  
  
    > [!NOTE]  
    > In der im Beispiel für diese Prozedur dargestellten Abfrage werden die beiden Tabellen `titles` und `publishers` miteinander verknüpft.  
  
    An dieser Stelle der Abfrage enthält die SQL-Anweisung eine HAVING-Klausel:  
  
    ```  
    SELECT titles.pub_id, AVG(titles.price)  
    FROM titles INNER JOIN publishers   
       ON titles.pub_id = publishers.pub_id  
    GROUP BY titles.pub_id  
    HAVING publishers.state = 'CA'  
    ```  
  
5.  In der **Group By** Spalte **in dem** aus der Liste von Gruppierungs- und Zusammenfassungsoptionen. Der Abfrage- und Sicht-Designer entfernt die Bedingung aus der HAVING-Klausel in der SQL-Anweisung und fügt sie der WHERE-Klausel hinzu.  
  
    Daraufhin wird stattdessen eine WHERE-Klausel in die SQL-Anweisung eingebunden:  
  
    ```  
    SELECT titles.pub_id, AVG(titles.price)  
    FROM titles INNER JOIN publishers   
       ON titles.pub_id = publishers.pub_id  
    WHERE publishers.state = 'CA'  
    GROUP BY titles.pub_id  
    ```  
  
## Siehe auch  
[Sortieren und Gruppieren von Abfrageergebnissen &#40; Visual Database Tools &#41;](../content/Sort-and-Group-Query-Results--Visual-Database-Tools-.md)  
[Zusammenfassen von Abfrageergebnissen &#40; Visual Database Tools &#41;](../content/Summarize-Query-Results--Visual-Database-Tools-.md)  
  
