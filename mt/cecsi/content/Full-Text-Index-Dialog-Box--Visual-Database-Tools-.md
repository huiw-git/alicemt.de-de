---
title: "Dialogfeld &quot;Volltextindex&quot; (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ef45b585-2567-4abe-b421-9fd0994e0146
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
# Dialogfeld &quot;Volltextindex&quot; (Visual Database Tools)
Dieses Dialogfeld ermöglicht Ihnen die Erstellung eine vollständigen\-Textindex für vollständige\-Textsuche Text\-Spalten in Datenbanktabellen. Eine vollständige\-Text auf einem regulären Index basiert, müssen Sie zuerst erstellen. Der reguläre Index muss auf einer einzelnen, nicht erstellt werden\-null-Spalte; es wird empfohlen, eine Spalte mit kleinen Werten anstatt einer Spalte mit großen Werten auswählen.  
  
> [!NOTE]  
> Erstellen Sie eine vollständige\-Textindex, erstellen Sie zuerst eine vollständige\-Volltextkatalog für die Datenbank eines externen Tools, z. B. [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] oder Enterprise Manager.  
  
> [!NOTE]  
> Vollständige\-Text Index-Funktion ist nicht verfügbar in jeder Edition von [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]. Eine Liste der Funktionen, die von den Editionen von unterstützt werden [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)], finden Sie unter [von den SQL Server 2012-Editionen unterstützte Funktionen](assetId:///5da61ff5-12b9-48e6-b3c8-0dacca1751c4).  
  
## Optionen  
**Aktiviert die vollständige\-Textindex**  
Listet vorhandene vollständige\-Textindizes. Wählen Sie einen Index, um seine Eigenschaften im Datenblatt rechts anzuzeigen. Wenn die Liste leer, keine vollständige ist\-Text Beziehungen für die Tabelle definiert wurden.  
  
**Hinzufügen**  
Erstellen Sie eine neue vollständige\-Textindex.  
  
**DELETE**  
Löschen Sie die vollständige\-in ausgewählten der **ausgewählten vollständige\-Textindex** Liste.  
  
**Kategorie Allgemein**  
Wenn die Kategorie erweitert ist, zeigt **Spalten** und **vollständige\-Text Katalogname**.  
  
**Spalten**  
Zeigt ein Komma\-getrennte Liste der Namen der vollständigen\-Text\-durchsuchbaren Spalten. Um die vollständige Liste anzuzeigen, klicken Sie auf die Schaltfläche mit den Auslassungspunkten (**...**) links neben dem Eigenschaftenfeld.  
  
**Vollständige\-Name des Volltextkatalogs**  
Zeigt den Namen des vollständigen\-Volltextkatalog auf der vollständigen\-Textindex gespeichert wird. Um den Index auf einen anderen Katalog zu speichern, klicken Sie auf den Katalognamen, und wählen Sie aus der Dropdownliste\--Liste.  
  
> [!NOTE]  
> Der Katalog muss zuerst erstellt in einem externen Tool, z. B. [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] oder Enterprise Manager.  
  
**Kategorie Identität**  
Wenn die Kategorie erweitert ist, zeigt das Namensfeld für diesen Index.  
  
**Name**  
Zeigt das System\-angegebenen Namen für diese vollständige\-Textindex.  
  
**Tabellenkategorie-Designer**  
Wenn die Kategorie erweitert ist, zeigt Eigenschaften, die vorgeben, wie der Index ausgeführt.  
  
**Active**  
Gibt an, ob Sie derzeit, eine vollständige ausführen können\-mit dieser vollständigen\-Textindex.  
  
**Ändern der Einstellung**  
Beschreibt den Status des Change tracking für diesen Index: manuell, automatisch oder aus.  
  
**Die Durchforstung ist abgeschlossen**  
Zeigt, ob die zuletzt gestartete Durchforstung abgeschlossen wurde. Wenn der Wert dieser Eigenschaft No ist, ist ein Crawl noch in Bearbeitung.  
  
**Enddatum und-Uhrzeit der aktuellen oder letzten Durchforstung**  
Zeigt das Datum und die Uhrzeit, zu der der letzten Durchforstung an.  
  
**Fehler im aktuellen oder letzten Durchforstung**  
Zeigt die Anzahl der Fehler im aktuellen oder letzten Durchforstung an.  
  
**Indexversion**  
Zeigt die Schemaversion der Tabelle zum Zeitpunkt des Crawls.  
  
**Zeilen In der aktuellen oder letzten Durchforstung**  
Zeigt die Anzahl der Zeilen in der aktuellen oder letzten Durchforstung aktualisiert.  
  
**Startdatum und-Uhrzeit der aktuellen oder letzten Durchforstung**  
Zeigt das Datum und die Uhrzeit, zu der aktuellen oder letzten Durchforstung gestartet.  
  
**Zeitstempel für nächste Durchforstung**  
Zeigt das Datum und die Uhrzeit, zu der die nächste Durchforstung gestartet werden kann.  
  
**Typ des aktuellen oder letzten Durchforstung**  
Zeigt den Typ des aktuellen oder letzten Durchforstung: vollständig, inkrementell, aktualisieren oder Automatische Propagierung.  
  
**Eindeutiger Indexname**  
Zeigt eine Liste aller mit dem Namen der Spalten in dieser Datenbank eindeutiger einzelne\-Spaltenindizes. Diese Spalten können verwendet werden, erstellen Sie eine vollständige\-Textindex.  
  
## Siehe auch  
[Verwenden des Volltextindizierungs-Assistenten](assetId:///3e9d9605-6525-4781-9168-fdaa06db3459)  
[CREATE FULLTEXT INDEX (Transact-SQL)](assetId:///8b80390f-5f8b-4e66-9bcc-cabd653c19fd)  
  
