---
title: "Darstellungsweise von Joins im Abfrage- und Sicht-Designer (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 20a99dcb-83bd-4aa6-9139-92e2e5ba4887
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
# Darstellungsweise von Joins im Abfrage- und Sicht-Designer (Visual Database Tools)
Wenn Tabellen verknüpft werden, die [Abfrage- und Sicht-Designer](../content/Query-and-View-Designer-Tools--Visual-Database-Tools-.md) stellt die Verknüpfung grafisch in die [Diagrammbereich](../content/Diagram-Pane--Visual-Database-Tools-.md) und mithilfe von SQL-Syntax in der [SQL-Bereich](../content/SQL-Pane--Visual-Database-Tools-.md).  
  
## Diagrammbereich  
Im Diagrammbereich wird im Abfrage- und Sicht-Designer eine Joinlinie zwischen den verknüpften Datenspalten an. Der Abfrage- und Sicht-Designer zeigt eine Joinlinie für jede Joinbedingung an. Die folgende Abbildung zeigt eine Joinlinie zwischen zwei verknüpften Tabellen:  
  
![Joinlinie zeigt Beziehung zwischen zwei Tabellen](../content/media/dv3wbig.png "dv3wbig")  
  
Wenn Tabellen durch mehrere Joinbedingungen miteinander verknüpft sind, zeigt der Abfrage- und Sicht-Designer wie im folgenden Beispiel mehrere Joinlinien an:  
  
![Mit mehr als einer Joinbedingung verknüpfte Tabellen](../content/media/dv3w9n1.png "dv3w9n1")  
  
Wenn die verknüpften Datenspalten nicht angezeigt werden (z. B. das Rechteck darstellt, der Tabelle oder\-strukturiertes Objekt minimiert ist oder die Verknüpfung einen Ausdruck beinhaltet), der Abfrage- und Ansicht-Designer setzt die Joinlinie in die Titelleiste des Rechtecks, das für die Tabelle oder die Tabelle\-strukturiertes Objekt.  
  
Die Form des Symbols in der Mitte der Joinlinie zeigt an, wie Tabellen bzw.\-strukturierter Objekte verknüpft werden. Die Join-Klausel einer anderen als gleich verwendet (\=), der Operator im Symbol Joinlinie angezeigt. In der folgenden Tabelle werden die in Joinlinien verwendeten Symbole aufgelistet.  
  
|**Joinliniensymbol**|**Beschreibung**|  
|----------------------|-------------------|  
|![Visual Database Tools (Symbol)](../content/media/dv3wbih.png "dv3wbih")|Innerer Join (erstellt mit einem Gleichheitszeichen).|  
|![Visual Database Tools (Symbol)](../content/media/dv3wbii.png "dv3wbii")|Innerer Join mit dem Operator "größer als".|  
|![Visual Database Tools (Symbol)](../content/media/dv3wbij.png "dv3wbij")|Äußerer Join, bei dem sämtliche Zeilen aus der links angezeigten Tabelle aufgenommen werden, auch wenn keine Übereinstimmungen in der verknüpften Tabelle vorliegen.|  
|![Visual Database Tools (Symbol)](../content/media/dv3wbik.png "dv3wbik")|Äußerer Join, bei dem sämtliche Zeilen aus der rechts angezeigten Tabelle aufgenommen werden, auch wenn keine Übereinstimmungen in der verknüpften Tabelle vorliegen.|  
|![Visual Database Tools (Symbol)](../content/media/dv3wbil.png "dv3wbil")|Ein vollständiger äußerer Join, bei der alle Zeilen aus beiden Tabellen aufgenommen werden, auch wenn keine Übereinstimmungen in der verknüpften Tabelle vorliegen.|  
  
Die Symbole an den Enden der Joinlinie zeigen den Jointyp an. In der folgenden Tabelle werden die Jointypen und die an den Enden der Joinslinien verwendeten Symbole aufgelistet.  
  
|**Symbole an den Enden der Joinlinien**|**Jointyp**|  
|---------------------------------|--------------------|  
|![Visual Database Tools (Symbol)](../content/media/dv3wbim.png "dv3wbim")|Eine\-zum\-eine Verknüpfung.|  
|![Visual Database Tools (Symbol)](../content/media/dv3wbin.png "dv3wbin")|Eine\-auf\-viele Join.|  
|![Visual Database Tools (Symbol)](../content/media/dv3wbio.png "dv3wbio")|Der Abfrage- und Sicht-Designer konnte den Joinstyp nicht ermitteln. Dies tritt häufig auf, wenn Sie einen Join manuell erstellt haben.|  
  
## SQL-Bereich  
Ein Join kann in einer SQL-Anweisung auf unterschiedliche Weise ausgedrückt werden. Die genaue Syntax ergibt sich aus der verwendeten Datenbank und daraus, wie Sie den Join definiert haben.  
  
Folgende Syntaxoptionen werden beim Verknüpfen von Tabellen angewendet:  
  
-   **JOIN-Qualifizierer in der FROM-Klausel**.   Die Schlüsselwörter INNER und OUTER geben den Jointyp an. Diese Syntax entspricht dem Standard bei ANSI 92 SQL.  
  
    Wenn Sie z. B. die Tabellen `publishers` und `pub_info` über die Spalte `pub_id` der beiden Tabellen verknüpfen, kann dies mit folgender SQL-Anweisung ausgedrückt werden:  
  
    ```  
    SELECT *  
    FROM publishers INNER JOIN pub_info ON  
       publishers.pub_id = pub_info.pub_id  
    ```  
  
    Wenn Sie einen äußeren Join erstellen, wird LEFT OUTER oder RIGHT OUTER statt INNER verwendet.  
  
-   **WHERE-Klausel zum Vergleich der Spalten in beiden Tabellen**.   Eine WHERE-Klausel wird angezeigt, wenn die Datenbank die JOIN-Syntax nicht unterstützt (oder wenn Sie sie selbst eingegeben haben). Wenn der Join über die WHERE-Klausel erstellt wird, werden beide Tabellennamen in der FROM-Klausel angegeben.  
  
    Die folgende Anweisung verknüpft z. B. die Tabellen `publishers` und `pub_info`.  
  
    ```  
    SELECT *  
    FROM publishers, pub_info  
    WHERE publishers.pub_id = pub_info.pub_id  
    ```  
  
## Siehe auch  
[Abfragen mit Joins & #40; Visual Database Tools & #41;](../content/Query-with-Joins--Visual-Database-Tools-.md)  
[Nehmen Sie im Dialogfeld & #40; Visual Database Tools & #41;](../content/Join-Dialog-Box--Visual-Database-Tools-.md)  
  
