---
title: "Angeben mehrerer Suchbedingungen f&#252;r mehrere Spalten (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 06617729-0d0b-4da2-9890-b7e2f5cdbc7b
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
# Angeben mehrerer Suchbedingungen f&#252;r mehrere Spalten (Visual Database Tools)
Sie können den Bereich der Abfrage erweitern oder einschränken, indem Sie verschiedene Spalten in die Suchbedingung aufnehmen. Auf diese Weise können Sie beispielsweise folgende Vorgänge durchführen:  
  
-   Sie können nach Mitarbeitern suchen, die entweder seit mehr als fünf Jahren in der Firma arbeiten oder bestimmte Tätigkeiten ausführen.  
  
-   Sie können nach einem Buch suchen, das von einem bestimmten Herausgeber veröffentlicht wurde und gleichzeitig ein Kochbuch ist.  
  
Für einer Abfrage, die in zwei oder mehr Spalten nach Werten sucht, wird eine OR-Bedingung verwendet. Demgegenüber wird zur Erstellung einer Abfrage, die alle Bedingungen in zwei oder mehr Spalten erfüllen muss, eine AND-Bedingung eingesetzt.  
  
## Angeben einer OR-Bedingung  
Wenn Sie mehrere mit OR verknüpfte Bedingungen erstellen möchten, setzen Sie jede Bedingung in eine andere Spalte des Kriterienbereichs.  
  
#### So geben Sie eine OR-Bedingung für zwei verschiedene Spalten an  
  
1.  In der [im Kriterienbereich](../content/Criteria-Pane--Visual-Database-Tools-.md), fügen Sie die Spalten, die Sie suchen möchten.  
  
2.  In der **Filter** Spalte für die erste Spalte zu suchen, geben Sie die erste Bedingung an.  
  
3.  In der **oder** -Spalte für die zweite Datenspalte zu suchen, geben Sie die zweite Bedingung an, und lassen die **Filter** Spalte leer.  
  
    Der Abfrage- und Sicht-Designer erstellt eine WHERE-Klausel mit einer OR-Bedingung, z. B.:  
  
    ```  
    SELECT job_lvl, hire_date  
    FROM employee  
    WHERE (job_lvl >= 200) OR   
      (hire_date < '01/01/1998')  
    ```  
  
4.  Wiederholen Sie die Schritte 2 und 3 für jede weitere Bedingung, die hinzugefügt werden soll. Verwenden Sie einen anderen **oder** Spalte für jede neue Bedingung.  
  
## Angeben einer AND-Bedingung  
Um verschiedene Datenspalten Startbedingungen suchen mit AND verknüpft, setzen Sie alle Bedingungen in der **Filter** Spalte des Rasters.  
  
#### So geben Sie eine AND-Bedingung für zwei verschiedene Spalten an  
  
1.  In der [im Kriterienbereich](../content/Criteria-Pane--Visual-Database-Tools-.md), fügen Sie die Spalten, die Sie suchen möchten.  
  
2.  In der **Filter** Spalte für die erste Datenspalte zu suchen, geben Sie die erste Bedingung an.  
  
3.  In der **Filter** Spalte für die zweite Datenspalte die zweite Bedingung angeben.  
  
    Der Abfrage- und Sicht-Designer erstellt eine WHERE-Klausel mit einer AND-Bedingung, z. B.:  
  
    ```  
    SELECT pub_id, title  
    FROM titles  
    WHERE (pub_id = '0877') AND (title LIKE '%Cook%')  
    ```  
  
4.  Wiederholen Sie die Schritte 2 und 3 für jede weitere Bedingung, die hinzugefügt werden soll.  
  
## Siehe auch  
[Kombinieren von Bedingungen, wenn AND hat Vorrang vor &#40; Visual Database Tools &#41;](../content/Combine-Conditions-When-AND-Has-Precedence--Visual-Database-Tools-.md)  
[Kombinieren von Bedingungen, wenn OR hat Vorrang vor &#40; Visual Database Tools &#41;](../content/Combine-Conditions-When-OR-Has-Precedence--Visual-Database-Tools-.md)  
[Konventionen für das Kombinieren von Suchbedingungen im Kriterienbereich &#40; Visual Database Tools &#41;](../content/Conventions-for-Combining-Search-Conditions-in-the-Criteria-Pane--Visual-Database-Tools-.md)  
[Geben Sie Suchkriterien &#40. Visual Database Tools &#41;](../content/Specify-Search-Criteria--Visual-Database-Tools-.md)  
  
