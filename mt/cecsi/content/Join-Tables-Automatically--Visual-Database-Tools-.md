---
title: "Automatisches Verkn&#252;pfen von Tabellen (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f152af82-bcb6-49ca-af19-48cdb7fc9ac6
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
# Automatisches Verkn&#252;pfen von Tabellen (Visual Database Tools)
Wenn Sie einer Abfrage zwei oder mehr Tabellen hinzufügen der [Abfrage- und Sicht-Designer](../content/Query-and-View-Designer-Tools--Visual-Database-Tools-.md) versucht zu bestimmen, ob diese verknüpft sind. Wenn dies der Fall, der Abfrage- und Ansicht-Designer automatisch Joinlinien zwischen den Rechtecken, die Tabellen bzw. darstellt\-Objekte mit Tabellenstruktur.  
  
Der Abfrage- und Sicht-Designer erkennt Tabellen unter den folgenden Umständen als verknüpft:  
  
-   Die Datenbank enthält Informationen, die angeben, dass die Tabellen verknüpft sind.  
  
-   Wenn zwei Spalten aus jeweils einer Tabelle denselben Namen und denselben Datentyp aufweisen. Die Spalte muss in mindestens einer der Tabellen ein Primärschlüssel sein. Wenn Sie z. B. die Tabellen `employee` und `jobs` hinzufügen, wobei die `job_id`-Spalte in der Tabelle `jobs` der Primärschlüssel ist und beide Tabellen eine `job_id`-Spalte mit demselben Datentyp enthalten, verknüpft der Abfrage- und Sicht-Designer die Tabellen automatisch.  
  
    > [!NOTE]  
    > Der Abfrage- und Sicht-Designer erstellt für Spalten mit demselben Namen und demselben Datentyp nur einen Join. Wenn mehrere Joins möglich sind, beendet der Abfrage- und Sicht-Designer den Vorgang nach dem Erstellen eines Joins, der auf dem ersten gefundenen Satz übereinstimmender Spalten basiert.  
  
-   Der Abfrage- und Sicht-Designer erkennt, dass eine Suchbedingung (eine WHERE-Klausel) eigentlich eine Joinbedingung ist. Sie fügen z. B. die Tabellen `employee` und `jobs` hinzu und erstellen anschließend eine Suchbedingung, die in der `job_id`-Spalte beider Tabellen nach demselben Wert sucht. Wenn Sie diesen Vorgang ausführen, erkennt der Abfrage- und Sicht-Designer, dass die Suchbedingung zu einem Join führt und erstellt anschließend eine Joinbedingung auf der Grundlage der Suchbedingung.  
  
Wenn der Abfrage- und Sicht-Designer einen Join erstellt hat, der für die Abfrage nicht geeignet ist, können Sie den Join ändern oder entfernen. Weitere Informationen finden Sie unter [Ändern von Verknüpfungsoperatoren & #40; Visual Database Tools & #41;](../content/Modify-Join-Operators--Visual-Database-Tools-.md) und [Joins & #40; entfernen Visual Database Tools & #41;](../content/Remove-Joins--Visual-Database-Tools-.md).  
  
Wenn der Abfrage- und Sicht-Designer die Tabellen in der Abfrage nicht automatisch verknüpft, können Sie selbst einen Join erstellen. Weitere Informationen finden Sie unter [Tabellen manuell verknüpfen & #40; Visual Database Tools & #41;](../content/Join-Tables-Manually--Visual-Database-Tools-.md).  
  
## Siehe auch  
[Wie der Abfrage- und Ansicht-Designer stellt Joins & #40; Visual Database Tools & #41;](../content/How-the-Query-and-View-Designer-Represents-Joins--Visual-Database-Tools-.md)  
[Entwerfen von Abfragen und Sichten Gewusst-wie-Themen & #40; Visual Database Tools & #41;](../content/Design-Queries-and-Views-How-to-Topics--Visual-Database-Tools-.md)  
[Abfragen mit Joins & #40; Visual Database Tools & #41;](../content/Query-with-Joins--Visual-Database-Tools-.md)  
  
