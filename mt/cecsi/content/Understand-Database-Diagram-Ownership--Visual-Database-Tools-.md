---
title: "Grundlagen des Besitzes von Datenbankdiagrammen (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4a27a48e-c4ef-4017-82b8-0cac4d0bbcac
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
# Grundlagen des Besitzes von Datenbankdiagrammen (Visual Database Tools)
Datenbankdiagramm-Designer verwenden, es zuerst werden von einem Mitglied der Db eingerichtet muss\_-Rolle (eine Rolle von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Datenbanken) zum Steuern des Zugriffs auf Diagramme. Jedes Diagramm hat nur einen einzigen Besitzer, und zwar den Benutzer, der das Diagramm erstellt hat. Weitere Informationen zum Einrichten der diagrammerstellung finden Sie unter [Set Up Database Diagram Designer & #40; Visual Database Tools & #41;](../content/Set-Up-Database-Diagram-Designer--Visual-Database-Tools-.md).  
  
Es folgen einige Punkte, die Sie beim Besitz von Diagrammen beachten sollten:  
  
-   Obwohl jeder beliebige Benutzer mit Zugriff auf eine Datenbank ein Diagramm erstellen kann, nachdem das Diagramm erstellt wurde, sind die einzigen Benutzer, die sie sehen können Ersteller des Diagramms und alle Mitglieder der Db\_Besitzerrolle.  
  
-   Der Besitz von Diagrammen kann nur an Mitglieder der-Datenbank übertragen werden\_Besitzerrolle. Und dies ist auch nur dann möglich, wenn der vorherige Besitzer des Diagramms aus der Datenbank entfernt wurde.  
  
-   Wenn der Besitzer eines Diagramms aus der Datenbank entfernt wurde, das Diagramm bleibt in der Datenbank bis ein Mitglied der Db\_Besitzerrolle versucht, ihn zu öffnen. An diesem Punkt die Db\_Besitzer Member können den Besitz des Diagramms zu übernehmen.  
  
## Siehe auch  
[Arbeiten Sie mit Datenbankdiagrammen & #40. Visual Database Tools & #41;](../content/Work-with-Database-Diagrams--Visual-Database-Tools-.md)  
[Richten Sie den Datenbankdiagramm-Designer & #40; Visual Database Tools & #41;](../content/Set-Up-Database-Diagram-Designer--Visual-Database-Tools-.md)  
  
