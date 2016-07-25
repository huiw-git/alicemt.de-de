---
title: "Wertzusammenfassung oder -aggregation &#252;ber benutzerdefinierte Ausdr&#252;cke (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 34130ac1-0106-4766-b324-acb0b7bb6f6e
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
# Wertzusammenfassung oder -aggregation &#252;ber benutzerdefinierte Ausdr&#252;cke (Visual Database Tools)
Zusätzlich zu den Aggregatfunktionen zum Aggregieren von Daten können Sie benutzerdefinierte Ausdrücke zum Erstellen von Aggregatwerten verwenden. Außerdem können in allen Bereichen einer Aggregatabfrage benutzerdefinierte Ausdrücke an Stelle der Aggregatfunktionen verwendet werden.  
  
In der Tabelle `titles` kann beispielsweise eine Abfrage erstellt werden, die nicht nur den Durchschnittspreis anzeigt, sondern auch angibt, welcher Durchschnittspreis sich unter Berücksichtigung von Preisnachlässen ergeben würde.  
  
Ausdrücke auf Grundlage von Berechnungen für einzelne Zeilen in der Tabelle können nicht in die Abfrage aufgenommen werden. Ein Ausdruck muss auf einem Aggregatwert beruhen, da während der Berechnung des Ausdrucks nur Aggregatwerte verfügbar sind.  
  
### So geben Sie einen benutzerdefinierten Ausdruck für einen Zusammenfassungswert an  
  
1.  Geben Sie die Gruppen für die Abfrage an. Weitere Informationen finden Sie unter [Gruppieren von Zeilen in Abfrageergebnissen & #40; Visual Database Tools & #41;](../content/Group-Rows-in-Query-Results--Visual-Database-Tools-.md).  
  
2.  Verschieben Sie in eine leere Zeile im Kriterienbereich, und geben Sie den Ausdruck in der **Spalten** Spalte.  
  
    Die [Abfrage- und Sicht-Designer](../content/Query-and-View-Designer-Tools--Visual-Database-Tools-.md) weist automatisch einen Spaltenalias mit dem Ausdruck, um im Abfrageergebnis eine aussagekräftige Spaltenüberschrift erstellt. Weitere Informationen finden Sie unter [Erstellen von Spaltenaliasen & #40; Visual Database Tools & #41;](../content/Create-Column-Aliases--Visual-Database-Tools-.md).  
  
3.  In der **Group By** Spalte für den jeweiligen Ausdruck die Option **Ausdruck**.  
  
4.  Führen Sie die Abfrage aus.  
  
## Siehe auch  
[Sortieren und Gruppieren von Abfrageergebnissen & #40; Visual Database Tools & #41;](../content/Sort-and-Group-Query-Results--Visual-Database-Tools-.md)  
[Zusammenfassen von Abfrageergebnissen & #40; Visual Database Tools & #41;](../content/Summarize-Query-Results--Visual-Database-Tools-.md)  
  
