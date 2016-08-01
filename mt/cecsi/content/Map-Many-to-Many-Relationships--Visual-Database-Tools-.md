---
title: "Zuordnen von m:n-Beziehungen (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2977cf92-98b5-48b2-b0fd-8fbc7040f2b4
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
# Zuordnen von m:n-Beziehungen (Visual Database Tools)
Viele\-auf\-viele-Beziehungen können Sie jede Zeile in einer Tabelle mit vielen Zeilen in einer anderen Tabelle in Beziehung setzen und umgekehrt. Sie können z. B. eine n erstellen\-\-n-Beziehung zwischen der `authors` Tabelle und die `titles` Tabelle zu allen ihren Büchern abzugleichen und zu jedem Buch alle seine Autoren zuzuordnen. Erstellen eine\-\-n-Beziehung aus beiden Tabellen würde fälschlicherweise angeben, dass jedes Buch nur einen Autor besitzen oder jeder Autor nur ein Buch schreiben kann.  
  
Viele\-auf\-viele-Beziehungen zwischen Tabellen in Datenbanken mittels Verknüpfungstabellen berücksichtigt werden. Eine Jointabelle enthält die Primärschlüsselspalten der beiden zu verknüpfenden Tabellen. Erstellen Sie dann eine Beziehung von den Primärschlüsselspalten beider Tabellen zu den korrespondierenden Spalten in der Jointabelle. In der Datenbank Pubs handelt es sich bei der Tabelle `titleauthor` um eine Jointabelle.  
  
### Erstellen Sie eine n:\-\-n-Beziehung zwischen Tabellen  
  
1.  Fügen Sie im Datenbankdiagramm die Tabellen, die Sie eine erstellen möchten\-zu\-n-Beziehung zwischen.  
  
2.  Erstellen Sie eine dritte Tabelle, indem rechts\-auf das Diagramm klicken und auswählen **neue Tabelle** aus dem Kontextmenü. Die neue Tabelle fungiert als Jointabelle.  
  
3.  In den **Namen auswählen** Dialogfeld ändern das System\-Tabellenname zugewiesen. Die Jointabelle zwischen der Tabelle `titles` und der Tabelle `authors` heißt jetzt `titleauthors`.  
  
4.  Kopieren Sie die Primärschlüsselspalten aus den beiden anderen Tabellen in die Jointabelle. Sie können der Jointabelle wie jeder anderen Tabelle weitere Spalten hinzufügen.  
  
5.  Der Primärschlüssel in der Jointabelle muss sämtliche Primärschlüsselspalten aus den beiden anderen Tabellen enthalten. Weitere Informationen finden Sie unter [How to: Create Primary Keys (Visual Database Tools)](assetId:///85c623ca-4656-4d70-a9db-ee4d897cd214).  
  
6.  Definieren Sie eine\-\-n-Beziehung zwischen jeder der beiden Primärtabellen und der Verknüpfungstabelle. Die Jointabelle muss in beiden Beziehungen die n-Seite darstellen. Weitere Informationen finden Sie unter [Gewusst wie: Erstellen von Beziehungen zwischen Tabellen (Visual Database Tools)](assetId:///867a54b8-5be4-46e6-9702-49ae6dabf67c).  
  
    > [!NOTE]  
    > Beim Erstellen einer Jointabelle in einem Datenbankdiagramm werden keine Daten aus den verknüpften Tabellen in die Jointabelle eingefügt. Informationen zum Einfügen von Daten in eine Tabelle finden Sie unter [Erstellen von Abfragen zum Einfügen von Ergebnissen & #40; Visual Database Tools & #41;](../content/Create-Insert-Results-Queries--Visual-Database-Tools-.md).  
  
## Siehe auch  
[Arbeiten Sie mit Datenbankdiagrammen & #40. Visual Database Tools & #41;](../content/Work-with-Database-Diagrams--Visual-Database-Tools-.md)  
  
