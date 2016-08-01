---
title: "Tabelleneigenschaften (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cc392987-1aab-45f5-b5af-a26be53409bf
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
# Tabelleneigenschaften (Visual Database Tools)
Diese Eigenschaften werden im Eigenschaftenfenster angezeigt, wenn Sie mit der rechten Maustaste in den Tabellen-Designer klicken und Eigenschaften auswählen. Wenn nicht anders beschrieben, können Sie diese Eigenschaften im Eigenschaftenfenster bearbeiten, wenn die Tabelle markiert ist.  
  
> [!NOTE]  
> Wenn die Tabelle für die Replikation veröffentlicht wird, stellen Sie schemaänderungen mit dem Transact\-SQL-Anweisung [ALTER TABLE](assetId:///f1745145-182d-4301-a334-18f799d361d1) oder SQL Server Management Objects (SMO). Wenn die Schemaänderungen mit dem Tabellen-Designer oder dem Datenbankdiagramm-Designer ausgeführt werden, wird versucht, die Tabelle zu entfernen und erneut zu erstellen. Da veröffentlichte Objekte nicht gelöscht werden können, schlägt die Schemaänderung fehl.  
  
## Anzeigen von Tabelleneigenschaften im Tabellen-Designer  
  
> [!NOTE]  
> Die in diesem Thema behandelten Eigenschaften sind nicht alphabetisch, sondern nach Kategorie angeordnet.  
  
**Kategorie Identität**  
Erweitert die Anzeige um Eigenschaften für **Namen**, **Beschreibung**, und **Schema**.  
  
**Name**  
Zeigt den Namen der Tabelle an. Bearbeiten Sie das Textfeld, um den Namen zu ändern.  
  
> [!CAUTION]  
> Wenn vorhandene, Ansichten, Benutzer fragt\-definierten Funktionen, gespeicherte Prozeduren oder Programme auf die Tabelle verweisen, die Namensänderung wird diese Objekte ungültig.  
  
**Datenbankname**  
Zeigt den Namen der Datenquelle der ausgewählten Tabelle an.  
  
**Beschreibung**  
Zeigt eine Beschreibung der ausgewählten Tabelle an. Um die ganze Beschreibung anzuzeigen oder zu bearbeiten, klicken Sie auf die Beschreibung, und klicken Sie dann auf die Auslassungspunkte **(...)** rechts neben der Eigenschaft.  
  
**Schema**  
Zeigt den Namen des Schemas an, zu dem die Tabelle gehört. (Gilt nur für Microsoft SQL Server.)  
  
**Servername**  
Zeigt den Namen des Servers für diese Datenquelle an.  
  
**Kategorie Tabellen-Designer**  
Erweitert die Anzeige um Eigenschaften für **Identitätsspalte**, **ist Indexable**, und **repliziert**.  
  
**Identitätsspalte**  
Zeigt die Spalte an, die als Identitätsspalte der Tabelle verwendet wird. Um die Identity-Spalte zu ändern, wählen Sie aus der Dropdownliste\--Liste. In der Liste werden nur Spalten mit einem numerischen Datentyp aufgeführt.  
  
**Ist indizierbar**  
Zeigt an, ob die Tabelle indiziert werden kann. Wenn die Tabelle nicht indiziert werden kann, liegt dies unter Umständen daran, dass Sie nicht der Besitzer der Tabelle sind, oder dass die Tabelle Spalten mit den Datentypen text, ntext oder image enthält.  
  
**Ist repliziert**  
Zeigt an, ob die Tabelle in einem anderen Speicherort repliziert wird.  
  
**Kategorie Reguläre Datenbereichsspezifikation**  
Erweitert die Anzeige um Eigenschaften für **(Datenbereichstyp)**, **Dateigruppe oder Partition Scheme**, und **Partitionsspaltenliste**.  
  
**(Datenbereichstyp)**  
Zeigt an, ob die Tabelle mit einem Dateigruppen- oder einem Partitionsschema gespeichert wird.  
  
**Schemaname der Dateigruppe oder Partition**  
Zeigt den Namen des Dateigruppen- oder Partitionsschemas an.  
  
**Partitionsspaltenliste**  
Ermöglicht den Zugriff auf die **Partitionsspaltenliste** Dialogfeld.  
  
**Zeilen-GUID-Spalte**  
Zeigt die Spalte an, die von Microsoft SQL Server als ROWGUID-Spalte der Tabelle verwendet wird. Um die ROWGUID-Spalte zu ändern, wählen Sie aus der Dropdownliste\--Liste. (Gilt nur für SQL Server 7.0 oder höher.)  
  
**Text\/Bild-Dateigruppe**  
Stellt eine Dropdownliste\--Liste, aus denen Sie die Dateigruppe für Spalten mit Datentypen Text oder Image auswählen können. Wenn die Tabelle mit einem Partitionsschema gespeichert wird, lassen Sie dieses Feld leer.  
  
## Siehe auch  
[Entwerfen von Tabellen &#40; Visual Database Tools &#41;](../content/Design-Tables--Visual-Database-Tools-.md)  
  
