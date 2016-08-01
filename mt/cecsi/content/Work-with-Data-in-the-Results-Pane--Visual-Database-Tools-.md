---
title: "Verwenden von Daten im Ergebnisbereich (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4f8a0080-91ef-4442-83ae-53be2f478c54
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
# Verwenden von Daten im Ergebnisbereich (Visual Database Tools)
Nach der Ausführung einer Abfrage oder Sicht werden die Ergebnisse im Ergebnisbereich angezeigt. Sie können anschließend mit diesen Ergebnissen arbeiten. Sie können z. B. Zeilen hinzufügen und löschen, Daten eingeben oder ändern und bequem durch umfangreiche Resultsets navigieren.  
  
Die folgenden Informationen können Ihnen helfen, Probleme zu vermeiden und mit den Resultsets effektiv zu arbeiten.  
  
## Zurückgeben der Resultsets  
Sie können Ergebnisse von einer Abfrage oder einer Sicht zurückgeben und auswählen, ob Sie nur den Ergebnisbereich oder alle Bereiche öffnen möchten. In jedem Fall wird die Abfrage oder die Sicht im Abfrage- und Sicht-Designer geöffnet. Der Unterschied besteht darin, dass im ersten Fall nur der Ergebnisbereich anzeigt wird und im anderen Fall alle Fenster anzeigt werden, die im Dialogfeld Optionen ausgewählt wurden. In der Standardeinstellung werden alle vier Bereiche (Ergebnisse, SQL, Diagramm und Kriterien) angezeigt.  
  
Weitere Informationen finden Sie unter [geöffnete Abfragen & #40; Visual Database Tools & #41;](../content/Open-Queries--Visual-Database-Tools-.md).  
  
Zum Ändern des Designs der Abfrage oder Ansicht, sodass es einen anderen Satz von Ergebnissen gibt oder Datensätze in einer anderen Reihenfolge zurückgegeben werden, finden Sie [Entwerfen von Abfragen und Sichten Gewusst-wie-Themen & #40; Visual Database Tools & #41;](../content/Design-Queries-and-Views-How-to-Topics--Visual-Database-Tools-.md).  
  
Sie können auch bestimmen, ob alle zurückgegeben oder in den Ergebnissen auf zwei Arten festlegen\-\-Abfrage während der Ausführung beenden, oder wählen Sie, wie viele Ergebnisse zurückgegeben werden, bevor die Abfrage ausgeführt wird.  
  
## Navigieren im Ergebnisbereich  
Verwenden Sie die Navigationsleiste am unteren Rand des Ergebnisbereichs, um schnell durch die Datensätze zu navigieren.  
  
Die Navigationsleiste ist mit Schaltflächen versehen, um zu den ersten und letzten Datensatz zu gehen, den nächsten und vorhergehenden Datensatz, und zu einem bestimmten Datensatz.  
  
Um zu einem bestimmten Datensatz zu gelangen, geben Sie die Zahl der Zeile in das Textfeld der Navigationsleiste ein, und drücken Sie die EINGABETASTE.  
  
Weitere Informationen zum Verwenden von Tastenkombinationen im Abfrage- und Ansicht-Designer finden Sie unter [Navigieren in der Abfrage und Sicht-Designer & #40; Visual Database Tools & #41;](../content/Navigate-in-the-Query-and-View-Designer--Visual-Database-Tools-.md).  
  
## Weitergeben der Änderungen an die Datenbank  
Im Ergebnisbereich wird ein Steuerelement für Vollständige Parallelität verwendet, sodass auf dem Datenblatt eine Kopie der Daten in der Datenbank statt einer kompletten Livesicht angezeigt wird. Dadurch wird nur dann ein Commit der Änderungen an die Datenbank ausgeführt, nachdem Sie den Cursor in einen Bereich außerhalb einer Zeile bewegt haben. Dadurch können mehrere Benutzer gleichzeitig mit der Datenbank arbeiten. Treten Konflikte auf (z. B. wenn ein anderer Benutzer dieselbe Zeile geändert hat, die bereits von Ihnen geändert wurde, und diese Änderung an die Datenbank weitergegeben hat, bevor Sie dies vornehmen konnten), erhalten Sie eine Meldung, in der der Konflikt mitgeteilt und entsprechende Lösungen angeboten werden.  
  
## Rückgängig machen von Änderungen mit ESC  
Sie können eine Änderung nur rückgängig machen, wenn noch kein Commit der Änderung an die Datenbank ausgeführt wurde. Die Daten werden nicht weitergegeben, wenn Sie den Cursor nicht in einen Bereich außerhalb des Datensatzes bewegt haben. Der Commit der Daten erfolgt auch nicht, wenn beim Fortbewegen des Cursors von einem Datensatz weg eine Fehlermeldung angezeigt wird, dass die Änderung nicht weitergegeben wird. Wenn die Änderung nicht weitergegeben wurde, können Sie die Änderung durch Drücken der ESC-TASTE rückgängig machen.  
  
Um alle Änderungen in einer Zeile rückgängig zu machen, wechseln Sie in eine Zelle in dieser Zeile, die Sie noch nicht bearbeitet haben, und drücken die ESC-TASTE.  
  
Um Änderungen in einer bestimmten Zelle rückgängig zu machen, die sie bearbeitet haben, gehen Sie zu der Zelle und drücken die ESC-TASTE.  
  
## Hinzufügen oder Löschen von Daten in der Datenbank  
Um zu sehen, wie Ihr Datenbankdesign funktioniert, müssen Sie möglicherweise Beispieldaten in die Datenbank eingeben. Diese Daten können Sie direkt in den Ergebnisbereich eingeben oder aus einem anderen Programm, z. B. Texteditor oder Excel, kopieren und in den Ergebnisbereich einfügen.  
  
Zusätzlich zum Kopieren von Zeilen in den Ergebnisbereich können Sie neue Datensätze hinzufügen oder bestehende Datensätze ändern oder löschen. Weitere Informationen finden Sie unter [Hinzufügen neuer Zeilen im Ergebnisbereich & #40; Visual Database Tools & #41;](../content/Add-New-Rows-in-the-Results-Pane--Visual-Database-Tools-.md), [Löschen von Zeilen im Ergebnisbereich & #40; Visual Database Tools & #41;](../content/Delete-Rows-in-the-Results-Pane--Visual-Database-Tools-.md), und [Bearbeiten von Zeilen im Ergebnisbereich & #40; Visual Database Tools & #41;](../content/Edit-Rows-in-the-Results-Pane--Visual-Database-Tools-.md).  
  
## Hinweise zum Arbeiten mit NULL-Werten und leeren Zellen  
Wenn Sie auf eine leere Zeile, um einen neuen Datensatz hinzufügen klicken, wird der Anfangswert aller Spalten *NULL*. Wenn eine Spalte NULL-Werte zulässt, können Sie diese unverändert belassen.  
  
Wenn Sie einen anderen ersetzen möchten\-null-Wert mit Null ist, geben Sie NULL in Großbuchstaben. Im Ergebnisbereich wird das Wort kursiv formatiert angezeigt, um darauf hinzuweisen, dass es nicht als Zeichenfolge, sondern als NULL-Wert erkannt werden soll.  
  
Geben Sie die Buchstaben ohne Anführungszeichen ein, um die Zeichenfolge "null" einzugeben. Solange mindestens einer der Buchstaben kleingeschrieben ist, wird der Wert als Zeichenfolge statt als NULL-Wert behandelt.  
  
Werte für Spalten mit einem binären Datentyp verfügen standardmäßig über NULL Werte. Diese Werte können im Ergebnisbereich nicht geändert werden.  
  
Um einen Leerraum anstelle von NULL einzugeben, löschen Sie den vorhandenen Text und bewegen den Cursor von der Zelle weg.  
  
## Überprüfen von Daten  
Der Abfrage- und Sicht-Designer kann einige Arten von Daten im Vergleich zu den Spalteneigenschaften überprüfen. Wenn Sie z. B. "abc" in eine Spalte mit einem float-Datentyp eingeben, erhalten Sie eine Fehlermeldung, und die Änderung wird nicht an die Datenbank übermittelt.  
  
Finden Sie unter den Datentyp einer Spalte, wenn Sie im Bereich Ergebnisse sind am schnellsten ist, öffnen Sie den Diagrammbereich und zeigen Sie auf den Namen der Spalte in der Tabelle oder\-bewertet Objekt.  
  
> [!NOTE]  
> Die maximale Länge, die im Ergebnisbereich für einen Textdatentyp angezeigt werden kann, beträgt 2,147,483,647.  
  
## Synchronhalten des Resultsets mit der Abfragedefinition  
Während Sie mit den Ergebnissen einer Abfrage oder Sicht arbeiten, ist es möglich, dass die Datensätze im Ergebnisbereich nicht mehr mit der Abfragedefinition synchron sind. Wenn Sie beispielsweise eine Abfrage für vier von fünf Spalten einer Tabelle ausgeführt haben und dann den Diagrammbereich verwendet haben, um die fünfte Spalte zur Abfragedefinition hinzuzufügen, werden die Daten der fünften Spalte nicht automatisch dem Ergebnisbereich hinzugefügt. Führen Sie die Abfrage erneut aus, damit der Ergebnisbereich die neue Abfragedefinition wiedergibt.  
  
Sie können feststellen, ob in diesem Fall\-\-ein Warnsymbol und der Text "Abfrage geändert" wird, in der unteren angezeigt\-in der oberen rechten Ecke des Ergebnisbereichs angezeigt, und das Symbol wiederholt\-linken Ecke des Bereichs.  
  
## Abstimmen von Änderungen, die von mehreren Benutzern vorgenommen wurden  
Während Sie mit den Ergebnissen einer Abfrage oder Sicht arbeiten, ist es möglich, dass die Datensätze von einem anderen Benutzer geändert werden, der auch mit der Datenbank arbeitet.  
  
Wenn dies geschieht, erhalten Sie eine Meldung, sobald Sie den Cursor aus der Zelle heraus bewegen, in der der Konflikt auftritt. Sie können anschließend die Änderung des anderen Benutzers überschreiben, Ihren Ergebnisbereich mit der Änderung des anderen Benutzers aktualisieren oder weiterhin Ihren Ergebnisbereich bearbeiten, ohne die Unterschiede abzustimmen. Wenn Sie die Unterschiede nicht abstimmen möchten, wird für die Änderungen kein Commit an die Datenbank ausgeführt.  
  
## Einschränkungen im Ergebnisbereich  
  
### Elemente, die nicht aktualisiert werden können  
Diese Tipps können Ihnen helfen, mit Daten im Ergebnisbereich erfolgreich zu arbeiten.  
  
-   Abfragen, die Spalten von mehr als einer Tabelle oder Sicht einschließen, können nicht aktualisiert werden.  
  
-   Sichten können nur aktualisiert werden, wenn die Datenbankeinschränkungen dies zulassen.  
  
-   Von einer gespeicherten Prozedur zurückgegebene Ergebnisse können nicht aktualisiert werden.  
  
-   Abfragen oder Sichten, die die Klauseln GROUP BY, DISTINCT oder TO XML verwenden, sind nicht aktualisierbar.  
  
-   Zurückgegebene Tabelle Ergebnisse\-Tabellenwertfunktionen können nur in einigen Fällen aktualisiert werden.  
  
-   Daten in Spalten, die sich aus einem Ausdruck in der Abfrage ergeben.  
  
-   Daten, die nicht erfolgreich vom Anbieter übersetzt wurden.  
  
### Elemente, die nicht vollständig dargestellt werden können  
Das, was die Datenbank an den Ergebnisbereich zurückgibt, wird größtenteils vom Anbieter der von Ihnen verwendeten Datenquelle verwaltet. Der Ergebnisbereich kann nicht immer die Daten von allen Datenbankmanagementsystemen übersetzen. Hier werden einige Fälle aufgeführt, bei denen dies so ist.  
  
-   Binäre Datentypen sind für Benutzer, die im Ergebnisbereich arbeiten, häufig nicht sinnvoll, und für den Download dieser Datentypen kann sehr viel Zeit benötigt werden. Damit sie dargestellt werden *<Binary data>* oder *Null*.  
  
-   Genauigkeit und Skalierung können nicht immer bewahrt werden. Der Ergebnisbereich unterstützt beispielsweise eine Genauigkeit von 27. Wenn Daten von einem Datentyp mit höherer Genauigkeit, die Daten abgeschnitten oder dargestellt werden kann *<Unable to read data>*.  
  
## Siehe auch  
[Durchführen Sie grundlegende Operationen mit Abfragen & #40; Visual Database Tools & #41;](../content/Perform-Basic-Operations-with-Queries--Visual-Database-Tools-.md)  
[Geben Sie Suchkriterien & #40. Visual Database Tools & #41;](../content/Specify-Search-Criteria--Visual-Database-Tools-.md)  
  
