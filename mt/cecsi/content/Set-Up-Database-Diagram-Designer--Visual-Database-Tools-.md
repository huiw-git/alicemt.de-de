---
title: "Einrichten des Datenbankdiagramm-Designers (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 927321ee-b459-4f5b-9719-4a7a95639143
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
# Einrichten des Datenbankdiagramm-Designers (Visual Database Tools)
Um den Datenbankdiagramm-Designer verwenden, es muss zunächst eingerichtet werden von einem Mitglied der **Db\_Besitzer** Rolle den Zugriff auf Diagramme zu steuern.  
  
### So richten Sie das Erstellen von Datenbankdiagrammen ein  
  
1.  Erweitern Sie im Objekt-Explorer einen Datenbankknoten.  
  
2.  Erweitern Sie den Knoten Datenbankdiagramme unter der Datenbankverbindung.  
  
3.  Wählen Sie **Ja** Wenn Sie aufgefordert werden, wenn Sie Datenbankdiagrammen einrichten möchten.  
  
    > [!NOTE]  
    > Damit werden die Datenbankdiagrammtabelle, gespeicherte Systemprozeduren und eine Systemfunktion in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Datenbank erstellt.  
  
4.  Visual Studio erstellt die folgenden Objekte für die Instanz von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]:  
  
    1.  sysdiagrams-Tabelle  
  
    2.  SP\_Alterdiagram gespeicherte Prozedur  
  
    3.  SP\_Creatediagram gespeicherte Prozedur  
  
    4.  SP\_Dropdiagram gespeicherte Prozedur  
  
    5.  SP\_Renamediagram gespeicherte Prozedur  
  
    6.  fn\_Diagramobjects-Funktion  
  
    7.  SP\_Helpdiagrams gespeicherte Prozedur  
  
    8.  SP\_Helpdiagramsdefinition gespeicherte Prozedur  
  
    9. SP\_Upgraddiagrams gespeicherte Prozedur  
  
## Siehe auch  
[Verstehen des Besitzes von Datenbankdiagrammen & #40; Visual Database Tools & #41;](../content/Understand-Database-Diagram-Ownership--Visual-Database-Tools-.md)  
[Aktualisieren von Datenbankdiagrammen aus älteren Versionen & #40; Visual Database Tools & #41;](../content/Upgrade-Database-Diagrams-from-Previous-Editions--Visual-Database-Tools-.md)  
[ALTER AUTHORIZATION (Transact-SQL)](assetId:///8c805ae2-91ed-4133-96f6-9835c908f373)  
  
