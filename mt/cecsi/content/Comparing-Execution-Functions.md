---
title: "Vergleichen von Ausf&#252;hrungsfunktionen"
ms.custom: na
ms.date: 06/28/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 130fc0fd-87dd-46b2-918f-de9dc572c769
caps.latest.revision: 18
caps.handback.revision: 17
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
# Vergleichen von Ausf&#252;hrungsfunktionen
[!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] bietet mehrere Optionen zum Ausführen von Funktionen.  
  
Wenn Sie den SQLSRV-Treiber verwenden, verwenden Sie [sqlsrv_query](../content/sqlsrv_query.md) zum Ausführen einer einzelnen Abfrage und [sqlsrv_prepare](../content/sqlsrv_prepare.md) mit [sqlsrv_execute](../content/sqlsrv_execute.md) zur mehrfachen Ausführung einer vorbereiteten Anweisung mit verschiedenen Parameterwerten für jede Ausführung.  
  
Wenn Sie den PDO\_SQLSRV-Treiber verwenden, können Sie eine Abfrage mit einer der folgenden Methoden ausführen:  
  
-   [PDO::exec](../Topic/PDO::exec.md)  
  
-   [PDO::query](../Topic/PDO::query.md)  
  
-   [PDO::prepare](../Topic/PDO::prepare.md) und [PDOStatement::execute](../Topic/PDOStatement::execute.md).  
  
## Siehe auch  
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
[Referenz zum Treiber PDO_SQLSRV](../content/PDO_SQLSRV-Driver-Reference.md)  
[Programmierhandbuch für den PHP-SQL-Treiber](../content/Programming-Guide-for-PHP-SQL-Driver.md)
  
