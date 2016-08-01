---
title: "Regeln zum Aktualisieren von Ergebnissen (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: de131ef0-ccbd-446f-9400-b93c7b8fa537
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
# Regeln zum Aktualisieren von Ergebnissen (Visual Database Tools)
In vielen Fällen können Sie die im Resultset Aktualisieren der [im Ergebnisbereich](../content/Results-Pane--Visual-Database-Tools-.md). Manchmal ist dies allerdings nicht möglich.  
  
In der Regel damit Ergebnisse aktualisiert werden, die [Abfrage- und Sicht-Designer](../content/Query-and-View-Designer-Tools--Visual-Database-Tools-.md) müssen ausreichende Informationen, um die Zeile in der Tabelle eindeutig identifizieren. Ein Beispiel ist der Fall, dass die Abfrage einen Primärschlüssel in die Ausgabeliste einfügt. Außerdem müssen Sie über eine ausreichende Berechtigung zum Update der Datenbank verfügen.  
  
Wenn die Abfrage auf einer Sicht basiert, kann sie aktualisiert werden. Dieselben Richtlinien werden angewendet, allerdings nicht nur auf die Sicht selbst, sondern auf die zugrunde liegenden Tabellen in der Sicht.  
  
> [!NOTE]  
> Der Abfrage- und Sicht-Designer kann nicht im Voraus ermitteln, ob Sie ein auf einer Sicht basierendes Resultset aktualisieren können. Daher werden alle Sichten angezeigt, obwohl Sie diese möglicherweise nicht aktualisieren können.  
  
Die folgende Tabelle gibt eine Übersicht über die einzelnen Fälle, in denen Sie Abfrageergebnisse im Ergebnisbereich aktualisieren bzw. nicht aktualisieren können. Häufig wird durch die verwendete Datenbank bestimmt, ob die Ergebnisse einer Abfrage aktualisiert werden können.  
  
|Query|Können die Ergebnisse aktualisiert werden?|  
|---------|---------------------------|  
|Abfrage auf Grundlage einer Tabelle mit Primärschlüssel in der Ausgabeliste|Ja (außer wie im Folgenden aufgeführt).|  
|Abfrage auf Grundlage einer Tabelle ohne eindeutigen Index und Primärschlüssel|Hängt von der Abfrage und der Datenbank ab. Einige Datenbanken lassen Updates zu, wenn genügend Informationen zur eindeutigen Identifizierung von Datensätzen verfügbar sind.|  
|Abfrage auf Grundlage mehrerer Tabellen, die nicht verknüpft sind|Nein.|  
|Abfrage auf Grundlage von Daten als gelesen markiert\-nur in der Datenbank|Nein.|  
|Abfrage auf Grundlage einer Sicht, die eine Tabelle ohne Einschränkungen umfasst|Ja (außer wie im Folgenden aufgeführt).|  
|Abfrage auf Grundlage von Tabellen verknüpft, mit einer\-zu\-1-Beziehung|Ja (außer wie im Folgenden aufgeführt).|  
|Abfrage auf Grundlage von Tabellen verknüpft, mit einer\-\-n-Beziehung|Meistens.|  
|Abfrage auf Grundlage von drei oder mehr Tabellen eine ist\-\-n-Beziehung|Nein.|  
|Abfrage auf Grundlage einer Tabelle, für die keine Updateberechtigung vorliegt|Kann gelöscht, aber nicht aktualisiert werden.|  
|Abfrage auf Grundlage einer Tabelle, für die keine Löschberechtigung vorliegt|Kann aktualisiert, aber nicht gelöscht werden.|  
|Aggregatabfrage|Nein.|  
|Abfrage auf Grundlage einer Unterabfrage, die Summen oder Aggregatfunktionen enthält|Nein.|  
|Abfrage, die das Schlüsselwort DISTINCT zum Ausschließen von doppelten Zeilen enthält|Nein.|  
|Abfrage, deren FROM-Klausel enthält, dass eines Benutzers\-benutzerdefinierte Funktion, die eine Tabelle und der Benutzer gibt\-definierte Funktion enthält mehrere select-Anweisungen|Nein.|  
|Abfrage, deren FROM-Klausel einen Inline-Benutzer enthält\-benutzerdefinierten Funktion|Ja.|  
  
Außerdem können Sie möglicherweise bestimmte Spalten in den Abfrageergebnissen nicht aktualisieren. Im Folgenden sind bestimmte Spaltentypen aufgeführt, die Sie im Ergebnisbereich nicht aktualisieren können.  
  
-   Spalten, die auf Ausdrücken basieren  
  
-   Spalten auf der Grundlage von skalaren Benutzer\-benutzerdefinierte Funktionen  
  
-   Zeilen oder Spalten, die von einem anderen Benutzer gelöscht wurden  
  
-   Zeilen oder Spalten, die von einem anderen Benutzer gesperrt wurden (gesperrte Zeilen können i. d. R. unmittelbar nach Aufhebung der Sperre aktualisiert werden)  
  
-   Timestamp- oder BLOB-Spalten  
  
## Siehe auch  
[Entwerfen von Abfragen und Sichten Gewusst-wie-Themen & #40; Visual Database Tools & #41;](../content/Design-Queries-and-Views-How-to-Topics--Visual-Database-Tools-.md)  
  
