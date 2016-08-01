---
title: "Designer in Visual Database Tools"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bd0ca68e-6f69-42dd-bcb5-ce511673769c
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
# Designer in Visual Database Tools
Visual Database Tools kombiniert eine Reihe von Entwurfstools, die zur Bearbeitung von Datenquellen verwendet werden können. Sie können damit Abfragen erstellen, die Datenbankstruktur entwerfen oder ändern und Daten aktualisieren. Die Tools heißen Datenbankdiagramm-Designer, Tabellen-Designer und Abfrage- und Sicht-Designer.  
  
## Eigenschaftenfenster  
Das Eigenschaftenfenster ist keine Eigenheit von Visual Database Tools; an dieser Stelle können Sie jedoch verschiedene Änderungen vornehmen. Hier werden die Eigenschaften des aktuell ausgewählten Elements (z. B. eine Tabelle) angezeigt. Diese Eigenschaften (vom Namen der Eigenschaften bis zur Sortierung einer Spalte) können geändert werden. Einige Eigenschaften werden im Eigenschaftenfenster angezeigt, müssen jedoch mit einem anderen Tool geändert werden.  
  
## Datenbankdiagramm-Designer  
Im Datenbankdiagramm-Designer können Sie über ein Fenster Tabellen und Beziehungen einer Datenbank erstellen, bearbeiten und anzeigen.  
  
Um den Datenbankdiagramm-Designer anzuzeigen, öffnen Sie ein vorhandenes Diagramm oder rechts\-Klicken Sie auf den Knoten Datenbank im Objekt-Explorer, und wählen Sie **Neues Datenbankdiagramm** aus der Dropdownliste\--Menü.  
  
Sobald der Designer geöffnet ist, wird die **Datenbankdiagramm** Menü wird im Hauptmenü angezeigt. Dieses Menü bildet den Zugriffspunkt zu den speziellen Funktionen des Designers.  
  
> [!NOTE]  
> Dieser Designer ist mit Microsoft SQL Server-Datenbanken verwendbar.  
>   
> Diese Version von Visual Database Tools unterstützt Microsoft SQL Server Version 7 und ältere Versionen nicht.  
  
## Tabellen-Designer  
Der Tabellen-Designer ist ein visuelles Tool, mit dem Sie eine einzelne Tabelle einer Microsoft SQL Server-Datenbank, mit der Sie eine Verbindung hergestellt haben, entwerfen und anzeigen können.  
  
Der Tabellen-Designer umfasst zwei Bereiche. Im oberen Bereich wird ein Datenblatt angezeigt, wobei jede Zeile des Datenblatts eine Spalte in der Datenbank wiedergibt. Für jede Datenbankspalte zeigt das Raster die grundlegenden Attribute: Spaltenname, Datentyp und NULL\-Einstellung zulässig.  
  
Im unteren Bereich des Tabellen-Designers werden auf der Registerkarte Spalteneigenschaften weitere Attribute derjenigen Spalte angezeigt, die im oberen Bereich ausgewählt ist.  
  
Tabellen-Designer, Sie können auch mit der rechten Maustaste\-auf Dialogfelder zuzugreifen, über die Sie erstellen und Ändern von Beziehungen, Einschränkungen, Indizes und Schlüssel für die Tabelle, im Bereich Raster klicken.  
  
Tabellen-Designer anzuzeigen, öffnen eine vorhandene Tabelle oder rechts\-Klicken Sie auf die **Tabellen** Knoten im Objekt-Explorer, und wählen Sie **neue Tabelle hinzufügen** aus der Dropdownliste\--Menü.  
  
Sobald der Designer geöffnet ist, wird das Menü Tabellen-Designer im Hauptmenü angezeigt. Dieses Menü bildet den Zugriffspunkt zu den speziellen Funktionen des Designers.  
  
> [!NOTE]  
> Dieser Designer ist mit Microsoft SQL Server-Datenbanken verwendbar.  
>   
> Diese Version von Visual Database Tools unterstützt Microsoft SQL Server Version 7 und ältere Versionen nicht.  
  
## Abfrage- und Sicht-Designer  
Beim Abfrage- und Sicht-Designer handelt es sich eigentlich um zwei Tools, die auf sehr ähnliche Weise funktionieren. Einige der Hauptunterschiede sind:  
  
-   Sichten werden zusammen mit der Datenbank gespeichert, während Abfragen in einem Visual Studio-Datenbankprojekt gespeichert werden.  
  
-   Der Abfrage-Designer kann mit fast jeder beliebigen Datenquelle verwendet werden, während der Sicht-Designer nur SQL Server unterstützt.  
  
-   Mit dem Abfrage-Designer können Sie SELECT-, INSERT-, UPDATE- und DELETE DML-Anweisungen entwerfen; dagegen können Sichten nur SELECT-Anweisungen enthalten.  
  
### Sicht-Designer  
Mit dem Sicht-Designer können Sie eine vorhandene Sicht entwerfen und darstellen oder in einer Microsoft SQL Server-Datenbank, mit der eine Verbindung besteht, eine neue Sicht erstellen.  
  
Der Sicht-Designer umfasst vier Bereiche: den Diagrammbereich, den Kriterienbereich, den SQL-Bereich und den Ergebnisbereich. Ausführlichere Informationen zu jedem dieser Bereiche finden Sie unter [Abfrage und Sicht-Designer-Tools & #40; Visual Database Tools & #41;](../content/Query-and-View-Designer-Tools--Visual-Database-Tools-.md).  
  
Um Sicht-Designer anzuzeigen, öffnen Sie eine vorhandene Ansicht oder rechts\-Klicken Sie auf die **Ansicht** Knoten im Objekt-Explorer, und wählen Sie **neue Ansicht hinzufügen** aus der Dropdownliste\--Menü.  
  
Sobald der Designer geöffnet ist, wird die **-Abfrage-Designer** Menü wird im Hauptmenü angezeigt. Dieses Menü bildet den Zugriffspunkt zu den speziellen Funktionen des Designers.  
  
> [!NOTE]  
> Dieser Designer ist mit Microsoft SQL Server-Datenbanken verwendbar.  
>   
> Diese Version von Visual Database Tools unterstützt Microsoft SQL Server Version 7 und ältere Versionen nicht.  
  
## Siehe auch  
[Entwerfen von Datenbankdiagrammen & #40; Visual Database Tools & #41;](../content/Design-Database-Diagrams--Visual-Database-Tools-.md)  
[Entwerfen von Tabellen & #40; Visual Database Tools & #41;](../content/Design-Tables--Visual-Database-Tools-.md)  
[Entwerfen von Abfragen und Sichten Gewusst-wie-Themen & #40; Visual Database Tools & #41;](../content/Design-Queries-and-Views-How-to-Topics--Visual-Database-Tools-.md)  
  
