---
title: "Einschlie&#223;en oder Ausschlie&#223;en von Zeilen (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ba4e1202-31a2-444d-8365-c68a530ef223
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
# Einschlie&#223;en oder Ausschlie&#223;en von Zeilen (Visual Database Tools)
Wenn Sie die Anzahl von durch eine SELECT-Abfrage zurückgegebenen Zeilen einschränken möchten, erstellen Sie Suchbedingungen oder Filterkriterien. In SQL werden Suchbedingungen entweder in die WHERE-Klausel der Anweisung eingefügt oder – wenn Sie eine Aggregatabfrage erstellen – in die HAVING-Klausel.  
  
> [!NOTE]  
> Sie können auch Suchbedingungen definieren, welche die von einer UPDATE-, INSERT RESULTS-, INSERT VALUES-, DELETE- oder MAKE TABLE-Abfrage betroffenen Zeilen angeben.  
  
Sobald die Abfrage ausgeführt wird, untersucht [!INCLUDE[ssDE](../content/includes/ssDE_md.md)] die Suchbedingung und wendet sie auf jede Zeile in den durchsuchten Tabellen an. Wenn eine Zeile die Bedingungen erfüllt, wird sie in die Abfrage aufgenommen. Eine Suchbedingung, die z. B. alle Mitarbeiter in einer bestimmten Region ermittelt, könnte folgendermaßen formuliert werden:  
  
```  
region = 'UK'  
```  
  
Die Definition der Kriterien für die Auswahl der Ergebniszeilen kann über mehrere Suchbedingungen erfolgen. Das folgende Kriterium für die Suche besteht z. B. aus zwei Suchbedingungen. Die Abfrage nimmt eine Zeile nur dann in das Resultset auf, wenn sie beide Bedingungen erfüllt.  
  
```  
region = 'UK' AND product_line = 'Housewares'  
```  
  
Sie können Bedingungen durch AND oder OR kombinieren. Im oben dargestellten Beispiel wird AND verwendet. Im Gegensatz hierzu sind die Bedingungen im folgenden Beispiel durch ein OR kombiniert. Das zurückgegebene Abfrageergebnis enthält alle Zeilen, die mindestens eine oder beide Suchbedingungen erfüllen:  
  
```  
region = 'UK' OR product_line = 'Housewares'  
```  
  
Für eine Spalte können auch mehrere Suchbedingungen kombiniert werden. Im folgenden Beispiel sind zwei Bedingungen für die Spalte Region kombiniert:  
  
```  
region = 'UK' OR region = 'US'  
```  
  
Ausführliche Informationen zum Kombinieren von Suchbedingungen finden Sie unter den folgenden Themen:  
  
-   [Konventionen für das Kombinieren von Suchbedingungen im Kriterienbereich & #40; Visual Database Tools & #41;](../content/Conventions-for-Combining-Search-Conditions-in-the-Criteria-Pane--Visual-Database-Tools-.md)  
  
-   [Geben Sie mehrerer Suchbedingungen für eine Spalte & #40 an. Visual Database Tools & #41;](../content/Specify-Multiple-Search-Conditions-for-One-Column--Visual-Database-Tools-.md)  
  
-   [Geben Sie mehrerer Suchbedingungen für mehrere Spalten & #40 an. Visual Database Tools & #41;](../content/Specify-Multiple-Search-Conditions-for-Multiple-Columns--Visual-Database-Tools-.md)  
  
-   [Kombinieren von Bedingungen, wenn AND hat Vorrang vor & #40; Visual Database Tools & #41;](../content/Combine-Conditions-When-AND-Has-Precedence--Visual-Database-Tools-.md)  
  
-   [Kombinieren von Bedingungen, wenn OR hat Vorrang vor & #40; Visual Database Tools & #41;](../content/Combine-Conditions-When-OR-Has-Precedence--Visual-Database-Tools-.md)  
  
## Beispiele  
Es folgen einige Beispiele für Abfragen mit verschiedenen Operatoren und Zeilenkriterien:  
  
-   **Literal** ein Textelement, Zahlen-, Datums- oder logischer Wert. Im folgenden Beispiel wird ein Literalwert für die Suche nach allen Zeilen für Mitarbeiter in Großbritannien verwendet:  
  
    ```  
    WHERE region = 'UK'  
    ```  
  
-   **Spaltenverweis** vergleicht die Werte in einer Spalte mit den Werten in einer anderen. Im folgenden Beispiel wird in der `products`-Tabelle nach allen Zeilen gesucht, in denen für die Produktionskosten ein kleinerer Wert als für die Frachtkosten angegeben ist:  
  
    ```  
    WHERE prod_cost < ship_cost  
    ```  
  
-   **Funktion** einen Verweis auf eine Funktion, die die Datenbank wieder\-End aufgelöst werden kann, um einen Wert für die Suche zu berechnen. Die Funktion kann eine Funktion definiert, die von der Datenbankserver oder einem Benutzer\-benutzerdefinierte Funktion, die einen skalaren Wert zurückgibt. Im folgenden Beispiel wird von Aufträgen gesucht (die GETDATE ()-Funktion liefert das aktuelle Datum):  
  
    ```  
    WHERE order_date = GETDATE()  
    ```  
  
-   **NULL** das folgende Beispiel sucht eine `authors` Tabelle nach allen Autoren einen Vornamen hinterlegt haben:  
  
    ```  
    WHERE au_fname IS NOT NULL  
    ```  
  
-   **Berechnung** das Ergebnis einer Berechnung, die Literalwerte, Spaltenverweise oder andere Ausdrücke enthalten kann. Im folgenden Beispiel wird in einer Tabelle mit dem Namen `products` nach allen Zeilen gesucht, in denen der Einzelhandelspreis mindestens doppelt so hoch ist wie der Herstellungspreis:  
  
    ```  
    WHERE sales_price > (prod_cost * 2)  
    ```  
  
## Siehe auch  
[Entwerfen von Abfragen und Sichten Gewusst-wie-Themen & #40; Visual Database Tools & #41;](../content/Design-Queries-and-Views-How-to-Topics--Visual-Database-Tools-.md)  
[Geben Sie Suchkriterien & #40. Visual Database Tools & #41;](../content/Specify-Search-Criteria--Visual-Database-Tools-.md)  
[Abfrage mit Parametern & #40; Visual Database Tools & #41;](../content/Query-with-Parameters--Visual-Database-Tools-.md)  
  
