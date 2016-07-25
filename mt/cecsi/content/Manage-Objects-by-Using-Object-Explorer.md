---
title: "Verwalten von Objekten mittels Objekt-Explorer"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e60367a7-3fdd-40b8-82bb-9e819d78de5a
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
# Verwalten von Objekten mittels Objekt-Explorer
Mit dem Objekt-Explorer können Sie Objekte, z. B. Datenbanken, Tabellen und gespeicherte Prozeduren, verwalten.  
  
## Anzeigen von Objekten im Objekt-Explorer  
Der Objekt-Explorer verwendet zum Gruppieren von Informationen in Ordnern eine Baumstruktur. Erweitern Sie Ordner, klicken Sie auf das Pluszeichen (+) (\+) oder doppelte\-Klicken Sie auf den Ordner. Erweitern Sie die Ordner, um detailliertere Informationen anzuzeigen. Rechts\-Klicken Sie auf Ordner oder Objekte zum Ausführen allgemeiner Aufgaben. Doppelte\-Klicken Sie auf Objekte, die am häufigsten verwendete Aufgabe ausführen.  
  
Wenn Sie zum ersten Mal einen Ordner erweitern, startet der Objekt-Explorer an den Server eine Abfrage nach Informationen zum Auffüllen der Struktur. Sie können andere Funktionen ausführen, während die Struktur aufgefüllt wird. Beim Objekt-Explorer die Struktur aufgefüllt wird, klicken Sie auf **Beenden** um den Prozess abzubrechen. Weitere Aktionen, z. B. Filtern der Liste, können nur für den Teil des Ordners ausgeführt werden, der aufgefüllt wurde, es sei denn, Sie aktualisieren den Ordner, um die Auffüllung erneut zu starten.  
  
Um Ressourcen zu sparen, wenn viele Objekte vorhanden sind, werden die Inhaltslisten der Ordner in der Struktur im Objekt-Explorer nicht automatisch aktualisiert. Zum Aktualisieren der Liste der Objekte in einem Ordner mit der rechten Maustaste\-auf den Ordner, und klicken Sie dann auf **Aktualisieren**.  
  
Der Objekt-Explorer kann maximal 65.536 Objekte anzeigen. Wenn die Anzahl der sichtbaren Objekte über 65.536 liegt, können Sie nicht durch weitere Objekte in der Strukturansicht des Objekt-Explorers einen Bildlauf durchführen. Zum Anzeigen weiterer Objekte im Objekt-Explorer schließen Sie nicht verwendete Knoten, oder wenden Sie Filter an, um die Anzahl der Objekte zu verringern.  
  
## Filtern der Objektliste im Objekt-Explorer  
Wenn ein Ordner eine große Anzahl an Objekten enthält, ist es möglicherweise schwierig, das gesuchte Objekt zu finden. In diesen Fällen können Sie mit der Filterfunktion des Objekt-Explorers die Liste verkleinern. Beispiel: Sie möchten in Listen mit Hunderten von Objekten nach einem bestimmten Datenbankbenutzer oder der zuletzt erstellten Tabelle suchen. Klicken Sie auf den Ordner, den Sie filtern möchten, und klicken Sie dann auf die Schaltfläche "Filter", öffnen die **Filtereinstellungen** im Dialogfeld. Sie können filtern Sie die Liste nach Namen, Erstellungsdatum und manchmal Schema und bieten zusätzliche Filteroperatoren wie **beginnt mit**, **enthält**, und **zwischen**.  
  
## Mit mehreren\-auswählen  
Im Objekt-Explorer kann nur jeweils ein Objekt ausgewählt werden. Um mehrere Elemente auszuwählen, drücken Sie die **F7** zum Öffnen der **Seite für die Details des Objekt-Explorer**. Die **Seite für die Details des Objekt-Explorer** unterstützt mehrere\-auswählen.  
  
## Registrieren eines Servers aus dem Objekt-Explorer  
Wenn eine Verbindung mit einem Server besteht, können Sie den Server auf einfache Weise zur späteren Verwendung registrieren. Mit der rechten Maustaste im Objekt-Explorer\-Klicken Sie auf den Namen des Servers, und klicken Sie dann auf **registrieren**. In der **Server registrieren** Dialogfeld geben in der servergruppenstruktur soll der Server befinden. In der **Servername** Feld, Sie können den Namen des Servers durch einen aussagekräftigeren Servernamen ersetzen. Sie könnten z. B. Server registrieren **APSQL02** durch einen aussagekräftigeren Namen wie "**Accounts Payable**".  
  
## Ausführen von Aktionen in Objekt-Explorer-Knoten  
Sie führen Aktionen bei Objekten aus, indem Sie direkt auf den Objekt-Explorer-Knoten klicken, der das Objekt darstellt. Jeder Typ des Objekts unterstützt einen eindeutigen Satz von rechten\-Klicken Sie auf Aktionen. Einige Arten von Aktionen mit der rechten Seite\-Menüs auf:  
  
### Öffnen eines verbundenen Abfrage-Editors  
Wenn der Objekt-Explorer mit einem Server verbunden ist, können Sie mit den Verbindungseinstellungen des Objekt-Explorers ein neues Fenster des Code-Editors öffnen. Um ein neues Fenster des Code-Editor zu öffnen, mit der rechten Maustaste\-Klicken Sie auf den Servernamen im Objekt-Explorer, und klicken Sie dann auf **neue Abfrage**. Um einen Code-Editor-Fenster, das mithilfe einer bestimmten Datenbank zu öffnen, mit der rechten Maustaste\-Klicken Sie auf den Datenbanknamen, und klicken Sie dann auf **neue Abfrage**. Beim Öffnen einer neuen Abfrage für einen Server mit Analysis Services können Sie DMX-, MDX- oder XMLA-Abfragen auswählen.  
  
### Starten von PowerShell  
Sie können eine PowerShell-Sitzung starten, indem rechts\-auf die meisten Ordner und Objekte in der Struktur des Objekt-Explorer klicken und auswählen **Starten von PowerShell**. Dies startet eine PowerShell-Sitzung mit der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] PowerShell-Unterstützung aktiviert der Pfad festgelegt, auf das Objekt Sie richtige\-im Objekt-Explorer geklickt haben. Sie können PowerShell-Befehle anschließend in einer interaktiven PowerShell-Umgebung eingeben. Weitere Informationen finden Sie unter [SQL Server PowerShell](assetId:///89b70725-bbe7-4ffe-a27d-2a40005a97e7).  
  
## Siehe auch  
[Objekt-Explorer](../content/Object-Explorer.md)  
[Öffnen und Konfigurieren des Objekt-Explorers](../content/Open-and-Configure-Object-Explorer.md)  
[Verbinden mit einer Instanz mit dem Objekt-Explorer](../content/Connect-to-an-Instance-From-Object-Explorer.md)  
[Detailbereich des Objekt-Explorers](../content/Object-Explorer-Details-Pane.md)  
[Benutzerdefinierte Berichte in Management Studio](../content/Custom-Reports-in-Management-Studio.md)  
  
