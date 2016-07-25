---
title: "Sortierreihenfolge (Dialogfeld) (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e4020f79-7abf-4839-b9b2-984ef7049817
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
# Sortierreihenfolge (Dialogfeld) (Visual Database Tools)
Mit diesem Dialogfeld können Sie eine Sortierreihenfolge für die Spalte angeben. Die Sortierreihenfolge einer Spalte wird bei jedem Vorgang verwendet, bei dem die Werte der Spalte mit einer anderen Spalte oder mit konstanten Werten verglichen werden. Gleichzeitig wird dadurch das Verhalten einiger Zeichenfolgenfunktionen beeinflusst, z. B. SUBSTRING und CHARINDEX. Eine vollständige Liste der Auswirkungen der Einstellung der Sortierreihenfolge einer Spalte finden Sie in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Dokumentation.  
  
Das Dialogfeld wird in den folgenden Fällen angezeigt:  
  
-   Wenn Sie auf der Registerkarte **Spalteneigenschaften** im Feld **Sortierung** einen ungültigen Sortierungsnamen eingeben.  
  
-   Sie klicken die **Sortierung** Feld der **Spalteneigenschaften** Registerkarte, und klicken Sie dann auf die Schaltfläche mit den Auslassungspunkten (**...**) rechts neben dem Feld.  
  
## Optionen  
**SQL-Sortierung**  
Wählen Sie eine der Sortierreihenfolgen definiert [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] aus der Dropdownliste\--Liste.  
  
**Windows-Sortierreihenfolge**  
Wählen Sie aus der Dropdownliste Windows definierten Sortierreihenfolgen\--Liste.  
  
**Binäre Sortierung**  
Verwenden Sie die Binärcodes der Zeichenwerte für Vergleiche. Wenn Sie diese Option auswählen, sind bestimmte Optionen der alphabetischen Vergleiche nicht verfügbar. Z. B. Fall\-insensitive Vergleiche sind nicht mehr verfügbar, da Groß- und Kleinbuchstaben unterschiedliche binäre Codierung aufweisen. Diese Option wird nur verwendet, wenn Sie **Windows-Sortierreihenfolge**ausgewählt haben.  
  
**Lexikalische Sortierung**  
Verwenden Sie alphabetische Vergleichsoptionen. Diese Option wird nur verwendet, wenn Sie **Windows-Sortierreihenfolge**ausgewählt haben. Zu den alphabetischen Vergleichsoptionen gehören folgende:  
  
-   **Groß-/Kleinschreibung beachten** Aktivieren Sie diese Option, wenn beim Vergleichen die Groß- und Kleinschreibung berücksichtigt werden soll.  
  
-   **Akzente berücksichtigen** Aktivieren Sie diese Option, wenn beim Vergleichen zwischen Buchstaben mit Akzent und Buchstaben ohne Akzent unterschieden werden soll. Wenn Sie diese Option aktivieren, werden beim Vergleichen außerdem gleiche Buchstaben mit unterschiedlichen Akzenten unterschieden.  
  
-   **Kana berücksichtigen** Aktivieren Sie diese Option, wenn beim Vergleichen Unterschiede zwischen Katakana- und Hiragana-Japanisch berücksichtigt werden sollen.  
  
-   **Breite berücksichtigen** Wählen Sie diese Option, wenn die Hälfte berücksichtigt werden sollen\-Breite und vollständige\-Breite Zeichen als ungleich.  
  
**Schaltfläche Standard wiederherstellen**  
Wenden Sie die Standardsortierreihenfolge für die Datenbank auf die Spalte an.  
  
## Siehe auch  
[Arbeiten Sie mit Spalten in Aggregatabfragen & #40. Visual Database Tools & #41;](../content/Work-with-Columns-in-Aggregate-Queries--Visual-Database-Tools-.md)  
  
