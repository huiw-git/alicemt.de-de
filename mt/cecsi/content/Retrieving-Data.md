---
title: "Abrufen von Daten"
ms.custom: na
ms.date: 06/16/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3414992c-61c0-4e7d-b509-72517e52c1bb
caps.latest.revision: 42
caps.handback.revision: 41
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
# Abrufen von Daten
Dieses Thema und die anderen Themen in diesem Abschnitt erläutern, wie Sie Daten abrufen können.  
  
## SQLSRV-Treiber  
Der SQLSRV-Treiber des [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] bietet die folgenden Optionen zum Abrufen von Daten aus einem Resultset:  
  
-   [sqlsrv_fetch_array](../content/sqlsrv_fetch_array.md)  
  
-   [sqlsrv_fetch_object](../content/sqlsrv_fetch_object.md)  
  
-   [sqlsrv_fetch](../content/sqlsrv_fetch.md)\/[sqlsrv_get_field](../content/sqlsrv_get_field.md)  
  
> [!NOTE]  
> Legen Sie bei Verwendung einer der oben genannten Funktionen keine Null-Vergleiche als Kriterium für das Beenden von Schleifen fest. Da **sqlsrv** -Funktionen „false“ zurückgeben, wenn ein Fehler auftritt, kann folgender Code nach einem Fehler in [sqlsrv_fetch_array](../content/sqlsrv_fetch_array.md)zu einer Endlosschleife führen:  
>   
> `/*``This code could result in an infinite loop. It is recommended that`  
>   
> `you do NOT use null comparisons as the criterion for exiting loops,`  
>   
> `as is done here. */`  
>   
> `do{`  
>   
> `$result = sqlsrv_fetch_array($stmt);`  
>   
> `} while( !is_null($result));`  
  
Wenn Ihre Abfrage mehr als ein Resultset abruft, können Sie das nächste Resultset mit [sqlsrv_next_result](../content/sqlsrv_next_result.md)anzeigen.  
  
Ab Version 1.1 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] können Sie [sqlsrv\_has\_rows](../content/sqlsrv_has_rows.md) verwenden, um zu überprüfen, ob ein Resultset Zeilen enthält.  
  
## PDO\_SQLSRV-Treiber  
Der PDO\_SQLSRV-Treiber des [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] bietet die folgenden Optionen zum Abrufen von Daten aus einem Resultset:  
  
-   [PDOStatement::fetch](../Topic/PDOStatement::fetch.md)  
  
-   [PDOStatement::fetchAll](../Topic/PDOStatement::fetchAll.md)  
  
-   [PDOStatement::fetchColumn](../Topic/PDOStatement::fetchColumn.md)  
  
-   [PDOStatement::fetchObject](../Topic/PDOStatement::fetchObject.md)  
  
Wenn Ihre Abfrage mehr als ein Resultset abruft, können Sie das nächste Resultset mit [PDOStatement::nextRowset](../Topic/PDOStatement::nextRowset.md)anzeigen.  
  
Sie können sehen, wie viele Zeilen ein Resultset aufweist, indem Sie einen bildlauffähigen Cursor verwenden und anschließend [PDOStatement::rowCount](../Topic/PDOStatement::rowCount.md)aufrufen.  
  
[PDO::prepare](../Topic/PDO::prepare.md) ermöglicht die Angabe ein Cursortyps. Anschließend können Sie mit [PDOStatement::fetch](../Topic/PDOStatement::fetch.md) eine Zeile auswählen. Unter [PDO::prepare](../Topic/PDO::prepare.md) finden Sie ein Beispiel und weitere Informationen.  
  
## In diesem Abschnitt  
  
|Thema|Beschreibung|  
|---------|---------------|  
|[Abrufen von Daten als Stream](../content/Retrieving-Data-as-a-Stream-Using-the-SQLSRV-Driver.md)|Bietet einen Überblick über das Streamen von Daten vom Server und stellt Links für spezifische Anwendungsszenarien bereit.|  
|[Verwenden direktionaler Parameter](../content/Using-Directional-Parameters.md)|Beschreibt die Verwendung direktionaler Parameter beim Aufrufen einer gespeicherten Prozedur.|  
|[Festlegen eines Cursortyps und Zeilenauswahl](../content/Specifying-a-Cursor-Type-and-Selecting-Rows.md)|Veranschaulicht, wie bei Verwendung des SSQLSRV-Treibers ein Resultset mit Zeilen erstellen, auf die Sie in beliebiger Reihenfolge zugreifen können.|  
|[Vorgehensweise: Datums- und Uhrzeittypen mittels des SQLSRV-Treibers als Zeichenfolgen abrufen ](../Topic/How%20to:%20Retrieve%20Date%20and%20Time%20Type%20as%20Strings%20Using%20the%20SQLSRV%20Driver.md)|Beschreibt, wie Sie Datums- und Uhrzeittypen als Zeichenfolgen abrufen|  
  
## Verwandte Abschnitte  
[Vorgehensweise: PHP-Datentypen festlegen](../Topic/How%20to:%20Specify%20PHP%20Data%20Types.md)  
  
## Siehe auch  
[Programmierhandbuch für den PHP-SQL-Treiber](../content/Programming-Guide-for-PHP-SQL-Driver.md)
[Abrufen von Daten](../content/Retrieving-Data.md)  
  
