---
title: "Angeben der TOP-Klausel in Abfragen (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ba7d7c10-9bb3-4d9b-90b0-5fa94ecae59b
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
# Angeben der TOP-Klausel in Abfragen (Visual Database Tools)
Die TOP-Klausel gibt nur die ersten *n* oder *n Prozent* Zeilen aus einer Abfrage. Mithilfe einer TOP-Klausel können Sie ressourcenschonend nur einen Teil der Ergebnisse anstatt alle Abfrageergebnisse prüfen, um zu ermitteln, ob die Abfrage ordnungsgemäß arbeitet.  
  
### So geben Sie die TOP-Klausel in Abfragen an  
  
1.  Öffnen Sie im Projektmappen-Explorer eine Abfrage, oder erstellen Sie eine neue Abfrage.  
  
2.  Aus der **Ansicht** Menü klicken Sie auf **Eigenschaftenfenster**.  
  
3.  In der **Eigenschaftenfenster**, suchen und erweitern Sie die **Oberste Angabe** Eigenschaft.  
  
4.  Klicken Sie auf die **(oben)** untergeordnete Eigenschaft, und legen Sie es auf **Ja**.  
  
5.  In der **Ausdruck** untergeordnete Eigenschaft, einen Ausdruck, der ein numerisches Ergebnis hat (z. B. "10" oder "2\*5").  
  
6.  Klicken Sie auf die **Prozent** untergeordnete Eigenschaft, und geben Sie an, ob behandelt die **Ausdruck** Eigenschaft als Prozentanteil aller Zeilen zurückgegeben (Ja) oder als absolute Anzahl der Zeilen (Nein) zurückgegeben.  
  
7.  Wenn die Abfrage die ORDER BY-Klausel verwendet wird, klicken Sie auf die **With Ties** untergeordnete Eigenschaft, und wählen Sie **Ja** auf alle Zeilen in einer Gruppe angezeigt werden, wenn nur ein Teil der Gruppe enthalten ist oder **Nr.** werden abgeschnitten.  
  
Bei der Ausführung dieser Schritte werden Sie feststellen, dass die im SQL-Bereich angezeigte TOP-Klausel entsprechend den aktuellen Einstellungen der Eigenschaften geändert wird.  
  
> [!NOTE]  
> Sie können auch die Werte der untergeordneten Eigenschaften von ändern die **Oberste Angabe** durch Bearbeiten der TOP-Klausel im SQL-Bereich.  
  
## Siehe auch  
[Entwerfen von Abfragen und Sichten Gewusst-wie-Themen & #40; Visual Database Tools & #41;](../content/Design-Queries-and-Views-How-to-Topics--Visual-Database-Tools-.md)  
[Abfrageeigenschaften & #40; Visual Database Tools & #41;](../content/Query-Properties--Visual-Database-Tools-.md)  
  
