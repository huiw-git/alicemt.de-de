---
title: "Mehrbenutzerumgebungen (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 330bd48c-9427-4967-b58e-b7c492d5ee36
caps.latest.revision: 3
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
# Mehrbenutzerumgebungen (Visual Database Tools)
In einer Mehrbenutzerumgebung können andere Benutzer eine Verbindung mit der Datenbank herstellen, in der Sie arbeiten, und Änderungen daran vornehmen. Im Ergebnis können mehrere Benutzer ggf. gleichzeitig mit demselben Datenbankobjekt arbeiten. In einer Mehrbenutzerumgebung kann es daher vorkommen, dass sich die Änderungen anderer Benutzer auf die Datenbank auswirken, während Sie selbst gerade Änderungen vornehmen, und umgekehrt.  
  
Bei der Arbeit mit Datenbanken in einer Mehrbenutzerumgebung stellen die Zugriffsberechtigungen ein zentrales Thema dar. Die Berechtigungen, die Sie in einer Datenbank besitzen, spielen die entscheidende Rolle im Hinblick auf die Aufgaben, die Sie in der Datenbank ausführen können. Zum Ändern von Objekten in einer Datenbank müssen Sie z. B. die erforderlichen Schreibberechtigungen für die Datenbank besitzen. Weitere Informationen über Berechtigungen finden Sie in der Datenbankdokumentation. Weitere Informationen finden Sie unter [Berechtigungen und Visual Database Tools & #40; Visual Database Tools & #41;](../content/Permissions-and-Visual-Database-Tools--Visual-Database-Tools-.md).  
  
Wenn Sie die an einer Tabelle vorgenommenen Änderungen speichern, überprüft der Tabellen-Designer, ob die Datenbank seit Ihrem letzten Speichern von Änderungen modifiziert wurde. Falls ein anderer Benutzer die Datenbank geändert hat, werden Sie darüber benachrichtigt. Eventuell müssen Sie diese Änderungen abgleichen. Weitere Informationen finden Sie unter [Abstimmen Änderungen von mehreren Benutzern & #40; Visual Database Tools & #41;](../content/Reconcile-Changes-Made-by-Multiple-Users--Visual-Database-Tools-.md).  
  
In einer Mehrbenutzerumgebung sind einige Besonderheiten zu beachten, damit einander widerstreitende Änderungen vermieden werden. Weitere Informationen finden Sie unter [Probleme der Datenbankentwicklung & #40; Visual Database Tools & #41;](../content/Issues-of-Database-Evolution--Visual-Database-Tools-.md).  
  
Ein Weg, Probleme zu vermeiden, ist das Arbeiten an einer Kopie der Datenbank, z. B. einer Testdatenbank. Sie können dann ein Änderungsskript erstellen, das Ihre Änderungen enthält und das Sie nach der offline vorgenommenen Klärung auf die Originaldatenbank anwenden. Weitere Informationen finden Sie unter [Entwicklung, Test und Produktionsdatenbanken & #40; Visual Database Tools & #41;](../content/Development--Test--and-Production-Databases--Visual-Database-Tools-.md).  
  
