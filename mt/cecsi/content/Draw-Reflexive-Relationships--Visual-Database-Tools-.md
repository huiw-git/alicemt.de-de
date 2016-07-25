---
title: "Zeichnen reflexiver Beziehungen (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e218363f-faec-46d5-9904-a537fbcc994d
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
# Zeichnen reflexiver Beziehungen (Visual Database Tools)
Sie erstellen eine reflexive Beziehung, um eine Spalte oder mehrere Spalten in einer Tabelle mit einer anderen Spalte oder mehreren Spalten in derselben Tabelle zu verknüpfen. Angenommen, in der Tabelle `employee` gibt es die Spalte `emp_id` und die Spalte `mgr_id`. Da jeder Manager gleichzeitig ein Mitarbeiter ist, verknüpfen Sie diese beiden Spalten, indem Sie eine Beziehungslinie innerhalb der Tabelle ziehen. Durch diese Beziehung wird sichergestellt, dass jede der Tabelle hinzugefügte Manager-ID mit einer vorhandenen Mitarbeiter-ID übereinstimmt.  
  
Bevor Sie eine Beziehung erstellen, müssen Sie zunächst einen Primärschlüssel oder eine UNIQUE-Einschränkung für die Tabelle definieren. Anschließend verknüpfen Sie die Primärschlüsselspalte mit einer übereinstimmenden Spalte. Wenn die Beziehung erstellt ist, wird die übereinstimmende Spalte der Fremdschlüssel für die Tabelle.  
  
### So erstellen Sie eine reflexive Beziehung  
  
1.  Klicken Sie im Datenbankdiagramm auf den Zeilenselektor für die Datenbankspalte, die Sie zu einer anderen Spalte in Beziehung setzen möchten, und ziehen Sie den Mauszeiger aus der Tabelle heraus, bis eine Linie angezeigt wird.  
  
2.  Ziehen Sie die Linie zurück in die ausgewählte Tabelle.  
  
3.  Lassen Sie die Maustaste los. Die **Tabellen und Spalten** das Dialogfeld wird angezeigt.  
  
4.  Wählen Sie die Fremdschlüsselspalte und die Primärschlüsseltabelle sowie -spalte aus, zu denen eine Beziehung hergestellt werden soll.  
  
5.  Wählen Sie **OK** zweimal, um die Beziehung zu erstellen.  
  
Beim Ausführen von Abfragen für eine Tabelle können eine reflexive Beziehung erstellen einen\-Join. Informationen über Abfragen in Tabellen mit Joins finden Sie unter [Abfragen mit Joins & #40; Visual Database Tools & #41;](../content/Query-with-Joins--Visual-Database-Tools-.md).  
  
## Siehe auch  
[Abfragen mit Joins & #40; Visual Database Tools & #41;](../content/Query-with-Joins--Visual-Database-Tools-.md)  
  
