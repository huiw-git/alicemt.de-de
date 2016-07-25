---
title: "Parameterabfragen (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4897c41a-324a-47b8-a30b-cbc9e9e19a8b
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
# Parameterabfragen (Visual Database Tools)
Für bestimmte Aufgaben werden Abfragen benötigt, die bei sich wiederholenden Aufrufen die Übergabe eines wechselnden Werts ermöglichen. Angenommen, Sie führen des Öfteren eine Abfrage aus, mit der alle `title_ids` eines Autors abgerufen werden. In diesem Fall führen Sie für jede Anforderung dieselbe Abfrage aus, wobei jedoch die ID bzw. der Name des Autors jeweils unterschiedlich ist.  
  
Zum Erstellen einer Abfrage, die bei jedem Aufruf mit unterschiedlichen Werten ausgeführt werden kann, verwenden Sie Parameter innerhalb der Abfrage. Ein Parameter ist ein Platzhalter für einen Wert, der erst beim Ausführen der Abfrage festgelegt wird. Eine SQL-Anweisung mit einem Parameter könnte folgendermaßen lauten, wobei "?" als Parameter für die ID des Autors dient:  
  
```  
SELECT title_id  
FROM titleauthor  
WHERE (au_id = ?)  
```  
  
## Verwendungsmöglichkeit von Parametern  
Sie können Parameter als Platzhalter für Literalwerte verwenden, d. h. sowohl für Textwerte als auch für numerische Werte. Sehr häufig werden Parameter als Platzhalter in Suchbedingungen für einzelne Zeilen oder Zeilengruppen verwendet (also in den WHERE- oder HAVING-Klauseln einer SQL-Anweisung).  
  
Sie können Parameter als Platzhalter in Ausdrücken verwenden. Angenommen, Sie möchten Rabattpreise berechnen und bei jedem Ausführen der Abfrage einen anderen Rabattwert angeben können. Hierzu lässt sich folgender Ausdruck verwenden:  
  
```  
(price * ?)  
```  
  
## Angeben unbenannter und benannter Parameter  
Sie können zwei Parametertypen angeben: unbenannte und benannte Parameter. Ein unbenannter Parameter wird durch ein Fragezeichen (?) bezeichnet, das Sie in einer Abfrage an der Position einfügen, an der Sie einen Literalwert abfragen oder einsetzen möchten. Beispielsweise, wenn Sie einen unbenannten Parameter verwenden, um nach einer Autoren Id in Suchen der `titleauthor` Tabelle, die resultierende Anweisung in der [SQL-Bereich](../content/SQL-Pane--Visual-Database-Tools-.md) könnte folgendermaßen aussehen:  
  
```  
SELECT title_id  
FROM titleauthor  
WHERE (au_id = ?)  
```  
  
Beim Ausführen der Abfrage der [Abfrage- und Sicht-Designer](../content/Query-and-View-Designer-Tools--Visual-Database-Tools-.md), die [Query Parameters Dialog Box](../content/Query-Parameters-Dialog-Box--Visual-Database-Tools-.md) wird mit "?" als Name des Parameters.  
  
Sie können einem Parameter auch einen Namen zuweisen. Benannte Parameter sind dann hilfreich, wenn in einer Abfrage mehrere Parameter enthalten sind. Wenn Sie z. B. benannte Parameter für die Suche nach dem Vor- und Nachnamen eines Autors in der Tabelle `authors` verwenden, ergibt sich folgende Anweisung im SQL-Bereich:  
  
```  
SELECT au_id  
FROM authors  
WHERE au_fname = %first name% AND  
      au_lname = %last name%  
```  
  
> [!TIP]  
> Definieren Sie Präfix- und Suffixzeichen, bevor Sie eine Abfrage mit benannten Parametern erstellen.  
  
Beim Ausführen der Abfrage im Abfrage- und Ansicht-Designer die [Query Parameters Dialog Box](../content/Query-Parameters-Dialog-Box--Visual-Database-Tools-.md) mit einer Liste benannter Parameter angezeigt.  
  
## Siehe auch  
[Abfrage mit Parametern & #40; Visual Database Tools & #41;](../content/Query-with-Parameters--Visual-Database-Tools-.md)  
[Unterstützte Abfragetypen & #40; Visual Database Tools & #41;](../content/Supported-Query-Types--Visual-Database-Tools-.md)  
[Entwerfen von Abfragen und Sichten Gewusst-wie-Themen & #40; Visual Database Tools & #41;](../content/Design-Queries-and-Views-How-to-Topics--Visual-Database-Tools-.md)  
  
