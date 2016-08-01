---
title: "Verwenden des Abfrage- und Sicht-Designers bei internationalen Daten (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4b51c56f-f902-4e72-b919-e36127369b63
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
# Verwenden des Abfrage- und Sicht-Designers bei internationalen Daten (Visual Database Tools)
Sie können die [Abfrage- und Sicht-Designer](../content/Query-and-View-Designer-Tools--Visual-Database-Tools-.md) mit Daten in jeder Sprache und in einer beliebigen Version des Windows-Betriebssystems. In den folgenden Richtlinien werden die Unterschiede erläutert und Informationen zur Datenverwaltung in internationalen Anwendungen bereitgestellt.  
  
## Lokalisierte Informationen im Kriterien- und im SQL-Bereich  
Wenn Sie eine Abfrage im Kriterienbereich erstellen, können Sie die Informationen in dem Format eingeben, das den Ländereinstellungen von Windows auf dem Computer entspricht. Wenn Sie z. B. nach Daten suchen, können Sie die Daten in den Spalten Kriterien in dem für Sie gewohnten Format eingeben, wobei jedoch folgende Ausnahmen zu beachten sind:  
  
-   Lange Datenformate werden nicht unterstützt.  
  
-   Währungssymbole sollten im Kriterienbereich nicht eingegeben werden.  
  
-   Währungssymbole werden im Ergebnisbereich nicht angezeigt.  
  
    > [!NOTE]  
    > Sie können im Ergebnisbereich zwar das Währungssymbol eingeben, das den Ländereinstellungen von Windows auf dem Computer entspricht, das Symbol wird jedoch entfernt und im Ergebnisbereich nicht angezeigt.  
  
-   Unäres minus wird immer auf der linken Seite (z. B. \-1) unabhängig von den regionalen Einstellungen-Optionen.  
  
Dagegen müssen Daten und Schlüsselwörter im SQL-Bereich immer im ANSI-Format (U.S.) angegeben werden. Beispielsweise fügt der Abfrage- und Sicht-Designer beim Erstellen einer Abfrage alle SQL-Schlüsselwörter wie SELECT oder FROM im ANSI-Format ein. Achten Sie beim Hinzufügen von Elementen zu Anweisungen im SQL-Bereich darauf, für diese Elemente die ANSI-Standardform zu verwenden.  
  
Bei der Eingabe von Daten mithilfe von lokalen\-bestimmtes Format im Kriterienbereich, der Abfrage- und Ansicht-Designer automatisch übersetzt ANSI-Format im SQL-Bereich. Wenn die Ländereinstellungen des Computers z. B. auf die Option Deutsch (Standard) festgelegt sind, können Sie im Kriterienbereich ein Datum u. a. im Format "31.12.96" eingeben. Allerdings wird das Datum angezeigt, im SQL-Bereich im ANSI-Format als `{ ts '1996-12-31 00:00:00' }.` wenn Sie Daten direkt im SQL-Bereich eingeben, müssen Sie diese im ANSI-Format eingeben.  
  
## Sortierreihenfolge  
Die in Abfragen für Daten verwendete Sortierreihenfolge wird durch die verwendete Datenbank vorgegeben. Im Dialogfeld Ländereinstellungen von Windows ausgewählte Optionen haben keinen Einfluss auf die Sortierreihenfolge für Abfragen. Sie haben jedoch die Möglichkeit, für einzelne Abfragen eine spezielle Reihenfolge für die Zeilenausgabe anzufordern.  
  
## Verwenden doppelte\-Byte-Zeichen  
Sie können DBCS-Zeichen für Literalwerte und für Namen von Datenbankobjekten, wie Tabellen- und Sichtnamen oder Aliase, eingeben. Weiterhin sind DBCS-Zeichen in Parameternamen und Parametermarkierungszeichen zulässig. In SQL-Elementen, z. B. Funktionsnamen oder SQL-Schlüsselwörtern, dürfen DBCS-Zeichen jedoch nicht verwendet werden.  
  
## Siehe auch  
[Entwerfen von Abfragen und Sichten Gewusst-wie-Themen &#40; Visual Database Tools &#41;](../content/Design-Queries-and-Views-How-to-Topics--Visual-Database-Tools-.md)  
  
