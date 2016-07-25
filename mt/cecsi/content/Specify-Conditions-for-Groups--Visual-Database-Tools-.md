---
title: "Angeben von Bedingungen f&#252;r Gruppen (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 269ad9c5-3261-4526-badf-7be3c869f229
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
# Angeben von Bedingungen f&#252;r Gruppen (Visual Database Tools)
Sie können die Anzahl der in einer Abfrage aufgeführten Gruppen begrenzen, indem Sie eine Bedingung angeben, die für Gruppen als Ganzes gilt – eine HAVING-Klausel. Die Bedingungen der HAVING-Klausel werden angewendet, nachdem alle Daten gruppiert und aggregiert wurden. Nur die Gruppen werden in die Abfrage aufgenommen, die die Bedingungen erfüllen.  
  
Angenommen, Sie möchten den Durchschnittspreis aller Bücher der einzelnen Herausgeber in der Tabelle `titles` anzeigen lassen, wenn dieser höher als 10,00 ist. In diesem Fall kann eine HAVING-Klausel mit folgender Bedingung angegeben werden: `AVG(price) > 10`.  
  
> [!NOTE]  
> In einigen Fällen kann es sinnvoll sein, vor Anwendung einer Bedingung auf Gruppen als Ganzes einzelne Zeilen aus den Gruppen auszuschließen. Weitere Informationen finden Sie unter [verwenden und in der WHERE-Klauseln in derselben Abfrage & #40; Visual Database Tools & #41;](../content/Use-HAVING-and-WHERE-Clauses-in-the-Same-Query--Visual-Database-Tools-.md).  
  
Sie können komplexe Bedingungen für eine HAVING-Klausel erstellen, indem Sie Bedingungen mit AND und OR verknüpfen. Weitere Informationen zum verwenden und und oder in suchbedingungen finden Sie unter [Angeben mehrerer Suchbedingungen für eine Spalte & #40; Visual Database Tools & #41;](../content/Specify-Multiple-Search-Conditions-for-One-Column--Visual-Database-Tools-.md).  
  
### So geben Sie eine Bedingung für eine Gruppe an  
  
1.  Geben Sie die Gruppen für die Abfrage an. Weitere Informationen finden Sie unter [Gruppieren von Zeilen in Abfrageergebnissen & #40; Visual Database Tools & #41;](../content/Group-Rows-in-Query-Results--Visual-Database-Tools-.md).  
  
2.  Wenn es nicht bereits in der [im Kriterienbereich](../content/Criteria-Pane--Visual-Database-Tools-.md), fügen Sie die Spalte, die die Bedingung basieren soll. (Meistens enthält die Bedingung eine bereits gruppierte bzw. zusammengefasste Spalte.) Spalten, die weder einer Aggregatfunktion noch der GROUP BY-Klausel angehören, können nicht verwendet werden.  
  
3.  In der **Filter** Spalte Geben Sie die Bedingung für die Gruppe gilt.  
  
    Die [Abfrage- und Sicht-Designer](../content/Query-and-View-Designer-Tools--Visual-Database-Tools-.md) erstellt automatisch eine HAVING-Klausel in der Anweisung in der [SQL-Bereich](../content/SQL-Pane--Visual-Database-Tools-.md), wie im folgenden Beispiel:  
  
    ```  
    SELECT pub_id, AVG(price)  
    FROM titles  
    GROUP BY pub_id  
    HAVING (AVG(price) > 10)  
    ```  
  
4.  Wiederholen Sie die Schritte 2 und 3 für jede weitere Bedingung, die angegeben werden soll.  
  
## Siehe auch  
[Sortieren und Gruppieren von Abfrageergebnissen & #40; Visual Database Tools & #41;](../content/Sort-and-Group-Query-Results--Visual-Database-Tools-.md)  
  
