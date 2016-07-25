---
title: "Abgleichen eines Datenbankdiagramms mit einer ge&#228;nderten Datenbank (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: eda8dea2-eedd-43a7-85aa-92bd97783b5f
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
# Abgleichen eines Datenbankdiagramms mit einer ge&#228;nderten Datenbank (Visual Database Tools)
Ein Datenbankdiagramm wird gespeichert, wenn die Datenbank mit dem Diagramm aktualisiert werden soll. Wenn die Datenbank jedoch von anderen Benutzern aktualisiert wurde, während Ihr Diagramm geöffnet war, können sich die Änderungen der anderen Benutzer auf Ihr Diagramm auswirken und umgekehrt.  
  
Beim Speichern des Diagramms wird die Datenbank mit dem Diagramm abgeglichen. Die Änderungen anderer Benutzer werden dabei überschrieben, sodass die Daten in der Datenbank mit Ihrem Diagramm übereinstimmen.  
  
### So aktualisieren Sie eine Datenbank anhand der Daten des Diagramms  
  
1.  Speichern Sie das Datenbankdiagramm.  
  
    Wenn Sie Ihr Diagramm noch nicht gespeichert haben, geben Sie einen Namen für das Diagramm in die **neue(s) Datenbankdiagramm speichern** Dialogfeld und wählen Sie **OK**.  
  
2.  Die **Speichern** im Dialogfeld die Tabellen, die beim Speichern des Diagramms betroffen sind. Wählen Sie **Ja** um den Vorgang fortzusetzen.  
  
3.  Die **Datenbank Änderungen erkannt** Dialogfeld listet die Objekte, die geändert wurden und geändert werden, damit Sie dem Diagramm übereinstimmt. Wählen Sie **Ja** Speichern Sie das Diagramm und die Liste der Änderungen zu übernehmen.  
  
    > [!NOTE]  
    > Wenn das Diagramm Tabellen und Spalten enthält, die in der Datenbank gelöscht wurden, werden beim Speichern des Diagramms nur die zugehörigen Definitionen in der Datenbank neu erstellt. Die Daten, die diese Objekte vor dem Löschen enthielten, können mit diesem Prozess nicht wiederhergestellt werden.  
  
### So aktualisieren Sie das Diagramm anhand der Daten einer geänderten Datenbank  
  
1.  Schließen Sie das Diagramm, ohne die Änderungen zu speichern.  
  
2.  Rechts\-Klicken Sie auf das Diagramm im Objekt-Explorer.  
  
3.  Klicken Sie im Kontextmenü auf **Aktualisieren**.  
  
4.  Öffnen Sie das Diagramm erneut.  
  
## Siehe auch  
[Arbeiten Sie mit Datenbankdiagrammen & #40. Visual Database Tools & #41;](../content/Work-with-Database-Diagrams--Visual-Database-Tools-.md)  
  
