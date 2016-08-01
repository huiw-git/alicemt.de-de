---
title: "Ausw&#228;hlen von Zeilen, die mit einem Wert nicht &#252;bereinstimmen (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 19898578-7b2f-401c-bb8f-9f2a017efdf7
caps.latest.revision: 3
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
# Ausw&#228;hlen von Zeilen, die mit einem Wert nicht &#252;bereinstimmen (Visual Database Tools)
Zum Suchen von Zeilen, die mit einem Wert nicht übereinstimmen, wird der Operator NOT verwendet.  
  
### So suchen Sie nach Zeilen, die mit einem Wert nicht übereinstimmen  
  
1.  Wenn Sie dies noch nicht getan haben, fügen Sie die Spalten oder Ausdrücke, die Sie in Ihrer Bedingung verwenden möchten die [im Kriterienbereich](../content/Criteria-Pane--Visual-Database-Tools-.md).  
  
2.  Suchen Sie die Zeile mit der Datenspalte oder den Ausdruck zu suchen und dann in der **Filter** Spalte des Datenblatts, geben Sie den Operator NOT gefolgt von einem Suchwert.  
  
Um beispielsweise alle Zeilen in der Tabelle `products` zu suchen, in denen der Wert in der Spalte für den Produktcode nicht mit "A" beginnt, können Sie folgende Suchbedingung eingeben:  
  
```  
NOT LIKE 'A%'  
```  
  
## Siehe auch  
[Regeln für das Eingeben von Suchwerten &#40; Visual Database Tools &#41;](../content/Rules-for-Entering-Search-Values--Visual-Database-Tools-.md)  
[Geben Sie Suchkriterien &#40. Visual Database Tools &#41;](../content/Specify-Search-Criteria--Visual-Database-Tools-.md)  
  
