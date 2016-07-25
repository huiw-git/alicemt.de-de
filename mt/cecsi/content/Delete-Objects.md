---
title: "Objekte l&#246;schen"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 49541441-179c-40d3-ba0c-01bcae545984
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
# Objekte l&#246;schen
In diesem Dialogfeld können Sie eine Datenbank oder ein Datenbankobjekt löschen.  
  
## Liste der Benutzeroberflächenelemente  
**Zu löschendes Objekt**  
Zeigt die Namen, Typen, Besitzer und den Status von zu löschenden Objekten sowie Fehlermeldungen während der Ausführung an.  
  
> [!NOTE]  
> Ausführen **Löschen** in einer Datenbank entspricht der Verwendung von DROP DATABASE in [!INCLUDE[tsql](../content/includes/tsql_md.md)].  
  
**Abhängigkeiten anzeigen**  
Klicken Sie hier, um sowohl die vom gerade ausgewählten Objekt abhängigen Objekte als auch die Objekte anzuzeigen, von denen das aktuelle Objekt abhängt (Aufwärts- und Abwärtsabhängigkeit). Die Informationen der **Abhängigkeiten anzeigen** Dialogfeld gelesen\-nur.  
  
> [!NOTE]  
> Die Schaltfläche **Abhängigkeiten anzeigen** wird nicht für alle Datenbankobjekttypen angezeigt. Anzeigen von Abhängigkeiten bei der **Abhängigkeiten anzeigen** Schaltfläche ist nicht verfügbar\-Klicken Sie auf das Objekt im Objekt-Explorer, und klicken Sie dann auf **Abhängigkeiten anzeigen**.  
  
**Sicherungs- und Wiederherstellungsverlaufsinformationen für Datenbanken löschen**  
Wird nur angezeigt, wenn eine Datenbank gelöscht wird, dieses Kontrollkästchens wird die Sicherung und Wiederherstellung Verlauf für die betreffende Datenbank aus der **Msdb** Datenbank.  
  
**Bestehende Verbindungen schließen**  
Wird nur angezeigt, wenn eine Datenbank gelöscht wird. Bei Aktivierung dieses Kontrollkästchens werden die Verbindungen zur betreffenden Datenbank beendet.  
  
