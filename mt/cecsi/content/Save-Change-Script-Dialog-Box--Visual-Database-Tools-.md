---
title: "&#196;nderungsskript speichern (Dialogfeld) (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fc9d1639-5efa-44fe-a04f-4d4d0def2833
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
# &#196;nderungsskript speichern (Dialogfeld) (Visual Database Tools)
Dieses Dialogfeld zeigt das [!INCLUDE[tsql](../content/includes/tsql_md.md)] -Skript für die Änderungen an, die Sie seit der letzten Speicherung der Tabelle vorgenommen haben. Außerdem können Sie in diesem Dialogfeld das Skript an einem auszuwählenden Speicherort als Textdatei speichern.  
  
Sie können auf dieses Dialogfeld nach dem Vornehmen nicht gespeicherter Änderungen einer Tabelle im Tabellen-Designer zugreifen. Klicken Sie im Menü **Tabellen-Designer** auf **Änderungsskript generieren**.  
  
> [!NOTE]  
> Änderungsskripts, die von Visual Database Tools zur Verfügung gestellt werden, enthalten keine Fehlerbehandlung. Annehmen, dass Datenbankobjekte nicht geändert wurden, da das Tool geöffnet wurde und die ändern\-Probleme treten daher nicht verknüpft. Vor dem Ausführen eines Änderungsskripts, sollten Sie den entsprechenden Fehler einschließen\--Anweisungen verarbeiten.  
  
## Optionen  
**Änderungsskript automatisch nach jedem Speichern erstellen**  
Wenn dieses Kontrollkästchen aktiviert, die **Änderungsskript speichern** Dialogfeld wird angezeigt, zu jedem beliebigen Zeitpunkt in einer Tabelle speichern.  
  
**ja**  
Rufen Sie die **Speichern** (Dialogfeld), in dem Sie den Speicherort für die Textdatei auswählen können.  
  
**Nein**  
Brechen Sie die Erstellung des Änderungsskripts ab.  
  
