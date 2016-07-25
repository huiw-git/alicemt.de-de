---
title: "Verwalten von Dateien mit Codierung"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 919544c9-59f0-4cc6-bb2a-f1ad671eb74b
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
# Verwalten von Dateien mit Codierung
Um die Anzeige von Code in einer bestimmten Sprache und auf einer bestimmten Plattform zu vereinfachen, können Sie einer Datei eine bestimmte Zeichencodierung zuordnen.  
  
## Öffnen von Dateien  
Sie können zum Bearbeiten der Datei einen Editor Ihrer Wahl verwenden.  
  
#### So öffnen Sie eine Datei mit einem bestimmten Editor  
  
1.  Auf der **Datei** auf **Öffnen**, und klicken Sie dann auf **Datei**.  
  
2.  In der **Datei öffnen** Dialogfeld Wählen Sie den Dateinamen ein.  
  
3.  Klicken Sie auf den Pfeil neben der **Öffnen** und klicken Sie dann auf**Öffnen mit** aus dem angezeigten Menü aus.  
  
4.  In der **Wählen Sie ein Programm zum Öffnen** Liste, wählen Sie einen Editor, und klicken Sie dann auf **Öffnen**. Wählen Sie zum Öffnen einer Datei mit einer bestimmten Codierung einen Editor mit Codierungsunterstützung aus, z. B. den SQL-Abfrage-Editor mit Codierung oder den XML-Editor mit Codierung.  
  
## Speichern von Dateien  
Sie können Code auch mit Unicode-Codierung oder einer anderen Codepage speichern, um verschiedene Sprachen zu unterstützen, z. B. Westeuropäisch oder Osteuropäisch. Sie können eine bestimmte zeichencodierung zuordnen mit einer Datei, um die Anzeige von Code in dieser Sprache sowie eine Linie zu erleichtern\-endet Typ, um ein bestimmtes Betriebssystem unterstützen. Darüber hinaus können einige Zeichen in Dateinamen nur gespeichert werden, wenn sie mit Unicode-Codierung gespeichert werden.  
  
#### So speichern Sie eine Datei mit einer anderen Codierung oder einem anderen Zeilenendentyp  
  
1.  Auf der **Datei** Menü klicken Sie auf **Speichern <filename> als**.  
  
2.  In der **Speichern unter** Dialogfeld erweitern Sie die **Speichern** und klicken Sie dann auf **mit Codierung speichern**.  
  
3.  In der **Erweiterte Speicheroptionen** Dialogfeld Wählen Sie die gewünschte Codierung aus dem **Codierung** Liste.  
  
4.  Aus der **Zeilenenden**Wählen Sie den Typ des gewünschten zeilenendentyp.  
  
    > [!NOTE]  
    > Wenn Sie die Datei mit Unicode-Codierung speichern, muss die Datei in [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] Visual SourceSafe als Binärdatei eingecheckt werden, da Visual SourceSafe keine Unterstützung für das Zusammenführen, Vergleichen und Anzeigen von Unterschieden zwischen Dateien bietet, die mit Unicode-Codierung gespeichert werden.  
  
Wenn Sie mit Visual SourceSafe Dateien mit ANSI-, UTF8- oder Unicode-Codierung speichern, beachten Sie die folgenden Einschränkungen:  
  
-   Bei ANSI-Dateien sind nur Zeichen zulässig, die in der aktuellen Codepage unterstützt werden, wodurch die internationale Verwendung eingeschränkt ist.  
  
-   Bei Unicode-Dateien können die Funktionen zum freigegebenen Auschecken, Überprüfen von Unterschieden oder Zusammenführen nicht verwendet werden, da sie als Binärdateien behandelt werden. Sie können dieses Format in internationalen Dateien verwenden.  
  
-   UTF8-Dateien funktionieren nicht sicher mit Visual SourceSafe, da Änderungen, die für Editoren von UTF8-Dateien Probleme verursachen, beim Einchecken, Auschecken, Überprüfen von Unterschieden und Zusammenführen vorgenommen werden.  
  
## Siehe auch  
[Dateien zum Verwalten von Projektmappen und Projekten](../content/Files-That-Manage-Solutions-and-Projects.md)  
[Zuordnen von Dateierweiterungen zu einem Code-Editor](assetId:///193630f4-93de-4950-8f36-68702531f925)  
  
