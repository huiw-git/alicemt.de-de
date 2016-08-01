---
title: "Regeln f&#252;r das Eingeben von Suchwerten (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3c8134b7-83f4-41b4-99c8-e3949a685ff5
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
# Regeln f&#252;r das Eingeben von Suchwerten (Visual Database Tools)
In diesem Thema werden die Konventionen erläutert, die beim Eingeben der folgenden Arten von Literalwerten für eine Suchbedingung beachtet werden müssen:  
  
-   Textwerte  
  
-   Numerische Werte  
  
-   Datumswerte  
  
-   Logische Werte  
  
> [!NOTE]  
> Die Informationen in diesem Thema wird von den Regeln für standard-SQL abgeleitet\-92. Datenbanken können SQL jedoch auf unterschiedliche Art implementieren. Die hier angezeigten Richtlinien sind daher nicht in jedem Fall gültig. Informationen zum Eingeben von Suchwerten in einer bestimmten Datenbank erhalten Sie in der Dokumentation zur verwendeten Datenbank.  
  
## Suchen von Textwerten  
Die folgenden Richtlinien gelten für die Eingabe von Textwerten in Suchbedingungen:  
  
-   **Anführungszeichen** Schließen Sie Textwerte in einfache Anführungszeichen, wie in diesem Beispiel für einen Nachnamen:  
  
    ```  
    'Smith'  
    ```  
  
    Bei der Eingabe einer Suchbedingung in der [im Kriterienbereich](../content/Criteria-Pane--Visual-Database-Tools-.md), können Sie einfach den Textwert eingeben und die Abfrage und Sicht-Designer wird automatisch einfache Anführungszeichen umgeben.  
  
    > [!NOTE]  
    > In einigen Datenbanken werden Begriffe in einfachen Anführungszeichen als Literalwerte interpretiert, wohingegen Begriffe in doppelten Anführungszeichen als Datenbankobjekte wie Spalten- oder Tabellenverweise interpretiert werden. Daher ist es möglich, dass der Abfrage- und Sicht-Designer die Begriffe in doppelten Anführungszeichen zwar akzeptiert, sie jedoch nicht wie erwartet interpretiert.  
  
-   **Einbetten von Apostrophen** enthält die gesuchten Daten ein einzelnes Anführungszeichen (ein Apostroph), können Sie zwei einfache Anführungszeichen, um anzugeben, dass dieses einzelne Anführungszeichen als Literalwert und kein Trennzeichen eingeben. Mit der folgenden Bedingung suchen Sie z. B. nach dem Wert "Swann's Way":  
  
    ```  
    ='Swann''s Way'  
    ```  
  
-   **Längenbeschränkungen** überschreiten Sie nicht die maximale Länge der SQL-Anweisung für die Datenbank bei der Eingabe langer Zeichenfolgen.  
  
-   **Groß-/Kleinschreibung** folgen den Regeln der Groß-und Kleinschreibung für die Datenbank, die Sie verwenden. Die verwendete Datenbank bestimmt, ob bei Textsuchen die Groß- und Kleinschreibung beachtet werden muss. In einigen Datenbanken muss z. B. den Operator "\=" bedeutet eine genaue Groß-und Kleinschreibung\-vertrauliche Übereinstimmung, während andere Übereinstimmungen für eine beliebige Kombination aus Groß-und Kleinbuchstaben zulassen.  
  
    Wenn Sie nicht sicher, ob die Datenbank eine Anfrage verwendet sind\-/Kleinschreibung beachten, können die obere oder untere-Funktionen in der Suchbedingung konvertiert die Daten der Suche die Groß-/Kleinschreibung wie im folgenden Beispiel dargestellt:  
  
    ```  
    WHERE UPPER(lname) = 'SMITH'  
    ```  
  
## Suchen von numerischen Werten  
Die folgenden Richtlinien gelten für die Eingabe von numerischen Werten in Suchbedingungen:  
  
-   **Anführungszeichen** Zahlen dürfen nicht in Anführungszeichen einschließen.  
  
-   **Nicht\-numerische Zeichen** enthalten keine nicht\-numerische Zeichen außer das Dezimaltrennzeichen (gemäß der **regionalen Einstellungen** Dialogfeld des Windows-Systemsteuerung) und dem negativen Vorzeichen (\-). Fügen Sie keine Zeichen für das Gruppieren von Ziffern (z. B. einen Punkt zwischen Tausendergruppen) oder Währungssymbole ein.  
  
-   **Dezimalzeichen** Wenn Sie ganze Zahlen eingeben, können Sie ein Dezimalzeichen einfügen, gibt an, ob der Wert für die gesuchte ist eine ganze Zahl oder eine reelle Zahl.  
  
-   **Wissenschaftliche Schreibweise** können Sie sehr große oder kleine Zahlen, die mit der wissenschaftlichen Schreibweise wie in diesem Beispiel eingeben:  
  
    ```  
    > 1.23456e-9  
    ```  
  
## Suchen von Datumsangaben  
Das für die Eingabe von Daten zu verwendende Format hängt von der Datenbank und dem Bereich des Abfrage- und Sicht-Designers ab, in dem Sie diese eingeben.  
  
> [!NOTE]  
> Falls Sie nicht wissen, welches Format Ihre Datenquelle verwendet, geben Sie in der Filterzeile des Kriterienbereichs ein Datum in einem Ihnen vertrauten Format ein. Der Designer solche Einträge in den meisten Fällen in das geeignete Format konvertieren.  
  
Im Abfrage- und Sicht-Designer können die folgenden Datumsformate verwendet werden:  
  
-   **Gebietsschema\-bestimmte** für Datumsangaben im angegebenen Format der **Windows Ländereinstellungen** (Dialogfeld).  
  
-   **Datenbank\-bestimmte** jedes Format interpretiert, von der Datenbank.  
  
-   **ANSI-Standarddatum** ein Format, geschweifte Klammern verwendet, um der Marker würde "zum Kennzeichnen des Datums und eine Datumszeichenfolge, wie im folgenden Beispiel:  
  
    ```  
    { d '1990-12-31' }  
    ```  
  
-   **ANSI-Standarddatum/-Uhrzeit** ähnlich wie ANSI\-Standardformatbezeichner für Datum, aber "ts anstelle von" d"verwendet und Stunden, Minuten und Sekunden zum Datum hinzugefügt (mithilfe von 24\-Stunden), wie in diesem Beispiel für den 31. Dezember 1990 gezeigt:  
  
    ```  
    { ts '1990-12-31 00:00:00' }  
    ```  
  
    Im Allgemeinen wird das ANSI-Standarddatenformat bei Datenbanken verwendet, in denen Daten mit einem True-Date-Datentyp dargestellt werden. Im Gegensatz dazu wird das Datetime-Format bei Datenbanken verwendet, die den Datetime-Datentyp unterstützen.  
  
In der folgenden Tabelle werden die Datumsformate aufgeführt, die Sie in den verschiedenen Bereichen des Abfrage- und Sicht-Designers verwenden können.  
  
|**Bereich**|**Datumsformat**|  
|------------|-------------------|  
|Kriterien|Gebietsschema\-datenbankspezifische\-bestimmte ANSI-Standard<br /><br />Datumsangaben der [im Kriterienbereich](../content/Criteria-Pane--Visual-Database-Tools-.md) werden in einer Datenbank konvertiert\-kompatiblen Format im SQL-Bereich.|  
|SQL|Datenbank\-bestimmte ANSI-Standard|  
|Ergebnisse|Gebietsschema\-bestimmte|  
  
## Suchen von logischen Werten  
Das Format logischer Daten ist in den einzelnen Datenbanken unterschiedlich. In vielen Fällen wird der Wert False als Null (0) gespeichert. Der Wert True wird häufig als 1 und gelegentlich gespeichert als \-1. Die folgenden Richtlinien gelten für die Eingabe von logischen Werten in Suchbedingungen:  
  
-   Verwenden Sie zum Suchen des Werts False wie im folgenden Beispiel dargestellt eine 0:  
  
    ```  
    SELECT * FROM authors  
    WHERE contract = 0  
    ```  
  
-   Wenn Sie nicht genau wissen, welches Format Sie für die Suche eines Werts True verwenden sollen, versuchen Sie es wie im folgenden Beispiel mit dem Wert 1:  
  
    ```  
    SELECT * FROM authors  
    WHERE contract = 1  
    ```  
  
-   Alternativ können Sie den Bereich der Suche erweitern, indem für alle suchen nicht\-NULL-Wert, wie im folgenden Beispiel:  
  
    ```  
    SELECT * FROM authors  
    WHERE contract <> 0  
    ```  
  
## Siehe auch  
[Geben Sie Suchkriterien & #40. Visual Database Tools & #41;](../content/Specify-Search-Criteria--Visual-Database-Tools-.md)  
  
