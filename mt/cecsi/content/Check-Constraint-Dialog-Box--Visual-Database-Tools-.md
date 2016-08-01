---
title: "CHECK-Einschr&#228;nkung (Dialogfeld) (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ad0bbf7f-b0de-406a-bd0a-cb779816b101
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
# CHECK-Einschr&#228;nkung (Dialogfeld) (Visual Database Tools)
Dieses Dialogfeld wird angezeigt, wenn Sie mit der rechten Maustaste\-Klicken Sie auf ein tabellendefinitions-Datenblatt im Tabellen-Designer, und klicken Sie auf **Check-Einschränkungen**. Das Dialogfeld enthält eine Reihe von Eigenschaften für nicht\-unique-Einschränkungen auf die Tabellen in der Datenbank zugeordnet. Eigenschaften für unique-Einschränkungen werden in der **Indizes\/Schlüssel** (Dialogfeld).  
  
> [!NOTE]  
> Wenn die Tabelle für die Replikation veröffentlicht wird, stellen Sie schemaänderungen mit dem Transact\-SQL-Anweisung [ALTER TABLE](assetId:///f1745145-182d-4301-a334-18f799d361d1) oder SQL Server Management Objects (SMO). Wenn die Schemaänderungen mit dem Tabellen-Designer oder dem Datenbankdiagramm-Designer ausgeführt werden, wird versucht, die Tabelle zu entfernen und erneut zu erstellen. Da veröffentlichte Objekte nicht gelöscht werden können, schlägt die Schemaänderung fehl.  
  
## Optionen  
**Ausgewählte CHECK-Einschränkungen**  
Listet verfügbare CHECK-Einschränkungen auf. Um die Eigenschaften einer Einschränkung anzuzeigen, wählen Sie sie in der Liste aus.  
  
**Hinzufügen**  
Erstellt eine neue Einschränkung für die ausgewählte Datenbanktabelle und stellt den Standardnamen sowie weitere Werte für die Einschränkung zur Verfügung. Die Einschränkung wird erst dann gültig, wenn ein Ausdruck für die Einschränkung eingegeben wird.  
  
**Delete**  
Entfernt die ausgewählte Einschränkung aus der Tabelle. Verwenden Sie diese Schaltfläche zum Entfernen der Einschränkung, um das Hinzufügen einer CHECK-Einschränkung abzubrechen.  
  
**Kategorie Allgemein**  
Erweitern Sie zum Anzeigen der **Ausdruck** Eigenschaftenfeld.  
  
**Ausdruck**  
Zeigt den Ausdruck für die ausgewählte CHECK-Einschränkung an. Bei neuen Einschränkungen müssen Sie den Ausdruck vor dem Verlassen dieses Felds eingeben. Sie können auch vorhandene CHECK-Einschränkungen bearbeiten. Weitere Informationen finden Sie unter [Arbeiten mit Einschränkungen (Visual Database Tools)](assetId:///637098af-2567-48f8-90f4-b41df059833e).  
  
**Kategorie Identität**  
Erweitern Sie zum Anzeigen der Eigenschaften für **Namen** und **Beschreibung**.  
  
**Name**  
Zeigt den Namen der ausgewählten CHECK-Einschränkung an. Um den Namen dieser Einschränkung zu ändern, geben Sie den Text direkt in das Eigenschaftenfeld ein.  
  
**Beschreibung**  
Beschreibt die CHECK-Einschränkung. Sie können die Beschreibung bearbeiten, indem Sie in das Eigenschaftenfeld eingeben oder auf die Schaltfläche mit den Auslassungspunkten (**...**), die rechts neben dem Eigenschaftenfeld angezeigt wird, und bearbeiten Sie die Beschreibung in den **Description-Eigenschaft** im Dialogfeld.  
  
**Kategorie Tabellen-Designer**  
Erweitern Sie zum Anzeigen der Eigenschaften für **vorhandene Daten bei Erstellung oder Re\-aktivieren**, **für Inserts und Updates erzwingen**, und **Replikation erzwingen**.  
  
**Aktivieren Sie vorhandene Daten bei Erstellung oder Re\-Aktivieren**  
Angeben, ob alle vor\-vorhandenen Daten (Daten, die in der Tabelle vorhanden ist, bevor die Einschränkung erstellt wird) mit der Einschränkung überprüft.  
  
**Für INSERTs und UPDATEs erzwingen**  
Gibt an, ob die Einschränkung erzwungen wird, wenn die Daten in die Tabelle eingefügt oder in der Tabelle aktualisiert werden.  
  
**Für Replikation erzwingen**  
Gibt an, ob die Einschränkung erzwungen wird, wenn durch einen Replikations-Agent in der Tabelle ein INSERT oder ein UPDATE ausgeführt werden.  
  
## Siehe auch  
[Verwenden von Einschränkungen (Visual Database Tools)](assetId:///637098af-2567-48f8-90f4-b41df059833e)  
[Indizes - Schlüssel im Dialogfeld & #40. Visual Database Tools & #41;](../content/Indexes---Keys-Dialog-Box--Visual-Database-Tools-.md)  
  
