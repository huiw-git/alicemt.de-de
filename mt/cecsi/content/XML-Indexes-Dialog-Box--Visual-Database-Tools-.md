---
title: "XML-Indizes (Dialogfeld) (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: eef38310-4498-4ccc-bb77-5bbd1c7cc477
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
# XML-Indizes (Dialogfeld) (Visual Database Tools)
Verwenden der **XML-Indizes** Dialogfeld zum Erstellen von Indizes für Spalten vom Datentyp XML, die nicht indiziert werden mithilfe der **Index\/Schlüssel** (Dialogfeld). Jede XML-Spalte kann mehrere XML-Indizes aufweisen, aber der zuerst erstellte Index (der primäre Index) bildet die Basis für alle weiteren Indizes (die sekundären Indizes). Wenn Sie den primären XML-Index löschen, werden auch die sekundären Indizes gelöscht.  
  
## Optionen  
**Ausgewählter XML-Index**  
Listet vorhandene XML-Indizes auf. Wird ausgewählt, um die zugehörigen Eigenschaften im rechten Datenblatt anzuzeigen. Falls die Liste leer ist, sind für die Tabelle Indizes definiert worden.  
  
**Hinzufügen**  
Erstellen Sie einen neuen XML-Index.  
  
**Delete**  
XML-Index löschen im ausgewählten der **ausgewählten XML-Index** Liste. Beim Löschen des primären XML-Indexes wird eine Meldung ausgegeben, dass dadurch auch alle sekundären Indizes gelöscht werden, und Sie können entweder den Vorgang fortsetzen oder die Aktion abbrechen.  
  
**Kategorie Allgemein**  
Wenn die Kategorie erweitert ist, werden die Eigenschaftenfelder für **Spalten**, **ist Primary**, und **Typ**.  
  
**Spalten**  
Zeigt an, dass dieser Index in aufsteigender Reihenfolge sortiert ist.  
  
**Ist Primary**  
Gibt an, ob dies der primäre Index ist. Der erste für die Spalte erstellte XML-Index stellt die Basis für die anderen Indizes dar.  
  
**Primärverweisname**  
Zeigt für einen sekundären Index den Namen des primären Indexes an. Nur verfügbar, wenn es sich um einen sekundären Index handelt.  
  
**Sekundärer Typ**  
Zeigt den Typ des sekundären Indexes an. Nur verfügbar, wenn es sich um einen sekundären Index handelt.  
  
**Typ**  
Zeigt an, dass dies ein XML-Index ist.  
  
**Kategorie Identität**  
Wenn die Kategorie erweitert ist, zeigt der **Namen** und **Beschreibung** Eigenschaftenfelder.  
  
**Name**  
Zeigt den Namen des XML-Indexes an. Wenn ein neuer Index erstellt wird, erhält dieser einen Standardnamen, der auf der Tabelle im aktiven Fenster des Tabellen-Designers basiert. Sie können den Namen jederzeit ändern.  
  
**Beschreibung**  
Beschreibt den Index. Um eine detailliertere Beschreibung zu schreiben, klicken Sie auf **Beschreibung** und klicken Sie dann auf die Schaltfläche mit den Auslassungspunkten (**...**), die rechts neben dem Eigenschaftenfeld angezeigt wird. Dadurch wird ein größerer Bereich verfügbar, in den Sie Text eingeben können.  
  
**Kategorie Tabellen-Designer**  
Wenn die Kategorie erweitert ist, werden Informationen zu den Eigenschaften dieses XML-Indexes angezeigt.  
  
**Füllspezifikation**  
Wenn die Kategorie erweitert ist, werden Informationen für **Füllfaktor** und **Pad_index**.  
  
**Füllfaktor**  
Geben Sie an, zu welchem Prozentsatz die Indexseite vom System gefüllt werden kann. Sobald eine Seite gefüllt ist, müssen beim Hinzufügen neuer Daten die Seite vom System geteilt werden, wobei die Leistung beeinträchtigt wird.  
  
-   Ein Wert von 100 bedeutet, dass die Seiten gefüllt werden. Diese Einstellung erfordert den geringsten Aufwand an Speicherplatz, ist aber auch am wenigsten effektiv. Diese Einstellung sollte verwendet werden, nur, wenn es keine Änderungen an den Daten, z. B. lesen werden\-nur Tabelle.  
  
-   Durch einen niedrigeren Wert bleibt auf den Datenseiten ein größerer Bereich leer. Dadurch müssen die Datenseiten seltener geteilt werden, wenn Indizes größer werden. Dies erfordert allerdings mehr Speicherplatz. Diese Einstellung empfiehlt sich eher, wenn Änderungen an den Daten in der Tabelle vorgenommen werden.  
  
**Index mit Leerstellen auffüllen**  
Geben Sie Seiten in diesem Index der gleiche Prozentwert für leere Bereiche (Auffüllung), angegeben **Füllfaktor**.  
  
**Ist deaktiviert**  
Geben Sie an, ob der Index deaktiviert ist. Deaktivierte Indizes unterstützen weder Suchvorgänge noch werden sie aktualisiert, wenn der Tabelle neue Elemente hinzugefügt werden. Sie können die Leistung für Masseneinfügungen und -updates verbessern, indem Sie einen Index deaktivieren.  
  
**Seitensperren sind zulässig**  
Angeben, ob die Seite\-Ebene Sperren für diesen Index zugelassen ist. Zulassen oder untersagen Seite\-Sperren auf Leistung der Datenbank auswirkt.  
  
**Re\-Berechnen von Statistiken**  
Berechnen Sie beim Erstellen des Indexes neue Statistiken. Re\-Berechnen von Statistiken wird die Erstellung der Indizes verlangsamt, aber in der Regel verbessert die Leistung von Abfragen.  
  
**Zeilensperren sind zulässig**  
Angeben, ob die Zeile\-Ebene Sperren für diesen Index zugelassen ist. Zulassen oder untersagen Zeile\-Sperren auf Leistung der Datenbank auswirkt.  
  
## Siehe auch  
[Erstellen von XML-Indizes](assetId:///6ecac598-355d-4408-baf7-1b2e8d4cf7c1)  
  
