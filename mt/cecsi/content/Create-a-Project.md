---
title: "Erstellen eines Projekts"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7897be19-365b-4b06-bcf0-8a669f67a673
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
# Erstellen eines Projekts
Sie können innerhalb einer vorhandenen Projektmappe ein oder mehrere Projekte erstellen.  
  
### So erstellen Sie ein neues Projekt erstellen und fügen es zu einer Projektmappe hinzu  
  
1.  Wählen Sie die Projektmappe im Projektmappen-Explorer aus.  
  
2.  Auf der **Datei** auf **Hinzufügen**, und klicken Sie auf **Neues Projekt**.  
  
3.  In der  **Neues Projekt** einen Projekttyp klicken Sie im Dialogfeld.  
  
    **Vorlagen**  
    In der **Vorlagen** Wählen Sie eine Vorlage. Eine kurze Beschreibung der ausgewählten Projektvorlage angezeigt, darunter die **Vorlagen** Feld.  
  
    **Name**  
    Geben Sie den Namen des zu erstellenden Skriptprojekts ein. Ein Ordner mit dem gleichen Namen wie das Projekt wird auch erstellt, dem Speicherort angezeigt, dem **Speicherort** Feld. Für einige Projekte erstellt [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] Quell- und andere unterstützende Dateien, die dem neuen Projektordner hinzugefügt werden.  
  
    > [!NOTE]  
    > Für manche Projekttypen den **Namen** Textfeld ist nicht verfügbar, weil der Name die Angabe des Speicherorts festgelegt werden. Webanwendungen und Webdienste befinden sich beispielsweise auf einem Webserver und leiten ihren Namen aus dem virtuellen Verzeichnis ab, das auf diesem Server angegeben wurde.  
  
    Folgende Zeichen dürfen nicht in den Namen verwendet werden:  
  
    -   Pfund (\#)  
  
    -   Prozent (%)  
  
    -   Kaufmännisches Und-Zeichen (&)  
  
    -   Sternchen (\*)  
  
    -   Senkrechter Strich (|)  
  
    -   Umgekehrter Schrägstrich (\\)  
  
    -   Doppelpunkt (:)  
  
    -   Anführungszeichen (")  
  
    -   Kleiner als (<)  
  
    -   Größer als (>)  
  
    -   Fragezeichen (?)  
  
    -   Schrägstrich (\/)  
  
    -   Führende oder nachfolgende Leerzeichen (' ')  
  
    -   Microsoft Windows oder MS reservierte Namen\-DOS, z. B. ("Nul", "Aux", "con", "com1", "lpt1" usw.)  
  
    **Speicherort**  
    Geben Sie hier den Speicherort ein, an dem das Projekt erstellt werden soll, oder wählen Sie einen aus der Liste.  
  
    **Durchsuchen**  
    Zeigt die **Projektspeicherort** -Dialogfeld, navigieren Sie zu einem neuen Verzeichnis, in dem das Projekt gespeichert.  
  
    **Lösung**  
    Wählen Sie **neue Projektmappe erstellen** um eine Projektmappe im Projektmappen-Explorer. Wählen Sie **Hinzufügen** das neue Projekt der aktuell geöffneten Projektmappe im Projektmappen-Explorer hinzu.  
  
    **Projektmappenverzeichnis erstellen**  
    Aktivieren der **Projektmappenname** Textfeld. Diese Option erstellt ein neues Verzeichnis mit dem gewählten Namen für das Projekt und die Projektmappe.  
  
    **Projektmappenname**  
    Geben Sie den Namen der neuen Projektmappe ein, in der das Projekt erstellt werden soll. Dieses Feld verwendet standardmäßig den gleichen Namen eingeben in den **Namen** Feld.  
  
    **Hinweis** um auf diese Option zuzugreifen, müssen Sie auswählen, sowohl die **neue Projektmappe erstellen** in die **Lösung** und die **Projektmappenverzeichnis erstellen** Kontrollkästchen. Einige Projektvorlagen unterstützen diese Option nicht (z. B. Webanwendungen).  
  
    **Zur Quellcodeverwaltung hinzufügen**  
    Wenn dieses Kontrollkästchen aktiviert ist, wird die Quellcodeverwaltungs-Anwendung öffnet, wenn Sie klicken **OK**. Geben Sie alle Daten ein, die von der Quellcodeverwaltungs-Anwendung angefordert werden, um den Vorgang fortzusetzen. Um diese Option verwenden zu können, muss eine Quellcodeverwaltungs-Clientanwendung installiert sein.  
  
4.  Klicken Sie auf **OK**.  
  
Für das Skriptprojekt können Sie einen Namen festlegen. Die Ordnernamen hingegen werden von [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)] festgelegt und können nicht geändert werden. Sie können die Laufwerk- und Pfadspezifikation für den gemeinsamen Ordner konfigurieren, mit der **Neues Projekt hinzufügen** Dialogfeld. Rechts\-Klicken Sie auf das Symbol in **Projektmappen-Explorer**, und klicken Sie dann auf **Hinzufügen**. Der Standardspeicherort für skriptprojektordner ist: C:\\Documents and Settings\\*Benutzername*\\Eigene\\SQL Server Management Studio\\Projekte\\.  
  
## Siehe auch  
[Projektmappen-Explorer](../content/Solution-Explorer.md)  
[Hinzufügen eines vorhandenen Projekts zu einer Projektmappe](../content/Add-an-Existing-Project-to-a-Solution.md)  
[Hinzufügen neuer Elemente zu einem Projekt](../content/Add-New-Items-to-a-Project.md)  
[Hinzufügen vorhandener Elemente zu einem Projekt](../content/Add-Existing-Items-to-a-Project.md)  
[Ändern des Standardspeicherorts für Projekte](../content/Change-the-Default-Location-for-Projects.md)  
[Entfernen oder Löschen eines Elements oder Projekts](../content/Remove-or-Delete-an-Item-or-Project.md)  
[Löschen einer Projektmappe](../content/Delete-a-Solution.md)  
  
