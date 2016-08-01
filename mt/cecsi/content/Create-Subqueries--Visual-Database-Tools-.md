---
title: "Erstellen von Unterabfragen (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 34f6b9b4-ca3a-4a4f-9594-36e513f1c547
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
# Erstellen von Unterabfragen (Visual Database Tools)
Sie können die Ergebnisse einer Abfrage als Eingabe für eine andere Abfrage verwenden. Sie können die Ergebnisse einer Unterabfrage als Anweisung verwenden, die der IN-Funktion, den EXISTS-Operator oder die FROM-Klausel verwendet.  
  
Sie können eine Unterabfrage erstellen, indem Sie sie entweder direkt im SQL-Bereich eingeben oder indem Sie eine Abfrage kopieren und in eine andere einfügen.  
  
### So definieren Sie eine Unterabfrage im SQL-Bereich  
  
1.  Erstellen Sie die primäre Abfrage.  
  
2.  Wählen Sie die SQL-Anweisung im SQL-Bereich, und verwenden Sie dann **Kopie** verschieben Sie die Abfrage in die Zwischenablage.  
  
3.  Starten Sie die neue Abfrage, und verwenden Sie dann **Einfügen** die erste Abfrage in der neuen Abfrage WHERE oder FROM-Klausel verschieben.  
  
    Angenommen, Sie haben zwei Tabellen, `products` und `suppliers`, und möchten eine Abfrage erstellen, in der alle Produkte von Lieferanten aus Schweden angezeigt werden. Dazu erstellen Sie die erste Abfrage anhand der Tabelle `suppliers`, um alle schwedischen Lieferanten zu herauszusuchen:  
  
    ```  
    SELECT supplier_id  
    FROM supplier  
    WHERE (country = 'Sweden')  
    ```  
  
    Kopieren Sie diese Abfrage mit dem Befehl Kopieren in die Zwischenablage. Die zweite Abfrage erstellen Sie anhand der Tabelle `products`, in der die erforderlichen Produktinformationen aufgeführt werden:  
  
    ```  
    SELECT product_id, supplier_id, product_name  
    FROM products  
    ```  
  
    Fügen Sie der zweiten Abfrage im SQL-Bereich eine WHERE-Klausel hinzu. Dann fügen Sie die erste Abfrage aus der Zwischenablage ein. Setzen Sie die erste Abfrage in Klammern, sodass das Endergebnis wie folgt aussieht:  
  
    ```  
    SELECT product_id, supplier_id, product_name  
    FROM products  
    WHERE supplier_id IN  
       (SELECT supplier_id  
      FROM supplier  
      WHERE (country = 'Sweden'))  
    ```  
  
## Siehe auch  
[Unterstützte Abfragetypen & #40; Visual Database Tools & #41;](../content/Supported-Query-Types--Visual-Database-Tools-.md)  
[Geben Sie Suchkriterien & #40. Visual Database Tools & #41;](../content/Specify-Search-Criteria--Visual-Database-Tools-.md)  
  
