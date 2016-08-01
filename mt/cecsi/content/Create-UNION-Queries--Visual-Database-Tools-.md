---
title: "Erstellen von UNION-Abfragen (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b5aafb1d-e4ed-4922-b790-56abc5ec551a
caps.latest.revision: 4
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
# Erstellen von UNION-Abfragen (Visual Database Tools)
Mit dem Schlüsselwort UNION können Sie die Ergebnisse von zwei SELECT-Anweisungen in eine Ergebnistabelle aufnehmen. Alle Zeilen, die von den beiden SELECT-Anweisungen zurückgegeben werden, werden zum Ergebnis des UNION-Ausdrucks kombiniert. Beispiele finden Sie unter [Wählen Beispiele (Transact-SQL)](assetId:///9b9caa3d-e7d0-42e1-b60b-a5572142186c).  
  
> [!NOTE]  
> Im Diagrammbereich kann nur eine SELECT-Klausel angezeigt werden. Wenn Sie eine UNION-Abfrage verwenden, wird der Bereich Tabellenvorgänge Abfrage-Designer daher nicht angezeigt.  
  
### So erstellen Sie eine zusammengeführte SELECT-Abfrage  
  
1.  Öffnen Sie eine Abfrage, oder erstellen Sie eine neue.  
  
2.  Geben Sie im Bereich SQL einen gültigen UNION-Ausdruck ein.  
  
    Das folgende Beispiel stellt einen gültigen UNION-Ausdruck dar.  
  
    ```  
    SELECT ProductModelID, Name  
    FROM Production.ProductModel  
    UNION  
    SELECT ProductModelID, Name   
    FROM dbo.Gloves;  
    ```  
  
3.  Auf der **-Abfrage-Designer** Menü klicken Sie auf **SQL ausführen** zum Ausführen der Abfrage.  
  
    Die UNION-Abfrage wird jetzt vom Abfrage-Designer formatiert.  
  
## Siehe auch  
[Unterstützte Abfragetypen &#40; Visual Database Tools &#41;](../content/Supported-Query-Types--Visual-Database-Tools-.md)  
[Entwerfen von Abfragen und Sichten Gewusst-wie-Themen &#40; Visual Database Tools &#41;](../content/Design-Queries-and-Views-How-to-Topics--Visual-Database-Tools-.md)  
[Durchführen Sie grundlegende Operationen mit Abfragen &#40; Visual Database Tools &#41;](../content/Perform-Basic-Operations-with-Queries--Visual-Database-Tools-.md)  
[UNION (Transact-SQL)](assetId:///607c296f-8a6a-49bc-975a-b8d0c0914df7)  
  
