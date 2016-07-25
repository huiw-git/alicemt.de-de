---
title: "Erstellen von &#228;u&#223;eren Joins (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 18de47b1-f936-427d-b852-fe6d20334f71
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
# Erstellen von &#228;u&#223;eren Joins (Visual Database Tools)
In der Standardeinstellung die [Abfrage- und Sicht-Designer](../content/Query-and-View-Designer-Tools--Visual-Database-Tools-.md) erstellt eine innere Verknüpfung zwischen Tabellen. Innere Joins entfernen die Zeilen, die nicht mit einer Zeile aus der anderen Tabelle übereinstimmen. Äußere Joins dagegen geben alle Zeilen aus mindestens einer der in der FROM-Klausel genannten Tabellen oder Sichten zurück, sofern diese Zeilen ggf. die WHERE- oder HAVING-Suchbedingungen erfüllen. Wenn Sie Datenzeilen in das Resultset einschließen möchten, die keine Übereinstimmung in der verknüpften Tabelle aufweisen, können Sie einen äußeren Join erstellen.  
  
Beim Erstellen eines äußeren Join ist die Reihenfolge relevant, in der Tabellen in der SQL-Anweisung angezeigt werden (wie im SQL-Bereich widergespiegelt). Die zuerst hinzugefügte Tabelle wird als "linke" Tabelle und die zweite hinzugefügte Tabelle als "rechte" Tabelle betrachtet. (Die tatsächliche Reihenfolge, in der die Tabellen angezeigt, in werden, der [Diagrammbereich](../content/Diagram-Pane--Visual-Database-Tools-.md) spielt keine Rolle.) Bei der Angabe eines linken oder rechten äußeren Joins verweisen Sie auf die Reihenfolge, in der die Tabellen hinzugefügt wurden, um die Abfrage und die Reihenfolge, in der SQL-Anweisung im, der [SQL-Bereich](../content/SQL-Pane--Visual-Database-Tools-.md).  
  
### So erstellen Sie einen äußeren Joins  
  
1.  Erstellen Sie den Joins automatisch oder manuell. Weitere Informationen finden Sie unter [& #40; Tabellen automatisch verknüpfen Visual Database Tools & #41;](../content/Join-Tables-Automatically--Visual-Database-Tools-.md) oder [Manuelles Verknüpfen von Tabellen & #40; Visual Database Tools & #41;](../content/Join-Tables-Manually--Visual-Database-Tools-.md).  
  
2.  Wählen Sie die Verknüpfungslinie im Diagrammbereich und dann von der **-Abfrage-Designer** Menü wählen **aus <tablename>**, wählen Sie den Befehl, der die Tabelle enthält, deren zusätzlichen Zeilen enthalten sein sollen.  
  
    -   Wählen Sie die erste Tabelle aus, um eine linken äußeren Joins zu erstellen.  
  
    -   Wählen Sie die zweite Tabelle aus, um eine rechten äußeren Joins zu erstellen.  
  
    -   Wählen Sie beide Tabellen aus, um eine vollständigen äußeren Joins zu erstellen.  
  
Wenn Sie angeben, ändert der Abfrage- und Sicht-Designer die Joinlinie zum Anzeigen eines äußeren Joins.  
  
Außerdem ändert der Abfrage- und Sicht-Designer die SQL-Anweisung im SQL-Bereich, um die Änderung des Jointyps widerzuspiegeln, wie in der folgenden Anweisung dargestellt:  
  
```  
SELECT employee.job_id, employee.emp_id,  
   employee.fname, employee.minit, jobs.job_desc  
FROM employee LEFT OUTER JOIN jobs ON   
    employee.job_id = jobs.job_id  
```  
  
Da ein äußerer Join Zeilen ohne Übereinstimmungen einschließt, kann diese zum Suchen von Zeilen verwendet werden, die Fremdschlüsseleinschränkungen verletzen. Erstellen Sie hierzu einen äußeren Join, und fügen Sie anschließend eine Suchbedingung zum Suchen von Zeilen hinzu, in denen die Primärschlüsselspalte der äußersten rechten Tabelle Null ist. Mit dem folgenden äußeren Join werden z. B. Zeilen in der Tabelle `employee` gesucht, für die keine übereinstimmenden Zeilen in der Tabelle `jobs` vorhanden sind:  
  
```  
SELECT employee.emp_id, employee.job_id  
FROM employee LEFT OUTER JOIN jobs   
   ON employee.job_id = jobs.job_id  
WHERE (jobs.job_id IS NULL)  
```  
  
## Siehe auch  
[Abfragen mit Joins & #40; Visual Database Tools & #41;](../content/Query-with-Joins--Visual-Database-Tools-.md)  
[Nehmen Sie im Dialogfeld & #40; Visual Database Tools & #41;](../content/Join-Dialog-Box--Visual-Database-Tools-.md)  
  
