---
title: "Abfrageeigenschaften (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 07495669-6ed5-4004-904e-aae1230be5e4
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
# Abfrageeigenschaften (Visual Database Tools)
Diese Eigenschaften werden im Eigenschaftenfenster angezeigt, wenn im Abfrage- und Sicht-Designer eine Abfrage geöffnet ist. Sofern nichts anderes angegeben ist, können Sie diese Eigenschaften im Eigenschaftenfenster bearbeiten.  
  
> [!NOTE]  
> Die Eigenschaften in diesem Thema sind nicht alphabetisch, sondern nach Kategorie sortiert.  
  
## Optionen  
**Kategorie Identität**  
Erweitern Sie zum Anzeigen der **Namen** Eigenschaft.  
  
**Name**  
Zeigt den Namen der aktuellen Abfrage an. Kann in [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)] nicht geändert werden.  
  
**Datenbankname**  
Zeigt den Namen der Datenquelle für die ausgewählte Tabelle an.  
  
**Servername**  
Zeigt den Namen des Servers für diese Datenquelle an.  
  
**Kategorie Abfrage-Designer**  
Wird erweitert, um die restlichen Eigenschaften anzuzeigen.  
  
**Zieltabelle**  
Geben Sie den Namen der Tabelle an, in welche die Daten eingefügt werden sollen. Diese Liste wird angezeigt, wenn Sie eine INSERT-Abfrage oder MAKE TABLE-Abfrage erstellen. Für eine INSERT-Abfrage wählen Sie eine Tabelle aus der Liste aus.  
  
Für eine MAKE TABLE-Abfrage geben Sie den Namen der neuen Tabelle ein. Geben Sie zum Erstellen einer Zieltabelle in einer anderen Datenquelle einen vollqualifizierten Tabellennamen an, der den Namen der Zieldatenquelle, den Besitzer (falls erforderlich) und den Namen der Tabelle enthält.  
  
> [!NOTE]  
> Der Abfrage-Designer überprüft nicht, ob der Name bereits verwendet wird oder ob Sie über eine Berechtigung zum Erstellen der Tabelle verfügen.  
  
**DISTINCT-Werte**  
Geben Sie an, dass die Abfrage alle Duplikate im Resultset herausfiltert. Diese Option ist hilfreich, wenn Sie nur einige Spalten aus der Tabelle bzw. den Tabellen verwenden und diese möglicherweise doppelte Werte enthalten, oder wenn die Verknüpfung von mehreren Tabellen eine Verdopplung von Zeilen im Resultset zur Folge hat. Das Aktivieren dieser Option ist gleichbedeutend mit dem Einfügen des Worts DISTINCT in die Anweisung im SQL-Bereich.  
  
**GROUP BY-Erweiterung**  
Geben Sie an, dass zusätzliche Optionen für Abfragen verfügbar sind, die auf Aggregatabfragen basieren. (Gilt nur für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)].)  
  
**Alle Spalten ausgeben**  
Geben Sie an, dass sämtliche Spalten aller Tabellen in der aktuellen Abfrage in das Resultset aufgenommen werden. Wenn Sie diese Option entspricht der Angabe eines Sternchens (\*) anstelle einzelner Spaltennamen nach dem Schlüsselwort SELECT in der SQL-Anweisung.  
  
**Abfrageparameterliste**  
Zeigt Abfrageparameter an. Bearbeiten Sie die Parameter auf die Eigenschaft, und klicken Sie auf die Auslassungspunkte **(...)** rechts neben der Eigenschaft. (Gilt nur für generische OLE DB-Datenquellen.)  
  
**SQL-Kommentar**  
Zeigt eine Beschreibung der SQL-Anweisungen an. Um die ganze Beschreibung anzuzeigen oder zu bearbeiten, klicken Sie auf die Beschreibung, und klicken Sie dann auf die Auslassungspunkte **(...)** rechts neben der Eigenschaft. Kommentare können Informationen darüber enthalten, wer die Abfrage verwendet und wann sie verwendet wird. (Gilt nur für Datenbanken von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] 7.0 oder höher.)  
  
**Kategorie Oberste Angabe**  
Erweitern Sie zum Anzeigen der Eigenschaften für die **oben**, **Prozent**, **Ausdruck**, und **With Ties** Eigenschaften.  
  
**(Nach oben)**  
Geben Sie die Abfrage enthält eine TOP-Klausel, die nur die ersten zurückgibt *n* Zeilen oder ersten *n* Prozent der Zeilen im Resultset. In der Standardeinstellung gibt die Abfrage die ersten 10 Zeilen im Resultset zurück.  
  
Verwenden Sie dieses Feld, um die Anzahl der zurückzugebenden Zeilen zu ändern oder einen anderen Prozentwert anzugeben. (Gilt nur für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] oder höher.)  
  
**Ausdruck**  
Geben Sie die Anzahl oder den Prozentsatz der Zeilen an, die bzw. der von der Abfrage zurückgeben wird. Wenn Sie für **Prozent** Ja festlegen, wird mit dieser Zahl der Prozentsatz der Zeilen festgelegt, der von der Abfrage zurückgegeben wird. Wenn Sie für **Prozent** Nein festlegen, steht diese Zahl für die Anzahl der zurückzugebenden Zeilen. (Gilt nur für Datenbanken von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] 7.0 oder höher.)  
  
**Prozent**  
Geben Sie, dass die Abfrage nur die ersten *n* Prozent der Zeilen im Resultset. (Gilt nur für Datenbanken von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] 7.0 oder höher.)  
  
**WITH TIES**  
Geben Sie an, dass die Sicht eine WITH TIES-Klausel enthält. Diese Klausel ist hilfreich, wenn eine Sicht sowohl eine ORDER BY-Klausel als auch eine TOP-Klausel mit Prozentangabe enthält. Wenn diese Option festgelegt ist und der Prozentbereich in der Mitte einer Zeilenfolge mit identischen Werten in der ORDER BY-Klausel endet, wird die Sicht bis ans Ende der betreffenden Zeilenfolge erweitert. (Gilt nur für Datenbanken von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] 7.0 oder höher.)  
  
## Siehe auch  
[Abfrage mit Parametern & #40; Visual Database Tools & #41;](../content/Query-with-Parameters--Visual-Database-Tools-.md)  
[Entwerfen von Abfragen und Sichten Gewusst-wie-Themen & #40; Visual Database Tools & #41;](../content/Design-Queries-and-Views-How-to-Topics--Visual-Database-Tools-.md)  
  
