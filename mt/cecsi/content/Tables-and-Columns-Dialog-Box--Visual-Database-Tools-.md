---
title: "Tabellen und Spalten (Dialogfeld) (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8cf27be1-e66d-4735-a428-9ab4b33af4f5
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
# Tabellen und Spalten (Dialogfeld) (Visual Database Tools)
In diesem Dialogfeld können Sie einen Primärschlüssel in einer Tabelle einem Fremdschlüssel in einer anderen Tabelle zuordnen. Sie können dieses Dialogfeld aufrufen, indem Sie im Menü **Tabellen-Designer** auf **Beziehungen**klicken. In der **Fremdschlüsselbeziehungen** im Dialogfeld klicken Sie auf die **Tabellen- und Spaltenspezifikation** Felds, und klicken Sie dann auf die Auslassungspunkte **(...)** rechts neben der Eigenschaft.  
  
> [!NOTE]  
> Wenn die Tabelle für die Replikation veröffentlicht wird, stellen Sie schemaänderungen mit dem Transact\-SQL-Anweisung [ALTER TABLE](assetId:///f1745145-182d-4301-a334-18f799d361d1) oder SQL Server Management Objects (SMO). Wenn die Schemaänderungen mit dem Tabellen-Designer oder dem Datenbankdiagramm-Designer ausgeführt werden, wird versucht, die Tabelle zu entfernen und erneut zu erstellen. Da veröffentlichte Objekte nicht gelöscht werden können, schlägt die Schemaänderung fehl.  
  
## Optionen  
**Beziehungsname**  
Zeigt den Namen der Beziehung an.  
  
**Primärschlüsseltabelle**  
Listet die in der Datenbank enthaltenen Tabellen auf. Wählen Sie die Tabelle, die auf dem primären\-key-Seite der Beziehung.  
  
**Fremdschlüsseltabelle**  
Zeigt die Tabelle an, die der Fremdschlüsselseite der Beziehung zugeordnet ist. Dabei handelt es sich um die aktuell im Tabellen-Designer ausgewählte Tabelle.  
  
**Datenblatt unter der Primärschlüsseltabelle**  
Listet die Spalten der Tabelle ausgewählt, die der **Primärschlüsseltabelle** Liste. Geben Sie die Spalten ein, die für den Primärschlüssel dieser Tabelle verwendet werden sollen.  
  
**Datenblatt unter der Fremdschlüsseltabelle**  
Listet die Spalten der Tabelle ausgewählt, die der **Fremdschlüsseltabelle** Liste. Geben Sie die Fremdschlüssel\-Schlüsselspalte des\-Schlüsseltabelle, die der Primärschlüsselspalte entspricht.  
  
> [!NOTE]  
> Die Spalten, die Sie für den Fremdschlüssel auswählen, müssen denselben Datentyp wie die entsprechenden Primärspalten aufweisen. Die Anzahl der Spalten muss in den jeweiligen Schlüsseln gleich sein. Wenn beispielsweise der Primärschlüssel der Tabelle auf der Primärseite der Beziehung aus zwei Spalten besteht, müssen Sie für jede Spalte eine entsprechende Spalte in der Tabelle für die Fremdschlüsselseite der Beziehung auswählen.  
  
## Siehe auch  
[Vorgehensweise: Erstellen von Beziehungen zwischen Tabellen (Visual Database Tools)](assetId:///867a54b8-5be4-46e6-9702-49ae6dabf67c)  
  
