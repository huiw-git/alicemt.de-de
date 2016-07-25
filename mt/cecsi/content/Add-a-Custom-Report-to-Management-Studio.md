---
title: "Hinzuf&#252;gen eines benutzerdefinierten Berichts zu Management Studio"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3cf8d726-0a90-4f80-98d0-352a2a59be0f
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
# Hinzuf&#252;gen eines benutzerdefinierten Berichts zu Management Studio
In diesem Thema wird beschrieben, wie ein einfacher, als RDL-Datei gespeicherter [!INCLUDE[ssRSnoversion](../content/includes/ssRSnoversion_md.md)]-Bericht erstellt und anschließend [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] diese RDL-Datei als benutzerdefinierter Bericht hinzugefügt wird. [!INCLUDE[ssRS](../content/includes/ssRS_md.md)] kann eine Vielzahl komplexer Berichte erstellt werden. Zum Erstellen eines Berichts mithilfe dieses Themas muss auf dem Computer [!INCLUDE[ssBIDevStudioFull](../content/includes/ssBIDevStudioFull_md.md)] installiert sein. Sie müssen [!INCLUDE[ssRS](../content/includes/ssRS_md.md)] nicht auf einem Computer mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] installieren, um einen benutzerdefinierten Bericht mithilfe von [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)] auszuführen.  
  
[Beispielberichte](http://go.microsoft.com/fwlink/?LinkId=81792), einschließlich der durch erstellten Standardberichte [!INCLUDE[msCoName](../content/includes/msCoName_md.md)], zum Download zur Verfügung. Diese Beispiele können mithilfe von [!INCLUDE[ssBIDevStudioFull](../content/includes/ssBIDevStudioFull_md.md)] geändert werden.  
  
### So erstellen Sie einen als RDL-Datei gespeicherten, einfachen Bericht  
  
1.  Klicken Sie auf **Start**, zeigen Sie auf **Programme**, zeigen Sie auf **Microsoft SQL Server**, und klicken Sie dann auf **SQL Server Data Tools**.  
  
2.  Zeigen Sie im Menü **Datei** auf **Neu**, und klicken Sie dann auf **Projekt**.  
  
3.  Klicken Sie in der Liste **Projekttypen** auf **Business Intelligence-Projekte**.  
  
4.  In der **Vorlagen** auf **Berichtsserverprojekt-Assistent**.  
  
5.  In **Namen**, Typ **ConnectionsReport**, und klicken Sie dann auf **OK**.  
  
6.  Auf der **Berichts-Assistenten** Seite "Einführung", klicken Sie auf **Weiter**.  
  
7.  Auf der **Wählen Sie die Datenquelle** Seite, und geben Sie im Feld Name einen Namen für die Verbindung mit Ihrem [!INCLUDE[ssDE](../content/includes/ssDE_md.md)], und klicken Sie dann auf **Bearbeiten**.  
  
8.  In der **Verbindungseigenschaften** Dialogfeld die **Servername** Geben Sie den Namen Ihrer Instanz von der [!INCLUDE[ssDE](../content/includes/ssDE_md.md)].  
  
9. In der **einen Datenbanknamen eingeben oder auswählen** Geben Sie den Namen einer beliebigen Datenbank auf Ihrem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)], wie z. B. [!INCLUDE[ssSampleDBobject](../content/includes/ssSampleDBobject_md.md)], und klicken Sie dann auf **OK**.  
  
10. Auf der **Wählen Sie die Datenquelle** auf **Weiter**.  
  
11. Auf der **Abfrage entwerfen** auf der Seite der **Abfragezeichenfolge** Geben die folgenden [!INCLUDE[tsql](../content/includes/tsql_md.md)] -Anweisung, die der aktuellen Verbindungen mit aufgelistet Ihrer [!INCLUDE[ssDE](../content/includes/ssDE_md.md)], und klicken Sie dann auf **Weiter**. Im Feld "Abfragezeichenfolge" des Berichts-Assistenten können keine Berichtsparameter eingegeben werden. Komplexere benutzerdefinierte Berichte müssen manuell erstellt werden.  
  
    **SELECT-Sitzung\_-Id, net\_transport von zu\_Exec\_Verbindungen;**  
  
12. Auf der **Auswählen des Berichtstyps** Seite **Tabellarisch**, und klicken Sie dann auf **Fertig stellen**.  
  
13. Auf der **der Assistent** auf der Seite der **Berichtsname** Geben **ConnectionsReport**, und klicken Sie dann auf **Fertig stellen** Erstellen und speichern Sie den Bericht.  
  
14. Schließen Sie [!INCLUDE[ssBIDevStudio](../content/includes/ssBIDevStudio_md.md)].  
  
15. Copy **ConnectionsReport.rdl** in einen Ordner, die Sie auf dem Datenbankserver für benutzerdefinierte Berichte erstellt.  
  
### So fügen Sie Management Studio einen Bericht hinzu  
  
-   In [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)], mit der rechten Maustaste\-Klicken Sie auf einen Knoten im Objekt-Explorer, zeigen Sie auf **Berichte**, klicken Sie auf **benutzerdefinierte Berichte**. In der **Datei öffnen** Dialogfeld Suchen den Ordner benutzerdefinierte Berichte und wählen Sie die **ConnectionsReport.rdl** Datei, und klicken Sie dann auf **Öffnen**.  
  
    Wenn ein neuer benutzerdefinierter Bericht erstmalig von einem Knoten des Objekt-Explorer geöffnet wird, wird der benutzerdefinierte Bericht der Liste zuletzt verwendeter Objekte unter hinzugefügt **benutzerdefinierte Berichte** im Kontextmenü des Knotens. Wenn ein Standardbericht erstmalig geöffnet wird, außerdem wird auf der Liste zuletzt verwendeter Objekte unter **benutzerdefinierte Berichte**. Wenn eine benutzerdefinierte Berichtsdatei gelöscht wird, wird beim nächsten Auswählen des Elements eine Aufforderung angezeigt, das Element aus der Liste zuletzt verwendeter Objekte zu löschen.  
  
    1.  So ändern Sie die Anzahl der Dateien, die in der Liste zuletzt verwendeter Objekte angezeigt werden, auf die **Tools** Menü klicken Sie auf **Optionen** erweitern die **Umgebung** Ordner, und klicken Sie dann auf **Allgemeine**.  
  
    2.  Passen Sie die Anzahl für **Dateien angezeigt, in der Liste zuletzt verwendeter**.  
  
## Siehe auch  
[Benutzerdefinierte Berichte in Management Studio](../content/Custom-Reports-in-Management-Studio.md)  
[Verwenden benutzerdefinierter Berichte mit Eigenschaften von Objekt-Explorer-Knoten](../content/Use-Custom-Reports-with-Object-Explorer-Node-Properties.md)  
[Aufheben der Unterdrückung von Warnungen für das Ausführen von benutzerdefinierten Berichten](../content/Unsuppress-Run-Custom-Report-Warnings.md)  
[SQL Server Reporting Services](assetId:///b8d18d3d-9db0-43e7-8286-7b46cc3a37ed)  
  
