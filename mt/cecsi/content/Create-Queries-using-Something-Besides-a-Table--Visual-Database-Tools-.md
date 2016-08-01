---
title: "Erstellen von Abfragen mit anderen Quellen als einer Tabelle (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8e4a1f0a-8a42-4733-be8d-e21d6dbddb33
caps.latest.revision: 5
caps.handback.revision: 4
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
# Erstellen von Abfragen mit anderen Quellen als einer Tabelle (Visual Database Tools)
Wenn Sie eine Abrufabfrage erstellen, geben Sie die aufzunehmenden Spalten und Zeilen sowie den Ort an, von dem der Abfrageprozessor die Ausgangsdaten abrufen kann. Üblicherweise handelt es sich bei diesen Ausgangsdaten um eine Tabelle oder mehrere verknüpfte Tabellen. Die zugrunde liegenden Daten können jedoch auch aus anderen Quellen stammen. In der Tat können Sie sich von Sichten, Abfragen, Synonyme oder Benutzer stammen\-benutzerdefinierte Funktionen, die eine Tabelle zurückgeben.  
  
## Verwenden einer Sicht anstelle einer Tabelle  
Sie können Zeilen aus einer Sicht auswählen. Nehmen Sie z. B. an, dass die Datenbank eine Sicht mit der Bezeichnung "ExpensiveBooks" enthält, in der jede Zeile einen Titel mit einem Preis über 19,99 beschreibt. Die Definition der Sicht kann folgendermaßen lauten:  
  
```  
SELECT *  
FROM titles  
WHERE price > 19.99  
```  
  
Sie können alle teuren Titel zum Thema Psychologie auswählen, indem Sie einfach alle Psychologiebücher aus der Sicht ExpensiveBooks abrufen. Hierfür kann folgende SQL-Anweisung formuliert werden:  
  
```  
SELECT *  
FROM ExpensiveBooks  
WHERE type = 'psychology'  
```  
  
In ähnlicher Weise kann eine Sicht in ein JOIN-Vorgang eingebunden werden. Sie können z. B. die Verkäufe an teuren Büchern ermitteln, indem Sie die Tabelle der Verkäufe mit der Sicht ExpensiveBooks verknüpfen. Hierfür kann folgende SQL-Anweisung formuliert werden:  
  
```  
SELECT *  
FROM sales   
         INNER JOIN   
         ExpensiveBooks   
         ON sales.title_id   
         =  ExpensiveBooks.title_id  
```  
  
Weitere Informationen zu einer Abfrage eine Ansicht hinzufügen, finden Sie unter [Hinzufügen von Tabellen zu Abfragen & #40; Visual Database Tools & #41;](../content/Add-Tables-to-Queries--Visual-Database-Tools-.md).  
  
## Verwenden einer Abfrage anstelle einer Tabelle  
Sie können Zeilen aus einer Abfrage auswählen. Nehmen Sie z. B. an, dass Sie bereits eine Abfrage erstellt haben, die die Titel und IDs für Bücher zurückgibt, für die ein Mitautor angegeben ist, also alle Bücher mit mehreren Autoren. Hierfür kann folgende SQL-Anweisung formuliert werden:  
  
```  
SELECT   
     titles.title_id, title, type  
FROM   
     titleauthor   
         INNER JOIN  
         titles   
         ON titleauthor.title_id   
         =  titles.title_id   
GROUP BY   
     titles.title_id, title, type  
HAVING COUNT(*) > 1  
```  
  
Sie können nun eine weitere Abfrage erstellen, die auf diesem Ergebnis aufbaut. Dies kann z. B. eine Abfrage sein, die alle Psychologiebücher ermittelt, die von mehreren Autoren geschrieben wurden. In dieser Abfrage können Sie die bereits vorhandene Abfrage als Quelle für die neuen Abfragedaten verwenden. Hierfür kann folgende SQL-Anweisung formuliert werden:  
  
```  
SELECT   
    title  
FROM   
    (  
    SELECT   
        titles.title_id,   
        title,   
        type  
    FROM   
        titleauthor   
            INNER JOIN  
            titles   
            ON titleauthor.title_id   
            =  titles.title_id   
    GROUP BY   
        titles.title_id,   
        title,   
        type  
    HAVING COUNT(*) > 1  
    )   
    co_authored_books  
WHERE     type = 'psychology'  
```  
  
Der hervorgehobene Text zeigt die vorhandene Abfrage, die die Ausgangsdaten für die neue Abfrage liefert. Beachten Sie, dass der neuen Abfrage einen Alias verwendet ("co\_erstellte\_Books") für die vorhandene Abfrage. Weitere Informationen zu Aliasen finden Sie unter [Erstellen von Tabellenaliasen & #40; Visual Database Tools & #41;](../content/Create-Table-Aliases--Visual-Database-Tools-.md) und [Erstellen von Spaltenaliasen & #40; Visual Database Tools & #41;](../content/Create-Column-Aliases--Visual-Database-Tools-.md).  
  
In ähnlicher Weise kann eine Abfrage in ein JOIN-Vorgang eingebunden werden. Sie können z. B. die Verkäufe an teuren Büchern mit Mitautorenschaft ermitteln, indem Sie die Sicht ExpensiveBooks mit der Abfrage verknüpfen, die die Bücher mit mehreren Autoren zurückgibt. Hierfür kann folgende SQL-Anweisung formuliert werden:  
  
```  
SELECT   
    ExpensiveBooks.title  
FROM   
    ExpensiveBooks   
        INNER JOIN  
        (  
        SELECT   
            titles.title_id,   
            title,   
            type  
        FROM   
            titleauthor   
                INNER JOIN  
                titles   
                ON titleauthor.title_id   
                =  titles.title_id   
        GROUP BY   
            titles.title_id,   
            title,   
            type  
        HAVING COUNT(*) > 1  
        )  
```  
  
Weitere Informationen zu einer Abfrage eine Abfrage hinzufügen, finden Sie unter [Hinzufügen von Tabellen zu Abfragen & #40; Visual Database Tools & #41;](../content/Add-Tables-to-Queries--Visual-Database-Tools-.md).  
  
## Verwenden eines Benutzers\-benutzerdefinierten Funktion anstelle einer Tabelle  
In SQL Server 2000 oder höher verwenden, können Sie einen Benutzer erstellen\-benutzerdefinierte Funktion, die eine Tabelle zurückgibt. Solche Funktionen eignen sich zum Ausführen komplexer oder prozeduraler Logiken.  
  
Nehmen wir beispielsweise an die Employee-Tabelle enthält die zusätzliche Spalte employee.manager\_emp\_-Id und ein Fremdschlüssel-Manager vorhanden ist\_emp\_Id employee.emp\_Id. Innerhalb jeder Zeile der Tabelle der Mitarbeiter, der Manager\_emp\_Id-Spalte gibt den Vorgesetzten des Mitarbeiters an. Genauer gesagt, gibt den Vorgesetzten des Mitarbeiters emp\_Id. Sie können einen Benutzer erstellen\-benutzerdefinierte Funktion, die eine Tabelle mit jeweils einer Zeile für jeden Mitarbeiter arbeiten innerhalb einer bestimmten hohes zurückgibt\-Ebene des Managers Organisationshierarchie. Sie können die Funktion aufrufen fn\_GetWholeTeam, und so gestalten, dass eine Eingabevariable – der emp\_Id des Managers, dessen Team Sie abrufen möchten.  
  
Sie können eine Abfrage, die fn schreiben\_GetWholeTeam-Funktion als Datenquelle. Hierfür kann folgende SQL-Anweisung formuliert werden:  
  
```  
SELECT *   
FROM   
     fn_GetWholeTeam ('VPA30890F')  
```  
  
"VPA30890F" ist der emp\_Id des Managers, dessen Organisation abgerufen werden soll. Weitere Informationen zum Hinzufügen eines Benutzers\-Funktion zu einer Abfrage finden Sie unter [Hinzufügen von Tabellen zu Abfragen & #40; Visual Database Tools & #41;](../content/Add-Tables-to-Queries--Visual-Database-Tools-.md). Eine vollständige Beschreibung des Benutzers\-definierte Funktionen finden Sie unter [benutzerdefinierte Funktionen](assetId:///d7ddafab-f5a6-44b0-81d5-ba96425aada4).  
  
