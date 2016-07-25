---
title: "Ersetzen von Vorlagenparametern"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1234aa14-3464-4a3e-922a-5cfb8fb23627
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
# Ersetzen von Vorlagenparametern
Vorlagen enthalten Parameter, die durch Implementierung ersetzt werden können\-spezifische Werte jedes Mal die Vorlage verwendet wird. Nach dem Öffnen einer Vorlage in einem Code-Editor können Sie die Parameter durch für die Implementierung relevante Werte ersetzen.  
  
## Vorbereitungen  
Die **Werte für Vorlagenparameter angeben** Dialog ist ein Raster mit drei Spalten. Die **Parameter** und **Typ** Spalten werden gelesen,\-nur und kann nicht geändert werden. Überprüfen Sie den Inhalt der **Wert** Spalte, und ändern Sie ggf. die Standardwerte auf Werte für die Implementierung geeignete.  
  
Um dieses Dialogfeld verwenden zu können, benötigen Sie Parameter in Ihrem Skript in spitze Klammern eingeschlossen (`< >`) im Format `<`*Parameter\_Namen*`,` *Daten\_Typ*`,` *Standardwert\_Wert*`>`.  
  
## Ersetzen von Vorlagenparametern  
Nach dem Öffnen der Vorlage in einem Code-Editor-Fenster:  
  
1.  Klicken Sie im Menü **Abfrage** auf **Werte für Vorlagenparameter angeben**.  
  
2.  In der **Werte für Vorlagenparameter angeben** Klicken Sie im Dialogfeld die **Werte** Spalte enthält einen vorgeschlagenen Wert für jeden Parameter. Akzeptieren Sie den Wert, oder ersetzen Sie ihn durch einen neuen Wert.  
  
3.  Klicken Sie auf **OK** Schließen die **Vorlageparameter ersetzen** Dialogfeld ein, und ändern Sie das Skript im Abfrage-Editor.  
  
## Siehe auch  
[Vorlagen-Explorer](../content/Template-Explorer.md)  
[Öffnen einer Vorlage](../content/Open-a-Template.md)  
  
