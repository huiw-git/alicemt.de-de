---
title: "Spalten f&#252;r Volltextindex (Dialogfeld) (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a6f41c5c-d950-4d64-9e42-d062925917b6
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
# Spalten f&#252;r Volltextindex (Dialogfeld) (Visual Database Tools)
Dieses Dialogfeld enthält die Spalten in der vollständigen\-Textindex für die Tabelle im Tabellen-Designer geöffnet. Um auf dieses Dialogfeld zuzugreifen, mit der rechten Maustaste\-Klicken Sie auf die Tabelle im Tabellen-Designer, wählen Sie **vollständige\-Textindex**, und in der **vollständige\-Textindex** Dialogfeld klicken Sie auf den Index mit Spalten, die Sie verwenden möchten, anzeigen oder bearbeiten, klicken Sie auf die **Spalten** im Raster auf der rechten Seite ein, und klicken Sie auf die Auslassungspunkte (**...**).  
  
## Optionen  
**Column**  
Zeigt die Namen der Spalten in der vollständigen\-Textindex. Um eine Spalte hinzuzufügen, klicken Sie auf die erste leere Zelle, und wählen Sie eine Spalte aus der Dropdownliste\--Liste. Nur Spalten mit Text\-basieren oder Image-Datentypen zugegriffen werden.  
  
**Datentyp**  
Zeigt den Datentyp für jede Spalte an. Dies ist ein Lesevorgang\-nur Eigenschaft. Um einen Datentyp zu ändern, öffnen Sie die Tabelle im Tabellen-Designer, klicken Sie auf die Spalte, und bearbeiten Sie den Datentyp in der **Spalteneigenschaften** Registerkarte.  
  
**Nach Spalte eingegeben**  
Gilt nur für Spalten mit dem Datentyp **Bild**. Stellt eine Dropdownliste\--Liste, die aus dem Sie, welche der anderen Spalten wählen können darstellen den Datentyp dieser Spalte. Wenn diese Spalte nicht die **Bild** werden Datentyp der Wert None.  
  
Spalten mit dem Datentyp **Image** kann Microsoft Office-Dateien (DOC-, XLS- und PPT-Dateien) enthalten, Textdateien (TXT-Dateien) und HTML-Dateien (HTM-Dateien) und wenn den Datentyp dieser Spalte auf Image ermöglicht die vollständige\-Text suchen, um den Inhalt der Dateien zu suchen.  
  
**Sprache**  
Listet verfügbare Sprachen auf. Wählen Sie die Sprache aus der Dropdownliste\--Liste für die Spaltendaten geeignet. Z. B. Wenn Sie ein englisches Betriebssystem verwenden, aber Sie möchten eine Spalte indizieren, die deutschen Text enthält, wählen Sie die Option Deutsch aus der Dropdownliste\--Liste, um die Leistung des Index zu verbessern.  
  
**Statistische Semantik**  
Wählen Sie aus, ob die semantische Indizierung für die ausgewählte Spalte aktiviert werden soll. Weitere Informationen finden Sie unter [semantische Suche Platzhalter](assetId:///cd8faa9d-07db-420d-93f4-a2ea7c974b97).  
  
Wenn Sie eine **Sprache** vor der Option **Statistische Semantik**auswählen und die ausgewählte Sprache über kein zugeordnetes semantisches Sprachmodell verfügt, ist das Kontrollkästchen **Statistische Semantik** deaktiviert. Bei Auswahl von **statistische Semantik** vor dem Auswählen einer **Sprache**, in der Dropdownliste verfügbaren Sprachen\-unten Kombinationsfeld Feld werden nur für das semantische Sprachmodell unterstützt vorhanden ist.  
  
## Siehe auch  
[Dialogfeld Volltextindex & #40; Visual Database Tools & #41;](../content/Full-Text-Index-Dialog-Box--Visual-Database-Tools-.md)  
  
