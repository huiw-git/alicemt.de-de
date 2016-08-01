---
title: "Externe Tools (Dialogfeld)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ba797203-24d0-4922-9b97-8ab483f1db14
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
# Externe Tools (Dialogfeld)
Verwenden der **Externe Tools** Dialogfeld Externe Tools wie z. B. SQLCMD oder den Editor zum Hinzufügen der **Tools** Menü. Externe Tools hinzufügen, können Sie auf einfache Weise andere Programme starten, bei der Arbeit in der [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] Umgebung. Sie können beim Starten des Tools Argumente und ein Arbeitsverzeichnis angeben. Darüber hinaus kann die Ausgabe einiger Tools angezeigt werden, der **Ausgabe** Fenster. Die **Externe Tools** Dialogfeld steht auf der **Tools** Menü.  
  
## Optionen  
**Inhalt des Menüs**  
Listet die Titel der gerade hinzugefügten Elemente der **Tools** Menü. Verwenden der **nach oben** und **nach unten** Pfeile, um die Reihenfolge der Elemente ändern, die im Menü angezeigt werden. Verwenden der **Löschen** Schaltfläche, um ein Element aus dem Menü zu entfernen.  
  
**Nach oben**  
Verschieben Sie das ausgewählte Tool höher in der Liste der Tools im der **Tools** Menü.  
  
**Nach unten**  
Verschieben Sie das ausgewählte Tool unten in der Liste der Tools im der **Tools** Menü.  
  
**Hinzufügen**  
Löscht die Textfelder, sodass Sie ein neues Tool angeben können.  
  
**Delete**  
Entfernen Sie das Tool oder den Befehl aus der **Menüinhalt** Liste auch auf die **Tools** Menü.  
  
**Titel**  
Geben Sie den Namen des Tools oder Befehls, der angezeigt wird die **Externe Tools** Untermenü der **Tools** Menü. Fügen Sie vor einem Buchstaben im Namen des Tools ein kaufmännisches Und-Zeichen (&) ein, um diesen Buchstaben als Tastenkombination anzugeben. Z. B. "& SQLCMD" SQLCMD anzeigen möchten, auf die **Tools** Menü.  
  
**Befehl**  
Gibt den Pfad zu der Datei an, die gestartet werden soll.  
  
**Argumente**  
Gibt die Variablen an, die an das Tool übergeben werden, wenn es im Menü aufgerufen wird. Argumente können Werte festlegen, die beim Starten an das Tool oder den Befehl übergeben werden. Ein Wert kann beispielsweise einen Dateinamen oder ein Verzeichnis angeben. Mit der Schaltfläche mit dem Pfeil können Sie aus einer Liste mit vordefinierten Argumenten auswählen. Sie können mehrere Argumente hinzufügen. Eine vollständige Liste vordefinierter Argumente und ihrer Definitionen finden Sie unter [Arguments for External Tools](../content/Arguments-for-External-Tools.md). Abhängig vom verwendeten Befehl oder Tool können Sie auch benutzerdefinierte Argumente eingeben, (wie z. B. Befehlszeilenoptionen).  
  
**Ausgabefenster verwenden**  
Öffnet das Ausgabefenster in [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)], in dem die Ausgabe des derzeit ausgeführten Befehls angezeigt wird. Nicht alle Tools zeigen ihre Ausgabe in einem Format an, das im Ausgabefenster dargestellt werden kann. Weitere Informationen finden Sie unter [Ausgabefenster](assetId:///9808e00c-c8f6-45cc-896e-192b8420f747).  
  
**Ausgabe als Unicode behandeln**  
Interpretiert die Ausgabe als Unicode.  
  
**Ausgangsverzeichnis**  
Gibt das Arbeitsverzeichnis für das Tool an. Mit der Schaltfläche mit dem Pfeil können Sie Verzeichnisse auswählen. Sie können mehrere Verzeichnisse auswählen.  
  
**Zur Argumenteingabe auffordern**  
Anzeigen der **Argumente** Dialogfeld können Sie Werte eingeben oder bearbeiten für die Argumente jedes Mal, wenn Sie das externe Tool starten.  
  
**Beim Beenden schließen**  
Schließt das vom Fenster geöffnete Tool, wenn das Tool geschlossen wird.  
  
## Beispiel  
Eingabe der folgenden Werte die **Externe Tools** Dialogfeld wird erstellen Sie ein Element mit der Bezeichnung "DAC", dass bei Auswahl dieser Option wird eine Eingabeaufforderung geöffnet und ausgeführt wird die **Sqlcmd** Hilfsprogramm mit der dedizierten administratorverbindung.  
  
|Klicken Sie im|Wert|  
|-------|---------|  
|**Titel**|DAC|  
|**Befehl**|[!INCLUDE[ssInstallPath](../content/includes/ssInstallPath_md.md)]Tools\\Binn\\SQLCMD.exe|  
|**Argumente**|\-A|  
  
## Siehe auch  
[Argumente für externe Tools](../content/Arguments-for-External-Tools.md)  
[Allgemeine Benutzeroberflächenelemente](../content/General-User-Interface-Elements.md)  
  
