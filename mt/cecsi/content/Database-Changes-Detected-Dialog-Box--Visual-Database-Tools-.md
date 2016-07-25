---
title: "Es wurden &#196;nderungen in der Datenbank festgestellt (Dialogfeld) (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 91f13086-371f-46a2-9f46-804c1415f3ed
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
# Es wurden &#196;nderungen in der Datenbank festgestellt (Dialogfeld) (Visual Database Tools)
Dieses Dialogfeld wird angezeigt, wenn Sie ein Datenbankdiagramm oder ausgewählte Tabellen speichern möchten, jedoch einige der Datenbankobjekte, auf die sich der Speichervorgang auswirkt, in Bezug auf die Datenbank veraltet sind. Das Übernehmen der in diesem Dialogfeld angezeigten Änderungen führt dazu, dass die Datenbank entsprechend dem Diagramm aktualisiert wird und Änderungen anderer Benutzer überschrieben werden.  
  
> [!NOTE]  
> Die in einer Tabelle oder einem Datenbankdiagramm vorgenommenen Änderungen können zwar nicht rückgängig gemacht werden, doch werden sie erst dann in der Datenbank gespeichert, wenn Sie die Tabelle bzw. das Diagramm speichern. Sie können nicht gespeicherte Änderungen verwerfen, indem Sie **Nein** auswählen und alle geöffneten Diagramme schließen, ohne sie zu speichern.  
  
## Optionen  
**Warnung bei Unterschiederkennung**  
Geben Sie an, ob dieses Dialogfeld beim nächsten Versuch angezeigt wird, ein Datenbankdiagramm oder ausgewählte Tabellen zu speichern. Wenn diese Option aktiviert ist, wird das Dialogfeld weiterhin immer dann angezeigt, wenn Sie ein Diagramm oder eine Tabelle speichern, das bzw. die in Bezug auf die Datenbank veraltet ist. Ist die Option deaktiviert, wird das Dialogfeld nicht angezeigt. Dieses Kontrollkästchen ist standardmäßig aktiviert. Wenn Sie diese Option deaktivieren, können Sie sie im Dialogfeld **Optionen** erneut aktivieren.  
  
**ja**  
Aktualisieren Sie die Datenbank mit allen in der Liste aufgeführten Änderungen.  
  
**Nein**  
Brechen Sie den Speichervorgang ab.  
  
> [!NOTE]  
> So aktualisieren das Diagramm an der Datenbank entsprechen, ohne Speichern zu schließen, mit der rechten Maustaste\-Klicken Sie auf das Diagramm im Server-Explorer und klicken Sie auf aktualisieren, und öffnen Sie das Diagramm erneut.  
  
**Textdatei speichern**  
Anzeigen der **Speichern** Dialogfeld, dem Sie einen Speicherort für eine Textdatei mit einer Liste der datenbankänderungen angeben.  
  
## Siehe auch  
[Abgleichen eines Datenbankdiagramms mit einer geänderten Datenbank & #40; Visual Database Tools & #41;](../content/Reconcile-a-Database-Diagram-with-a-Modified-Database--Visual-Database-Tools-.md)  
[Mehrbenutzerumgebungen & #40; Visual Database Tools & #41;](../content/Multiuser-Environments--Visual-Database-Tools-.md)  
  
