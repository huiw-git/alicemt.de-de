---
title: "Hinzuf&#252;gen vorhandener Elemente zu einem Projekt"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 084b3879-e96b-45a7-b421-6a4b0db2b92b
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
# Hinzuf&#252;gen vorhandener Elemente zu einem Projekt
Sie können neue Elemente zu einem Projekt hinzufügen, um die Funktionalität der Anwendung zu erweitern. Bei einem vorhandenen Element kann es sich um eine Abfrage oder eine beliebige Datei handeln. [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] verfügt über zwei Projekttypen: [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Skriptprojekt und Analysis Services-Skriptprojekt. Der Projekttyp bestimmt die Abfragedateien, die Sie zu einem Projekt hinzufügen können. So können Sie beispielsweise eine [!INCLUDE[tsql](../content/includes/tsql_md.md)]-Abfrage (eine Datei mit einer SQL-Erweiterung) zu einem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Skriptprojekt hinzufügen, nicht jedoch zu einem Analysis Services-Skriptprojekt. Um zusätzliche Erweiterungen zu einem Projekttyp zu verknüpfen, finden Sie unter [Gewusst wie: Zuordnen von Dateierweiterungen zu einem Code-Editor](assetId:///193630f4-93de-4950-8f36-68702531f925).  
  
### So fügen Sie eine vorhandene Abfrage oder eine beliebige Datei zu einem Projekt hinzu  
  
1.  Wählen Sie im Projektmappen-Explorer ein Zielprojekt aus.  
  
2.  Auf der **Projekt** Menü klicken Sie auf **Vorhandenes Element hinzufügen**.  
  
    **Suchen in**  
    Suchen Sie in der Liste nach den Dateien oder Ordnern, die dem Projekt hinzugefügt werden sollen. Die Dateien von XML-Webdiensten und ASP.NET-Webanwendungen sind auf dem Webserver gespeichert.  
  
    **Desktop**  
    Zeigt die Dateien und Ordner auf dem Desktop an.  
  
    **Eigene Projekte**  
    Zeigt die Dateien und Ordner auf der standardmäßigen **Meine Projekte** Speicherort.  
  
    **Arbeitsplatz**  
    Zeigt den Inhalt der **Arbeitsplatz** Ordner.  
  
    **Dateiname**  
    Mithilfe dieser Option können Sie die anzuzeigenden Dateien oder Ordner filtern. Geben Sie den Dateinamen, nach dem gefiltert werden soll, vollständig oder teilweise ein. Als Platzhalter können Sie das Sternchen (`*`) verwenden.  
  
    > [!NOTE]  
    > Navigieren Sie zu Web-und Netzwerkadressen durch Eingabe der URL oder Netzwerkpfad Pfads in der **Dateiname** Feld. Z. B. **http:\/\/Mywebsite** werden unter der Webadresse Mywebsite, und **\\\\Myserver\\MeineFreigabe** zeigt die Dateien an die myshare auf Myserver.  
  
    **Dateityp**  
    Mithilfe dieser Option können Sie Dateien nach der Dateierweiterung filtern. Jedes Produkt listet Standardfilter für die am häufigsten verwendeten Dateitypen auf.  
  
    **Hinzufügen**  
    Verwenden Sie diese Dropdownliste\-unten, um das Element zum Projekt hinzufügen, und öffnen Sie das Element im Standardeditor.  
  
    -   **Hinzufügen**  
  
        Kopiert ein vorhandenes Objekt in den Projektordner auf dem Datenträger und fügt das Objekt dem ausgewählten Projekt im Projektmappen-Explorer hinzu. Die an diesem Objekt vorgenommenen Änderungen haben keine Auswirkungen auf das Objekt am ursprünglichen Speicherort. Dies ist der Standardeditor für diesen Dateityp.  
  
    -   **Als Link hinzufügen**  
  
        Fügt dem Projekt die ausgewählte Datei hinzu und öffnet sie mit dem Standard-Editor für den Dateityp. Mit dieser Option wird die ursprünglich ausgewählte Datei geöffnet. Die Datei wird nicht in den Projektordner kopiert.  
  
3.  Beim Hinzufügen von Abfragedateien werden Sie im Verbindungsdialogfeld aufgefordert, eine Verbindung für die Abfrage anzugeben. Klicken Sie auf **Abbrechen** im Verbindungsdialogfeld, wenn Sie nicht für die Abfrage keine Verbindung zuordnen möchten.  
  
4.  Wird die Datei hinzugefügt werden, die **Abfragen** oder **verschiedene Dateien** -Ordner des Projekts.  
  
## Siehe auch  
[Projektmappen-Explorer](../content/Solution-Explorer.md)  
[Hinzufügen neuer Elemente zu einem Projekt](../content/Add-New-Items-to-a-Project.md)  
[Entfernen oder Löschen eines Elements oder Projekts](../content/Remove-or-Delete-an-Item-or-Project.md)  
  
