---
title: "Indizes - Dialogfeld &quot;Schl&#252;ssel&quot; (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9e4060ba-80c3-468f-bccb-e12e99f672c2
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
# Indizes - Dialogfeld &quot;Schl&#252;ssel&quot; (Visual Database Tools)
Verwenden Sie dieses Dialogfeld zum Erstellen oder Ändern von Indizes, Primärschlüssel und eindeutige Schlüssel. Um auf dieses Dialogfeld zuzugreifen, öffnen Sie die Tabellendefinition für die Tabelle mit dem Index oder Schlüssel, die richtigen\-Klicken Sie auf das tabellendefinitions-Datenblatt, und klicken Sie dann auf **Indizes\/Schlüssel**.  
  
> [!NOTE]  
> Wenn die Tabelle für die Replikation veröffentlicht wird, stellen Sie schemaänderungen mit dem Transact\-SQL-Anweisung [ALTER TABLE](assetId:///f1745145-182d-4301-a334-18f799d361d1) oder SQL Server Management Objects (SMO). Wenn die Schemaänderungen mit dem Tabellen-Designer oder dem Datenbankdiagramm-Designer ausgeführt werden, wird versucht, die Tabelle zu entfernen und erneut zu erstellen. Da veröffentlichte Objekte nicht gelöscht werden können, schlägt die Schemaänderung fehl.  
  
## Optionen  
**Ausgewählten primären\/Eindeutiger Schlüssel oder Index**  
Listet die vorhandenen Primärschlüssel oder eindeutige Schlüssel und Indizes. Wählen Sie eine seiner Eigenschaften im Datenblatt rechts anzuzeigen. Falls die Liste leer ist, sind für die Tabelle Indizes definiert worden.  
  
**Hinzufügen**  
Erstellen Sie einen neuen primären oder eindeutigen Schlüssel oder Index.  
  
**DELETE**  
Löschen der ausgewählten Schlüssel oder Index in der **ausgewählten primären\/Eindeutiger Schlüssel oder Index** Liste.  
  
**Kategorie Allgemein**  
Wenn die Kategorie erweitert ist, werden die Eigenschaften **Spalten**, **ist eindeutig**, und **Typ**.  
  
**Spalten**  
Listet die ausgewählte Sortierreihenfolge für die Spalten im Schlüssel oder Index, und ermöglicht den Zugriff auf ein Dialogfeld, in dem die Sortierreihenfolgen definiert werden können. Um das Dialogfeld anzuzeigen, klicken Sie auf **Spalten** und klicken Sie dann auf die Schaltfläche mit den Auslassungspunkten (...) rechts neben dem Eigenschaftenfeld.  
  
**Ist eindeutig**  
Gibt an, ob in diesen Index oder Schlüssel eingegebene Daten eindeutig sein müssen. Dies ist für XML-Indizes nicht verfügbar.  
  
**Typ**  
Angeben, ob das Element, in ausgewählt der **ausgewählten primären\/Eindeutiger Schlüssel oder Index** Liste ist ein eindeutiger Schlüssel, einen Primärschlüssel oder einen Index. Primärschlüssel für dieses Feld ist finden Sie unter\-nur.  
  
**Kategorie Identität**  
Wenn die Kategorie erweitert ist, wird die Eigenschaftenfelder für **Namen** und **Beschreibung**.  
  
**Name**  
Zeigt den Namen des Schlüssels oder Index. Wenn ein neuer Index erstellt wird, erhält dieser einen Standardnamen, der auf der Tabelle im aktiven Fenster des Tabellen-Designers basiert. Sie können den Namen jederzeit ändern.  
  
**Beschreibung**  
Dient zum Beschreiben der Schlüssel oder Index. Um eine detailliertere Beschreibung zu schreiben, klicken Sie auf **Beschreibung** und klicken Sie dann auf die Schaltfläche mit den Auslassungspunkten (**...**), die rechts neben dem Eigenschaftenfeld angezeigt wird. Dadurch wird ein größerer Bereich verfügbar, in den Sie Text eingeben können.  
  
**Tabellenkategorie-Designer**  
Wenn die Kategorie erweitert ist, werden Informationen für **als Clustered erstellen**.  
  
**Als Clustered erstellen**  
Stellen Sie den Schlüssel oder Index zu gruppieren. Für eine Tabelle ist nur ein gruppierter Index zulässig. Daten in der Tabelle werden in der Reihenfolge des gruppierten Indexes gespeichert. Weitere Informationen finden Sie unter [gruppierte Indizes erstellen](assetId:///47148383-c2c7-4f08-a9e4-7016bf2d1d13) und [nicht gruppierte Indizes erstellen](assetId:///9402029a-1227-46c4-93aa-c2122eb1b943).  
  
**Datenbereichsspezifikation**  
Wenn die Kategorie erweitert ist, werden Informationen für **(Datenbereichstyp)**, **Dateigruppe oder Partition Scheme**, und **Partitionsspaltenliste**.  
  
**(Datenbereichstyp)**  
Gibt an, ob dieser Index oder Schlüssel zu einer Dateigruppe oder einem Partitionsschema gehört.  
  
**Der Dateigruppe oder Partition Schemaname**  
Zeigt den Namen der Dateigruppe oder des Partitionsschemas auf dem sie gespeichert ist.  
  
**Partitionsspaltenliste**  
Zeigt ein Komma\-getrennte Liste von Spalten, die in der Spalte Partitionsfunktion beteiligt sind. Nicht verfügbar, wenn die Dateigruppe ausgewählt wird, in der **(Datenbereichstyp)** Feld.  
  
**Füllspezifikation**  
Wenn die Kategorie erweitert ist, werden Informationen für **Füllfaktor** und **Pad_index**.  
  
**Füllfaktor**  
Gibt an, welcher Prozentsatz der Blattebene des Indexes\-Ebene von Seiten, die vom System gefüllt werden kann. Sobald eine Seite gefüllt ist, muss das System die Seiten zum Hinzufügen von neuer Daten, wodurch die Systemleistung beeinträchtigt teilen.  
  
-   Ein Wert von 100 bedeutet, dass die Seiten werden gefüllt sind. Dies erfordert den geringsten Speicherplatz. Diese Einstellung sollte verwendet werden, nur, wenn es keine Änderungen an den Daten, z. B. lesen werden\-nur Tabelle.  
  
-   Ein niedriger Wert bleibt leer auf den Datenseiten. Dies reduziert die Notwendigkeit von Datenseiten zu teilen, wenn Indizes größer, aber mehr Speicherplatz erforderlich.  
  
**Index mit Leerstellen auffüllen**  
Gibt an, ob Zwischenseiten in diesem Index der gleiche Prozentwert für leere Bereiche (Auffüllen) im angegebenen bereitgestellt werden **Füllfaktor** größer werdende.  
  
**Doppelte Schlüssel ignorieren**  
Geben Sie an, was geschieht, wenn eine Zeile, während eines Masseneinfügevorgangs eingefügt wird, dessen Schlüsselwert mit einem vorhandenen Schlüsselwert identisch ist. Wenn Sie auswählen:  
  
-   **Ja** [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Gibt eine Warnung aus, ignoriert die betreffende Zeile und versucht, die übrigen Zeilen einzufügen.  
  
-   **Nicht** [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] eine Fehlermeldung ausgegeben und ein Rollback für die gesamte Bulk Insert-Vorgang.  
  
**Eingeschlossene Spalten**  
Zeigt ein Komma\-getrennte Liste der Namen aller Spalten, die den Indexschlüssel bilden. Unterschlüsselspalten können nur für nicht gruppierte Indizes angegeben werden. Diese Eigenschaft ist für XML-Indizes ausgeblendet.  
  
**Ist deaktiviert**  
Gibt an, ob dieser Index deaktiviert ist. Dies ist ein Lesevorgang\-nur Eigenschaft. Diese Eigenschaft wird nur festgelegt, um **Ja** wenn der Index außerhalb von Visual Database Tools deaktiviert wurde.  
  
**Voll\-Text Key**  
Angeben, ob dieser Index eine vollständige\-Text Schlüssel. Weitere Informationen zu vollständigen\-Text-Schlüsseln finden Sie unter SQL Server-Onlinedokumentation. Diese Eigenschaft ist für XML-Indizes ausgeblendet.  
  
**Seitensperren sind zulässig**  
Angeben, ob die Seite\-Ebene Sperren für diesen Index zugelassen ist. Zulassen oder untersagen Seite\-Sperren auf Leistung der Datenbank auswirkt. Die empfohlene Einstellung lautet **Ja**.  
  
**Re\-Berechnen von Statistiken**  
Angeben, ob das zugrunde liegende [!INCLUDE[ssDE](../content/includes/ssDE_md.md)] neue Statistiken berechnet, wenn der Index erstellt wird. Re\-Berechnen von Statistiken wird die Erstellung der Indizes verlangsamt, aber wird sehr wahrscheinlich die abfrageleistung verbessern.  
  
**Zeilensperren sind zulässig**  
Angeben, ob die Zeile\-Ebene Sperren für diesen Index zugelassen ist. Zulassen oder untersagen Zeile\-Sperren auf Leistung der Datenbank auswirkt. Die empfohlene Einstellung lautet **Ja**.  
  
## Siehe auch  
[Arbeiten mit Einschränkungen (Visual Database Tools)](assetId:///637098af-2567-48f8-90f4-b41df059833e)  
[Arbeiten mit Schlüsseln (Visual Database Tools)](assetId:///31fbcc9f-2dc5-4bf9-aa50-ed70ec7b5bcd)  
  
