---
title: "Verkn&#252;pfen von Tabellen &#252;ber mehrere Spalten (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 56a158bc-a42a-4b78-baad-4721d2d22cd3
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
# Verkn&#252;pfen von Tabellen &#252;ber mehrere Spalten (Visual Database Tools)
Sie können Tabellen über mehrere Spalten verknüpfen. Dies bedeutet, dass Sie eine Abfrage erstellen können, die Übereinstimmungen von Zeilen aus den zwei Tabellen nur herstellt, wenn diese mehrere Bedingungen erfüllen. Wenn die Datenbank eine Beziehung mehrere Fremdschlüssel enthält\-Schlüsselspalten in einer Tabelle mit einem mehrspaltigen Primärschlüssel in der anderen Tabelle, können Sie diese Beziehung einen Join über mehrere Spalten zu erstellen. Weitere Informationen finden Sie unter [& #40; Tabellen automatisch verknüpfen Visual Database Tools & #41;](../content/Join-Tables-Automatically--Visual-Database-Tools-.md).  
  
Auch wenn die Datenbank nicht mehrfach enthält\-Spalte foreign\-Beziehung, können Sie die Verknüpfung manuell erstellen.  
  
### So erstellen Sie manuell einen Join über mehrere Spalten  
  
1.  Hinzufügen der [Diagrammbereich](../content/Diagram-Pane--Visual-Database-Tools-.md) die Tabellen, die Sie hinzufügen möchten.  
  
2.  Ziehen Sie den Namen der ersten Joinspalte aus dem Fenster der ersten Tabelle, und legen Sie diesen auf der entsprechenden Spalte im Fenster der zweiten Tabelle ab. Einen Join kann nicht auf der Grundlage von text-, ntext- oder image-Spalten erstellt werden.  
  
    > [!NOTE]  
    > Im Allgemeinen müssen die Joinspalten denselben (oder einen kompatiblen) Datentyp aufweisen. Wenn z. B. die Joinspalte in der ersten Tabelle eine Datenspalte ist, müssen Sie diese mit einer Datenspalte in der zweiten Tabelle verknüpfen. Wenn es sich jedoch bei der ersten Joinspalte um eine Integer-Spalte handelt, muss die zu verknüpfende Spalte ebenfalls vom Integer-Datentyp sein, kann jedoch eine andere Größe aufweisen. In einzelnen Fällen ist ein Join scheinbar inkompatibler Spalten dank impliziter Datentypkonvertierungen jedoch möglich.  
    >   
    > Die [Abfrage- und Sicht-Designer](../content/Query-and-View-Designer-Tools--Visual-Database-Tools-.md) überprüft nicht die Datentypen der Spalten, die Sie verwenden, um eine Verknüpfung zu erstellen, aber wenn Sie die Abfrage ausführen, die Datenbank wird eine Fehlermeldung angezeigt, wenn die Datentypen nicht kompatibel sind.  
  
3.  Ziehen Sie den Namen der zweiten Joinspalte aus dem Fenster der ersten Tabelle, und legen Sie diesen auf der entsprechenden Spalte im Fenster der zweiten Tabelle ab.  
  
4.  Wiederholen Sie Schritt drei für jedes weitere Paar von Joinspalten in den beiden Tabellen.  
  
5.  Führen Sie die Abfrage aus.  
  
## Siehe auch  
[Abfragen mit Joins & #40; Visual Database Tools & #41;](../content/Query-with-Joins--Visual-Database-Tools-.md)  
  
