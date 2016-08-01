---
title: "Dialogfeld &#39;R&#228;umliche Indizes&#39; (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4d84239a-68c7-4aa2-8602-2b51dd07260f
caps.latest.revision: 5
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
# Dialogfeld &#39;R&#228;umliche Indizes&#39; (Visual Database Tools)
Verwenden der **Räumlichkeitsindizes** Dialogfeld zum Erstellen von Indizes für Spalten des der **Geometrie** oder **Geography** -Datentyp (*räumliche Spalten*), die nicht mit indiziert werden die **Index\/Schlüssel** (Dialogfeld). Jede räumliche Spalte kann mehr als einen räumlichen Index aufweisen, jedoch müssen sie einzeln erstellt werden.  
  
Informationen zu Einschränkungen für die Erstellung von räumlichen Indizes finden Sie unter [Übersicht über räumliche Indizes](assetId:///b1ae7b78-182a-459e-ab28-f743e43f8293).  
  
## Optionen  
**Ausgewählter räumlicher Index**  
Listet vorhandene räumliche Indizes auf. Wählen Sie einen Index aus, um dessen Eigenschaften anzuzeigen. Wenn die Liste leer ist, wurden bisher keine räumlichen Indizes für die Tabelle definiert.  
  
**Hinzufügen**  
Erstellt einen neuen räumlichen Index.  
  
**Delete**  
Löscht die im ausgewählten räumlichen Index die **ausgewählter Räumlichkeitsindex** Liste.  
  
**Zellen pro Objekt**  
Gibt die Anzahl von Zellen\-pro\--Objekt, das für ein einzelnes räumliches Objekt im Index verwendet werden kann. Bei dieser Zahl kann es sich um jede ganze Zahl von 1 bis 8192 handeln. Der Standardwert ist 16.  
  
Wenn ein Objekt mehr Zellen als bedeckt *n*, verwendet die Indizierung so viele Zellen wie erforderlich, geben Sie eine vollständige Top\-Ebene Mosaik. In solchen Fällen ist es möglich, dass ein Objekt mehr als die angegebene Anzahl von Zellen erhält. In diesem Fall ist die maximale Anzahl die Anzahl der Zellen, die oben generiert\-Ebene Raster hängt die **auf Ebene1** Dichte.  
  
**Spalten**  
Gibt den Spaltennamen und die Sortierreihenfolge an.  
  
**IsSpatialIndex**  
Gibt an, dass ein räumlicher Index ausgewählt ist.  
  
**Ebene 1**  
Gibt die Dichte des ersten\-des Rasters der Ebene (oben).  
  
**Ebene 2**  
Gibt die Dichte der zweiten\-auf Raster.  
  
**Ebene 3**  
Gibt die Dichte des dritten\-auf Raster.  
  
**Ebene 4**  
Gibt die Dichte des vierten\-auf Raster.  
  
**Mosaikschema**  
Gibt das Mosaikschema an:  
  
**Geometrie** Spaltenoptionen:  
  
-   **Geometrieraster** für eine Geometry-Spalte  
  
-   **Geografieraster** für eine Geography-Spalte  
  
**Typ**  
Gibt an, dass ein räumlicher Index ausgewählt ist.  
  
**X\-max**  
Gibt die x\-Koordinate des oberen\-rechte Ecke des umgebenden Felds. Diese Eigenschaft wird abgeblendet, wenn die **Mosaikschema** ist **Geografieraster**.  
  
**X\-Min.**  
Gibt die x\-Koordinate der unteren\-linken Ecke des umgebenden Felds. Diese Eigenschaft wird abgeblendet, wenn die **Mosaikschema** ist **Geografieraster**.  
  
**Y\-max**  
Gibt den y\--Koordinate des oberen\-rechte Ecke des umgebenden Felds. Diese Eigenschaft wird abgeblendet, wenn die **Mosaikschema** ist **Geografieraster**.  
  
**Y\-Min.**  
Gibt den y\-Koordinate der unteren\-linken Ecke des umgebenden Felds. Diese Eigenschaft wird abgeblendet, wenn die **Mosaikschema** ist **Geografieraster**.  
  
**Identität**  
Wenn die Kategorie erweitert ist, zeigt der **Namen** und **Beschreibung** Eigenschaftenfelder.  
  
**(Name)**  
Zeigt den Namen des räumlichen Indexes an. Wenn ein neuer Index erstellt wird, erhält dieser einen Standardnamen, der auf der Tabelle im aktiven Fenster des Tabellen-Designers basiert. Sie können den Namen jederzeit ändern.  
  
**Beschreibung**  
Beschreibt den Index. Um eine detailliertere Beschreibung zu schreiben, klicken Sie auf **Beschreibung** und klicken Sie dann auf die Schaltfläche mit den Auslassungspunkten (**...**), die rechts neben dem Eigenschaftenfeld angezeigt wird. Dadurch wird ein größerer Bereich verfügbar, in den Sie Text eingeben können.  
  
**Kategorie Tabellen-Designer**  
Wenn die Kategorie erweitert ist, werden Informationen zu den Eigenschaften dieses räumlichen Indexes angezeigt.  
  
**Füllspezifikation**  
Wenn die Kategorie erweitert ist, werden Informationen für **Füllfaktor** und **Pad_index**.  
  
**Füllfaktor**  
Geben Sie an, zu welchem Prozentsatz die Indexseite vom System gefüllt werden kann. Wenn eine Seite gefüllt ist, muss beim Hinzufügen neuer Daten die Seite geteilt werden. Dies beeinträchtigt die Leistung.  
  
-   Ein Wert von 100 bedeutet, dass die Seiten gefüllt werden. Diese Einstellung erfordert den geringsten Aufwand an Speicherplatz, ist aber auch am wenigsten effektiv. Diese Einstellung sollte verwendet werden, nur, wenn es keine Änderungen an den Daten, z. B. lesen werden\-nur Tabelle.  
  
-   Durch einen niedrigeren Wert bleibt auf den Datenseiten ein größerer Bereich leer. Dadurch müssen die Datenseiten seltener geteilt werden, wenn Indizes größer werden. Dies erfordert allerdings mehr Speicherplatz. Diese Einstellung empfiehlt sich eher, wenn Änderungen an den Daten in der Tabelle vorgenommen werden.  
  
**Index mit Leerstellen auffüllen**  
Stellt Seiten in diesem Index der gleiche Prozentwert für leere Bereiche (Auffüllung), angegeben **Füllfaktor**.  
  
**Seitensperren sind zulässig**  
Gibt an, ob die Seite\-Ebene Sperren für diesen Index zugelassen ist. Zulassen oder untersagen Seite\-Sperren auf Leistung der Datenbank auswirkt.  
  
**Re\-compute** **Statistiken**  
Gibt an, ob beim Erstellen des Index neue Statistiken berechnet werden sollen. Durch erneutes Berechnen von Statistiken wird die Erstellung der Indizes verlangsamt, die Abfrageleistung wird jedoch meist verbessert.  
  
**Zeilensperren sind zulässig**  
Gibt an, ob die Zeile\-Ebene Sperren für diesen Index zugelassen ist. Zulassen oder untersagen Zeile\-Sperren auf Leistung der Datenbank auswirkt.  
  
## Siehe auch  
[Übersicht über räumliche Indizes](assetId:///b1ae7b78-182a-459e-ab28-f743e43f8293)  
  
