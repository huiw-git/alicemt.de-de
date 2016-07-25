---
title: "Exemplarische Vorgehensweise: Hinzuf&#252;gen und &#196;ndern von Datenbankdiagrammen"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 228caa0d-8f24-46ab-86d1-b6d8631322bc
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
# Exemplarische Vorgehensweise: Hinzuf&#252;gen und &#196;ndern von Datenbankdiagrammen
In dieser exemplarischen Vorgehensweise wird das Erstellen und Ändern eines Datenbankdiagramms und das Ausführen von Änderungen an der Datenbank mithilfe der Datenbankdiagrammkomponente erläutert. Es wird in Einzelschritten erklärt, wie Diagrammen Tabellen hinzugefügt werden, wie Beziehungen zwischen Tabellen erstellt werden, wie Einschränkungen und Indizes für Spalten erstellt werden und wie die Ebene der Informationen geändert wird, die für die einzelnen Tabellen angezeigt werden.  
  
## Erforderliche Komponenten  
Wenn Sie diese exemplarische Vorgehensweise abschließen möchten, müssen folgende Voraussetzungen erfüllt sein:  
  
-   Zugriff auf [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] mit der [!INCLUDE[ssSampleDBobject](../content/includes/ssSampleDBobject_md.md)]-Beispieldatenbank  
  
-   Ein Konto bei Datenbankbesitzer **Dbo** Berechtigungen  
  
> [!NOTE]  
> Wenn Sie versuchen, über ein Konto Änderungen vorzunehmen, das nicht über ausreichende Rechte zum Ändern von Tabellen verfügt, wird eine Fehlermeldung angezeigt.  
  
## Erstellen eines Diagramms  
  
#### So erstellen Sie ein neues Datenbankdiagramm  
  
1.  Auf der **Ansicht** Menü klicken Sie auf **Objekt-Explorer**.  
  
2.  Öffnen Sie den Knoten Datenbanken und dann den Knoten [!INCLUDE[ssSampleDBobject](../content/includes/ssSampleDBobject_md.md)].  
  
3.  Rechts\-Klicken Sie auf den Knoten Datenbankdiagramme, und wählen Sie **Neues Datenbankdiagramm**.  
  
    Wenn die Datenbank nicht über die zum Erstellen von Diagrammen erforderlichen Objekte verfügt, wird folgende Meldung angezeigt: **Dieser Datenbank fehlt mindestens eines der Unterstützungsobjekte, die erforderlich sind, damit Diagramme für die Datenbank erstellt werden können. Möchten Sie sie erstellen?** Klicken Sie auf **Ja**.  
  
    Die **Tabelle hinzufügen** das Dialogfeld wird angezeigt.  
  
4.  Wählen Sie **Adresstyp (Person)** und **Adresse (Person)** und klicken Sie auf **Hinzufügen**.  
  
    Dem Diagramm werden zwei Tabellen hinzugefügt.  
  
5.  Schließen der **Tabelle hinzufügen** Dialogfeld.  
  
#### So zeigen Sie unterschiedliche Spaltendaten an  
  
1.  Rechts\-Klicken Sie auf die `Address` Tabelle. Zeigen Sie im Kontextmenü auf **Tabellenansicht**, und klicken Sie dann auf **Standard**.  
  
    Das Tabellenraster zeigt drei Spalten: **Spaltenname**, **-Datentyp**, und **NULL-Werte zulassen**.  
  
2.  Rechts\-Klicken Sie auf die `Address` auf **Tabellenansicht** und wählen Sie **Schlüssel**.  
  
    Das Tabellenraster zeigt eine Spalte mit der Tabelle\-Spaltennamen. Es werden nur solche Spalten angezeigt, die an Indizes beteiligt sind.  
  
## Erstellen neuer Tabellen  
  
#### So erstellen Sie Tabellen im Datenbank-Designer  
  
1.  Rechts\-Klicken Sie auf den Datenbankdiagramm-Designer außerhalb der vorhandenen Tabellen, und wählen Sie **neue Tabelle**.  
  
2.  In den **Namen auswählen** Dialogfeld klicken Sie auf **OK** akzeptieren den Standardnamen **Table1**.  
  
    Ein neues Tabellenraster mit drei Spalten angezeigt: **Spaltenname**, **-Datentyp**, und **NULL-Werte zulassen**.  
  
3.  Fügen Sie die folgende Informationen, um **Table1**:  
  
    |**Spaltenname**|**Datentyp**|**NULL-Werte zulassen**|  
    |-------------------|-----------------|-------------------|  
    |**T1col1**|**int**|aktiviert|  
    |**T1col2**|**varchar(50)**|aktiviert|  
    |**T1col3**|**float**|aktiviert|  
  
4.  Rechts\-Klicken Sie auf `T1col1` und wählen Sie **Primärschlüssel festlegen**.  
  
    Neben dem Spaltennamen wird ein Schlüsselsymbol angezeigt.  
  
5.  Aus der **Datei** Menü klicken Sie auf **Diagramm1**.  
  
6.  In den **Namen auswählen** Dialogfeld klicken Sie auf **OK** akzeptieren den Standardnamen **Diagram1**.  
  
7.  Die **Speichern** das Dialogfeld mit einer Meldung wird angezeigt, die `Table1` wird in der Datenbank gespeichert werden. Klicken Sie auf **Ja**.  
  
## Ändern der Tabellenstruktur  
Im Datenbank-Designer können Sie CHECK-Einschränkungen hinzufügen und Beziehungen zwischen Tabellen herstellen.  
  
#### So erstellen Sie CHECK-Einschränkungen  
  
1.  In `Table1`, mit der rechten Maustaste\-Klicken Sie auf die `T1col3` Zeile, und wählen Sie **Check-Einschränkungen**.  
  
    Die **Check-Einschränkungen** das Dialogfeld wird angezeigt.  
  
2.  Klicken Sie auf **Hinzufügen**.  
  
    Eine neue Einschränkung wird in der **ausgewählte Check-Einschränkung** Liste mit dem Standardnamen `CK_Table1`.  
  
3.  Wählen Sie die **Ausdruck** Zeile im Raster, und klicken Sie auf die Schaltfläche mit den Auslassungspunkten.  
  
    Die **Check-Einschränkungsausdruck** das Dialogfeld wird angezeigt.  
  
4.  Typ **T1col3 > 5** und klicken Sie auf **OK**.  
  
    `Table1` verfügt jetzt über eine Einschränkung, die alle Werte in ein `T1col3` muss größer als 5 sein.  
  
5.  Klicken Sie auf **Schließen**.  
  
#### So erstellen Sie Beziehungen zwischen Tabellen  
  
1.  Erstellen Sie im Datenbank-Designer eine neue Tabelle mit dem Namen `Table2` und mit folgenden Spalten:  
  
    |**Spaltenname**|**Datentyp**|**NULL-Werte zulassen**|  
    |-------------------|-----------------|-------------------|  
    |**T2col1**|**int**|nicht aktiviert|  
    |**T2col2**|**varchar(50)**|aktiviert|  
    |**T2col3**|**xml**|aktiviert|  
  
    > [!NOTE]  
    > Die Spalten in einer Fremdschlüsselbeziehung, die sich auf der Seite des Primärschlüssels befinden, müssen Teil eines Primärschlüssels oder einer Unique-Einschränkung sein.  
  
2.  Ziehen Sie `T2col1` in `T1col1`.  
  
    Werden zwei Dialogfelder angezeigt: **Foreign Key-Beziehung** im Hintergrund und **Tabellen und Spalten** im Vordergrund.  
  
3.  Klicken Sie auf **OK** die neue Beziehung zu speichern.  
  
4.  Klicken Sie auf **OK** erneut.  
  
## Erstellen von Indizes  
Sie können für die meisten Datentypen (einschließlich XML) Indizes erstellen.  
  
#### So erstellen Sie einen Standardindex  
  
1.  Rechts\-Klicken Sie auf `Table1` und wählen Sie **Indizes\/Schlüssel**.  
  
    Die **Indizes\/Schlüssel** das Dialogfeld wird angezeigt.  
  
2.  Klicken Sie auf **Hinzufügen**.  
  
    Wird ein neuer Index in der **ausgewählten primären\/Eindeutiger Schlüssel oder Index** Liste mit einem Standardnamen wie `IX_Table1`.  
  
3.  Wählen Sie die **Spalten** Zeile, und klicken Sie auf die Schaltfläche mit den Auslassungspunkten.  
  
    Die **Indexspalten** das Dialogfeld wird angezeigt.  
  
4.  Klicken Sie auf die Dropdownliste\-Pfeil unter **Spaltenname** und wählen Sie `T1col2`.  
  
    > [!NOTE]  
    > Sie können diesem Index zusätzliche Spalten hinzufügen, indem Sie die Zelle unter `T1col2` auswählen und einen anderen Spaltennamen auswählen.  
  
5.  Klicken Sie auf **OK** um diesen Index zu speichern.  
  
6.  Klicken Sie auf **Schließen** in der **Indizes\/Schlüssel** (Dialogfeld).  
  
#### So erstellen Sie einen XML-Index  
  
1.  Rechts\-Klicken Sie auf `T2col1` und wählen Sie **Primärschlüssel festlegen**.  
  
    > [!NOTE]  
    > Voraussetzung für das Hinzufügen eines XML-Index ist es, dass eine andere Spalte in der Tabelle als gruppierter Primärschlüssel festgelegt wurde.  
  
2.  Rechts\-Klicken Sie auf die `T2col3` für die Zeile im `Table2` und wählen Sie **XML-Indizes**.  
  
    Die **XML-Indizes** das Dialogfeld wird angezeigt.  
  
3.  Klicken Sie auf **Hinzufügen**.  
  
    Ein XML-Index mit Standardwerten werden hinzugefügt werden, um die **Ausgewählter XML-Index** Liste.  
  
4.  Klicken Sie auf **Schließen**.  
  
    > [!NOTE]  
    > XML-Indizes werden pro erstellt\-Spalte. Dabei ist der erste XML-Index primär, und alle weiteren Indizes sind sekundär.  
  
## Speichern des Diagramms  
Sämtliche von Ihnen an einem Diagramm vorgenommenen Änderungen werden erst nach dem Speichern des Diagramms an die Datenbank gesendet. Wenn Probleme oder Konflikte auftreten, wird ein Dialogfeld mit weiteren Informationen angezeigt.  
  
#### So speichern Sie ein Datenbankdiagramm  
  
1.  Auf der **Datei** Klicken Sie im Menü **Diagramm1**.  
  
    Die **Speichern** das Dialogfeld wird angezeigt. Wenn **Warnung bei betroffenen Tabellen** ist ausgewählt, werden Informationen zu neuen oder geänderten Tabellen aufgeführt.  
  
2.  Klicken Sie auf **OK**.  
  
3.  Wenn Fehler aufgetreten sind, die **Post\-Benachrichtigungen speichern** das Dialogfeld wird angezeigt, die Fehler und ihre Ursachen. Beheben Sie die Fehler, und speichern Sie das Diagramm anschließend erneut.  
  
## Nächste Schritte  
Hierbei handelt es sich um ein einfaches Diagramm, das nur zwei vorhandene und zwei neue Tabellen enthält. Damit wird jedoch das Potenzial zur Diagrammdarstellung einer vorhandenen Datenbank oder zur visuellen Erstellung eines neuen Schemas veranschaulicht. Mit folgenden Funktionen können Sie Ihre Fähigkeiten vertiefen:  
  
-   Erstellen neuer Diagramme mit Gruppen verbundener Tabellen  
  
-   Anpassen der für jede Tabelle angezeigten Informationsmenge  
  
-   Ändern des Layouts und Hinzufügen von Anmerkungen  
  
-   Kopieren des Diagramms in eine Bitmap  
  
## Siehe auch  
[Anpassen der Menge an Informationen, die in Diagrammen & #40 angezeigt. Visual Database Tools & #41;](../content/Customize-the-Amount-of-Information-Displayed-in-Diagrams--Visual-Database-Tools-.md)  
[Richten Sie den Datenbankdiagramm-Designer & #40; Visual Database Tools & #41;](../content/Set-Up-Database-Diagram-Designer--Visual-Database-Tools-.md)  
[Hinzufügen von Tabellen zu Diagrammen & #40; Visual Database Tools & #41;](../content/Add-Tables-to-Diagrams--Visual-Database-Tools-.md)  
[Erstellen Sie Beziehungen zwischen Tabellen in einem Diagramm & #40. Visual Database Tools & #41;](../content/Create-Relationships-Between-Tables-on-a-Diagram--Visual-Database-Tools-.md)  
[Erstellen von XML-Indizes](assetId:///6ecac598-355d-4408-baf7-1b2e8d4cf7c1)  
[Kopieren Sie ein Abbild eines Datenbankdiagramms in die Zwischenablage & #40. Visual Database Tools & #41;](../content/Copy-an-Image-of-a-Database-Diagram-to-the-Clipboard--Visual-Database-Tools-.md)  
[Arbeiten Sie mit dem Diagrammlayout & #40. Visual Database Tools & #41;](../content/Work-with-Diagram-Layout--Visual-Database-Tools-.md)  
  
