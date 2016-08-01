---
title: "Entwerfen von Datenbankdiagrammen (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6d2c14e1-3d73-4d10-ae5b-7f2b5d6c4ea8
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
# Entwerfen von Datenbankdiagrammen (Visual Database Tools)
Der Datenbank-Designer ist ein visuelles Tool, mit dem Sie eine Datenbank, mit der eine Verbindung besteht, entwerfen und anzeigen lassen können. Beim Entwerfen einer Datenbank können Sie mithilfe des Datenbank-Designers Tabellen, Spalten, Schlüssel, Indizes, Beziehungen und Einschränkungen erstellen, bearbeiten oder löschen. Zur Darstellung einer Datenbank können Sie ein oder mehrere Diagramme erstellen, die die Tabellen, Spalten, Schlüssel oder Beziehungen innerhalb der Datenbank teilweise oder ganz anzeigen.  
  
![Datenbankdiagramm zur Illustration von Tabellenbeziehungen](../content/media/dv3w7c1.gif "dv3w7c1")  
  
Sie können für jede Datenbank beliebig viele Datenbankdiagramme erstellen, und jede Datenbanktabelle kann in einer beliebigen Anzahl von Diagrammen angezeigt werden. Daher können Sie verschiedene Diagramme erstellen, um unterschiedliche Bereiche der Datenbank darzustellen oder unterschiedliche Aspekte des Entwurfs hervorzuheben. Sie können z. B. ein umfangreiches Diagramm erstellen, in dem alle Tabellen und Spalten angezeigt werden, und ein kleineres Diagramm, in dem die Tabellen ohne ihre Spalten dargestellt sind.  
  
Jedes erstellte Diagramm wird in der zugehörigen Datenbank gespeichert.  
  
## Tabellen und Spalten in einem Datenbankdiagramm  
Innerhalb eines Datenbankdiagramms können Tabellen mit drei unterschiedlichen Merkmalen angezeigt werden: einer Titelleiste, einem Zeilenselektor und einer Reihe von Eigenschaftenspalten.  
  
**Titelleiste** der Titelleiste wird der Name der Tabelle  
  
Wenn Sie eine Tabelle geändert haben, und noch nicht, ein Sternchen gespeichert wurden (\*) am Ende des Tabellennamens, ungespeicherte Änderungen hinzuweisen. Informationen über das Speichern von geänderten Tabellen und Diagrammen finden Sie unter [Arbeiten mit Datenbankdiagrammen & #40; Visual Database Tools & #41;](../content/Work-with-Database-Diagrams--Visual-Database-Tools-.md)  
  
**Zeilenselektor** können Sie auf den Zeilenselektor, um eine Datenbankspalte in der Tabelle markieren klicken. Der Zeilenselektor zeigt ein Symbol in Form eines Schlüssels an, wenn sich die Spalte im Primärschlüssel der Tabelle befindet. Informationen zu Primärschlüsseln finden Sie unter [Arbeiten mit Schlüsseln (Visual Database Tools)](assetId:///31fbcc9f-2dc5-4bf9-aa50-ed70ec7b5bcd).  
  
**Eigenschaftenspalten** die Reihe von Eigenschaftenspalten wird nur in bestimmten Ansichten der Tabelle angezeigt. Sie können sich eine Tabelle in fünf verschiedenen Sichten anzeigen lassen, um dann die Größe und das Layout des betreffenden Diagramms verwalten zu können.  
  
Weitere Informationen über Tabellenansichten finden Sie unter [Anpassen der Menge der Informationen in Diagrammen & #40; Visual Database Tools & #41;](../content/Customize-the-Amount-of-Information-Displayed-in-Diagrams--Visual-Database-Tools-.md).  
  
## Beziehungen in einem Datenbankdiagramm  
Innerhalb eines Datenbankdiagramms können Eigenschaften mit drei unterschiedlichen Merkmalen angezeigt werden: Endpunkte, eine bestimmte Linienart und verknüpfte Tabellen.  
  
**Endpunkte** die Endpunkte der Linie geben an, ob die Beziehung eines\-\-oder\-auf\-viele. Besitzt eine Beziehung einen Schlüssel an einem Endpunkt und eine Abbildung\-acht am anderen, ist es eine\-\-n-Beziehung. Wenn eine Beziehung an jedem Endpunkt einen Schlüssel aufweist, ist es eine\-auf\-1-Beziehung.  
  
**Linienart** die Linie selbst (nicht die Endpunkte) gibt an, ob das Database Management System (DBMS) erzwingt die referenzielle Integrität für die Beziehung, wenn neue Daten, um die Fremdschlüssel hinzugefügt werden\-Schlüsseltabelle. Wenn Linie durchgezogenen erzwingt das DBMS referenzielle Integrität für die Beziehung, wenn Zeilen hinzugefügt oder werden, in der fremden geändert\-Schlüsseltabelle. Bei einer gepunkteten Linie, DBMS erzwingt keine referenzielle Integrität für die Beziehung, wenn Zeilen hinzugefügt oder werden, in der fremden geändert\-Schlüsseltabelle.  
  
**Verknüpfte Tabellen** die Beziehungslinie gibt an, dass ein Fremdschlüssel\--Beziehung zwischen zwei Tabellen vorhanden ist. Für eine\-\-n-Beziehung, die Fremdschlüssel\-Schlüssel ist die Tabelle in der Nähe der Zeile Zahl\-acht Symbol. Wenn beide Endpunkte der Linie mit derselben Tabelle verbunden sind, handelt es sich um eine reflexive Beziehung. Weitere Informationen finden Sie unter [Draw Reflexive Relationships & #40; Visual Database Tools & #41;](../content/Draw-Reflexive-Relationships--Visual-Database-Tools-.md).  
  
## In diesem Abschnitt  
[Verstehen des Besitzes von Datenbankdiagrammen & #40; Visual Database Tools & #41;](../content/Understand-Database-Diagram-Ownership--Visual-Database-Tools-.md)  
  
[Navigieren Sie im Datenbankdiagramm-Designer & #40. Visual Database Tools & #41;](../content/Navigate-in-Database-Diagram-Designer--Visual-Database-Tools-.md)  
  
[Richten Sie den Datenbankdiagramm-Designer & #40; Visual Database Tools & #41;](../content/Set-Up-Database-Diagram-Designer--Visual-Database-Tools-.md)  
  
[Aktualisieren von Datenbankdiagrammen aus älteren Versionen & #40; Visual Database Tools & #41;](../content/Upgrade-Database-Diagrams-from-Previous-Editions--Visual-Database-Tools-.md)  
  
[Öffnen Sie Datenbankdiagramm-Designer & #40; Visual Database Tools & #41;](../content/Open-Database-Diagram-Designer--Visual-Database-Tools-.md)  
  
## Siehe auch  
[Arbeiten Sie mit Datenbankdiagrammen & #40. Visual Database Tools & #41;](../content/Work-with-Database-Diagrams--Visual-Database-Tools-.md)  
[Arbeiten Sie mit Tabellen im Datenbankdiagramm & #40. Visual Database Tools & #41;](../content/Work-with-Tables-in-Database-Diagram--Visual-Database-Tools-.md)  
[Arbeiten Sie mit dem Diagrammlayout & #40. Visual Database Tools & #41;](../content/Work-with-Diagram-Layout--Visual-Database-Tools-.md)  
  
