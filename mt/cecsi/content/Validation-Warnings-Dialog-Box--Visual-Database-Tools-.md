---
title: "G&#252;ltigkeitswarnungen (Dialogfeld) (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fc76e234-ec9c-4a19-a65b-cb558ec8268e
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
# G&#252;ltigkeitswarnungen (Dialogfeld) (Visual Database Tools)
Dieses Dialogfeld wird angezeigt, wenn Sie Änderungen zu speichern versuchen, die u. U. Schaden anrichten, oder wenn der Commit für die Datenbank vermutlich fehlschlägt. In diesem Dialogfeld werden die möglichen Nebeneffekte bzw. die Gründe für das Fehlschlagen des Commitvorgangs angegeben. Sie können dann entweder mit der Änderung fortfahren oder den Vorgang abbrechen.  
  
> [!NOTE]  
> Dieses Dialogfeld wird angezeigt, wenn Sie versuchen, vorgenommene Änderungen an die Datenbank zu übermitteln, oder wenn Sie ein Änderungsskript speichern.  
  
Das Dialogfeld kann aus folgenden Gründen angezeigt werden:  
  
-   Sie besitzen möglicherweise nicht die Datenbankberechtigungen zum Ausführen eines Commits für alle Änderungen.  
  
-   Die Änderungen würden falsch formatierte abgeleitete Spalten, Standardeinschränkungen oder CHECK-Einschränkungen zur Folge haben.  
  
-   Die Änderung des Datentyps für eine Spalte könnte zu Datenverlusten führen.  
  
-   Eine Änderung hätte einen Index von mehr als 900 Byte zur Folge.  
  
-   Eine Änderung würde eine Tabelle oder Spalte, die Teil eines Schemas ändern\-anzeigen oder Benutzer gebundenen\-benutzerdefinierten Funktion.  
  
-   Eine Änderung, ergibt die Remoteumgebung\-Erstellung einer Tabelle verfügt, die über einen oder mehrere Trigger verschlüsselt; der Trigger gelöscht werden.  
  
-   Die Änderungen ergibt besondere Einstellungen von ANSI\_NULL-Werte oder ANSI\_FÜLLZEICHEN oder sowohl für die Spalten innerhalb einer Tabelle.  
  
## Optionen  
**ja**  
Setzen Sie den Vorgang fort, und generieren Sie das Änderungsskript, oder übermitteln Sie die Änderungen an die Datenbank. Der Commitvorgang kann trotzdem noch fehlschlagen, wenn Sie nicht über die Berechtigungen zum Ändern der Datenbank verfügen, wenn die Änderungen bewirken, dass der Index größer als 900 Bytes wird, oder wenn die Änderungen eine falsch formatierte berechnete Spalte, Standardeinschränkungen oder CHECK-Einschränkungen zur Folge haben.  
  
**Nein**  
Brechen Sie den Speichervorgang ab.  
  
**Textdatei speichern**  
Anzeigen der **Speichern** Dialogfeld, in dem Sie einen Speicherort für eine Textdatei mit einer Liste der Warnungen angeben können.  
  
## Siehe auch  
[Entwerfen von Tabellen & #40; Visual Database Tools & #41;](../content/Design-Tables--Visual-Database-Tools-.md)  
[Entwerfen von Abfragen und Sichten Gewusst-wie-Themen & #40; Visual Database Tools & #41;](../content/Design-Queries-and-Views-How-to-Topics--Visual-Database-Tools-.md)  
  
