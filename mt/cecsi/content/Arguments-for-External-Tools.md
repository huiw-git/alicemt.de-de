---
title: "Argumente f&#252;r externe Tools"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3991c13a-f23f-450b-a2ba-19391c399735
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
# Argumente f&#252;r externe Tools
Argumente sind Variablen, die die Studio-Umgebung Werte stellt für ein externes Tool aus beim Starten der **Tools** Menü. Externe tools, wie z. B. Editor hinzugefügt werden kann die **Tools** Menü mit den **Externe Tools** (Dialogfeld).  
  
In der folgenden Tabelle sind die Argumente für externe Tools aufgeführt.  
  
|Name|Argument|Beschreibung|  
|--------|------------|---------------|  
|**Elementpfad**|$(ItemPath)|Der vollständige Dateiname der aktuellen Quelle (definiert als Laufwerk \+ Pfad \+ Dateiname); leer, wenn eine nicht\-Quellcodefenster aktiv ist.|  
|**Elementverzeichnis**|$(ItemDir)|Das Verzeichnis der aktuellen Quelle (definiert als Laufwerk \+ Pfad); leer, wenn eine nicht\-Quellcodefenster aktiv ist.|  
|**Elementdateiname**|$(ItemFilename)|Der Dateiname der aktuellen Quelle (definiert als Dateiname); leer, wenn eine nicht\-Quellcodefenster aktiv ist.|  
|**Elementerweiterung**|$(ItemExt)|Die Dateinamenerweiterung der aktuellen Quelle.|  
|**Aktuelle Zeile**\*|$(CurLine)|Die aktuelle Zeilenposition des Cursors im Editor.|  
|**Aktuelle Spalte**\*|$(CurCol)|Die aktuelle Spaltenposition des Cursors im Editor.|  
|**Aktueller Text**\*|$(CurText)|Der aktuelle Text (das Wort unter der aktuellen Cursorposition oder eine einzelne\-Zeile auswählen, sofern vorhanden).|  
|**Zielpfad**|$(TargetPath)|Der vollständige Dateiname des Ziels (definiert als Laufwerk \+ Pfad \+ Dateiname).|  
|**Zielverzeichnis**|$(TargetDir)|Das Verzeichnis des Ziels.|  
|**Zielname**|$(TargetName)|Der Dateiname des Ziels.|  
|**Zielerweiterung**|$(TargetExt)|Die Dateinamenerweiterung des Ziels.|  
|**Projektverzeichnis**|$(ProjDir)|Das Verzeichnis des aktuellen Projekts (definiert als Laufwerk \+ Pfad).|  
|**Projektdateiname**|$(ProjFileName)|Der Dateiname des aktuellen Projekts (definiert als Laufwerk \+ Pfad \+ Dateiname).|  
|**Projektmappenverzeichnis**|$(SolutionDir)|Das Verzeichnis der aktuellen Projektmappe (definiert als Laufwerk \+ Pfad).|  
|**Projektmappen-Dateiname**|$(SolutionFileName)|Der Dateiname der aktuellen Projektmappe (definiert als Laufwerk \+ Pfad \+ Dateiname).|  
  
\*Die aktuelle Zeile, die aktuelle Spalte bzw. den aktuellen Text der Position des Cursors im Text-Editor basiert auf wie in der Statusleiste angezeigt.  
  
## Siehe auch  
[Externe Tools (Dialogfeld)](../content/External-Tools-Dialog-Box.md)  
[Allgemeine Benutzeroberflächenelemente](../content/General-User-Interface-Elements.md)  
  
