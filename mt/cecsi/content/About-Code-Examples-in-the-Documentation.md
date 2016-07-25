---
title: "Informationen zu den Codebeispielen in der Dokumentation"
ms.custom: na
ms.date: 06/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3f035c37-0f2e-47d4-94e0-a10774402e82
caps.latest.revision: 31
caps.handback.revision: 30
manager: jhubbard
translation.priority.ht: 
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
# Informationen zu den Codebeispielen in der Dokumentation
Es gibt einige Punkte zu beachten, wenn Sie die Codebeispiele in der [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] -Dokumentation ausführen:  
  
-   In fast allen Beispielen wird davon ausgegangen, dass SQL Server 2005 oder höher \(SQL Server 2008 oder höher bei Version 3.1\) und die AdventureWorks-Datenbank auf dem lokalen Computer installiert sind.  
  
    Informationen zur Vorgehensweise beim Herunterladen der kostenlosen Editionen und Testversionen von SQL Server finden Sie unter [SQL Server](http://go.microsoft.com/fwlink/?LinkID=120193).  
  
    Informationen zum Herunterladen der AdventureWorks-Datenbank finden Sie unter [Microsoft SQL Server-Beispiele und Communityprojekte](http://go.microsoft.com/fwlink/?LinkID=67739).  
  
    Weitere Informationen zum Installieren der AdventureWorks-Datenbank finden Sie unter [Anleitung: Installieren der AdventureWorks-Datenbank](http://go.microsoft.com/fwlink/?LinkID=65819).  
  
-   Fast alle Codebeispiele in dieser Dokumentation sollen über die Befehlszeile ausgeführt werden, die das automatische Testen aller Codebeispiele ermöglicht. Informationen über das Ausführen von PHP über die Befehlszeile finden Sie unter [PHP über die Befehlszeile](http://php.net/manual/en/features.commandline.php).  
  
-   Obwohl Beispiele dafür geschrieben sind, von der Befehlszeile ausgeführt zu werden, kann jedes Beispiel auch ausgeführt werden, indem Sie es in einem Browser aufrufen, ohne Änderungen am Skript vorzunehmen. Um eine schöne Formatierung der Ausgabe zu erzielen, ersetzen Sie in jedem Beispiel jedes "\\n" durch „<\/br>“, bevor Sie es in einem Browser aufrufen.  
  
-   Um jedes Beispiel auf das Wesentliche zu beschränken, wird die richtige Fehlerbehandlung nicht in allen Beispielen durchgeführt. Es wird empfohlen, dass jeder Aufruf einer **sqlsrv** -Funktion oder PDO-Methode auf Fehler überprüft wird und gemäß den Anforderungen der Anwendung behandelt wird.  
  
    Eine einfache Möglichkeit, Fehlerinformationen abzurufen, wenn ein Fehler aufgetreten ist, ist das Beenden des Skripts mit der folgenden Codezeile:  
  
    ```  
    die( print_r( sqlsrv_errors(), true));  
    ```  
  
    Oder falls Sie PDO verwenden,  
  
    ```  
    print_r ($stmt->errorInfo());  
    die();  
    ```  
  
    Weitere Informationen zum Behandeln von Fehlern und Warnungen finden Sie unter [Handhabung von Fehlern und Warnungen](../content/Handling-Errors-and-Warnings.md).  
  
## Siehe auch  
[Übersicht zum PHP-SQL-Treiber](../content/Overview-of-the-PHP-SQL-Driver.md)
  
