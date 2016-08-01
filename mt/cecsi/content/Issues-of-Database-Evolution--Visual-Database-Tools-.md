---
title: "Fragen zur Datenbankentwicklung (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1ed6ae10-d212-4ec2-8569-1b94ab1cba6d
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
# Fragen zur Datenbankentwicklung (Visual Database Tools)
Wenn Sie die Struktur einer bereitgestellten Datenbank ändern, sollten Sie insbesondere darauf achten, dass die Änderungen mit den vorhandenen Daten und der vorhandenen Datenbankstruktur kompatibel sind. Besondere Vorkehrungen können bei den folgenden Änderungen erforderlich sein:  
  
-   **Hinzufügen einer Einschränkung** Wenn Sie eine Einschränkung hinzufügen, enthält die Tabelle möglicherweise bereits Daten, die nicht erfüllt. Wenn Sie versuchen, die neue Einschränkung zu speichern der [das Dialogfeld Benachrichtigung nach dem Speichervorgang & #40; Visual Database Tools & #41;](../content/Post-Save-Notifications-Dialog-Box--Visual-Database-Tools-.md) informiert Sie, dass der Datenbankserver die Einschränkung nicht erstellen konnte. Um die Datenbank auf die Übernahme der neuen Einschränkung zu erzwingen, löschen Sie die **vorhandene Daten bei Erstellung überprüfen** das Kontrollkästchen.  
  
-   **Hinzufügen einer Beziehung** Wenn Sie eine Beziehung hinzufügen, enthält die Tabelle möglicherweise bereits Zeilen der fremden\-Schlüsseltabelle, die keine entsprechende Zeilen in der primären\-Schlüsseltabelle. Das bedeutet, dass die vorhandenen Daten die Forderung nach referenzieller Integrität nicht erfüllen. Wenn Sie versuchen, die neue Beziehung zu speichern der[das Dialogfeld Benachrichtigung nach dem Speichervorgang & #40; Visual Database Tools & #41;](../content/Post-Save-Notifications-Dialog-Box--Visual-Database-Tools-.md) Sie werden informiert, dass der Datenbankserver die überarbeitete nicht speichern konnte foreign\-Schlüsseltabelle. Um die Datenbank auf die Übernahme der Änderung zu erzwingen, löschen Sie die **vorhandene Daten bei Erstellung überprüfen** das Kontrollkästchen.  
  
-   **Ändern einer Tabelle zu einer indizierten Ansicht** wenn Sie eine Tabelle ändern, die an einer indizierten Microsoft SQL Server-Sicht beteiligt ist, gehen die Indizes für die Sicht verloren. Informationen über das Neuerstellen von Indizes finden Sie in SQL Server Books Online.  
  
-   **Löschen eines Objekts** Löschen ein Objekts, beispielsweise eine Spalte, Tabelle oder Sicht, überprüfen Sie zunächst um sicherzustellen, dass das Objekt nicht von einem anderen Objekt in der Datenbank verwiesen wird.  
  
Unabhängig davon, welche Arten von Änderungen Sie am Entwurf der Datenbank vornehmen, sollten Sie jede Änderung protokollieren. Eine Möglichkeit dafür ist das Aufbewahren der SQL-Skripts aller Änderungen, die Sie an der Produktionsdatenbank vornehmen.  
  
## Siehe auch  
[Verwenden von Einschränkungen (Visual Database Tools)](assetId:///637098af-2567-48f8-90f4-b41df059833e)  
[Mehrbenutzerumgebungen & #40; Visual Database Tools & #41;](../content/Multiuser-Environments--Visual-Database-Tools-.md)  
  
