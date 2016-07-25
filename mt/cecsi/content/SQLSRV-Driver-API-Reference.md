---
title: "API-Referenz f&#252;r den SQLSRV-Treiber"
ms.custom: na
ms.date: 06/28/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0b55da26-ddeb-4e89-872a-91e0aba57103
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
# API-Referenz f&#252;r den SQLSRV-Treiber
Der Name der API für den SQLSRV-Treiber in der [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] ist **sqlsrv**. Allee **sqlsrv** -Funktionen beginnen mit **sqlsrv\_** , gefolgt von einem Verb oder einem Substantiv. Die Funktionen, auf die ein Verb folgt, das eine Aktion ausführt und die Funktionen, auf die ein Substantiv folgt, geben Metadaten zurück.  
  
## In diesem Abschnitt  
Der SQLSRV-Treiber enthält die folgenden Funktionen:  
  
|Funktion|Beschreibung|  
|------------|---------------|  
|[sqlsrv\_begin\_transaction](../content/sqlsrv_begin_transaction.md)|beginnt eine Transaktion,|  
|[sqlsrv\_cancel](../content/sqlsrv_cancel.md)|Verwirft eine Aussage; bricht ausstehende Ergebnisse der Aussage ab|  
|[sqlsrv\_client\_info](../content/sqlsrv_client_info.md)|Stellt Informationen über den Client bereit|  
|[sqlsrv\_close](../content/sqlsrv_close.md)|Schließt eine Verbindung Gibt alle der Verbindung zugeordneten Ressourcen frei|  
|[sqlsrv\_commit](../content/sqlsrv_commit.md)|Führt einen Commit für die Transaktion aus.|  
|[sqlsrv\_configure](../content/sqlsrv_configure.md)|Ändert Fehlerbehandlung und Protokollierungskonfigurationen|  
|[sqlsrv\_connect](../content/sqlsrv_connect.md)|Erstellt und öffnet eine Verbindung|  
|[sqlsrv\_errors](../content/sqlsrv_errors.md)|Gibt Informationen über Fehler und\/oder Warnungen für den letzten Vorgang zurück|  
|[sqlsrv\_execute](../content/sqlsrv_execute.md)|Führt eine vorbereitete Anweisung aus|  
|[sqlsrv\_fetch](../content/sqlsrv_fetch.md)|Macht die nächste Datenzeile zum Lesen verfügbar.|  
|[sqlsrv\_fetch\_array](../content/sqlsrv_fetch_array.md)|Gibt die nächste Datenzeile als ein numerisch indiziertes Array, ein assoziatives Array oder beides zurück.|  
|[sqlsrv\_fetch\_object](../content/sqlsrv_fetch_object.md)|Ruft die nächste Datenzeile als Objekt ab.|  
|[sqlsrv\_field\_metadata](../content/sqlsrv_field_metadata.md)|Gibt Metadaten eines Feldes zurück.|  
|[sqlsrv\_free\_stmt](../content/sqlsrv_free_stmt.md)|Schließt eine Anweisung. Gibt alle der Anweisung zugeordneten Ressourcen frei.|  
|[sqlsrv\_get\_config](../content/sqlsrv_get_config.md)|Gibt den Wert der angegebenen Konfigurationseinstellung zurück.|  
|[sqlsrv\_get\_field](../content/sqlsrv_get_field.md)|Ruft ein Feld in der aktuellen Zeile nach Index ab. Der PHP-Rückgabetyp kann angegeben werden.|  
|[sqlsrv_has_rows](../content/sqlsrv_has_rows.md)|Erkennt, ob ein Resultset eine oder mehrere Zeilen hat.|  
|[sqlsrv\_next\_result](../content/sqlsrv_next_result.md)|Stellt das nächste Ergebnis zur Verarbeitung zur Verfügung.|  
|[sqlsrv_num_rows](../content/sqlsrv_num_rows.md)|Berichtet über die Anzahl der Zeilen in einem Resultset.|  
|[sqlsrv\_num\_fields](../content/sqlsrv_num_fields.md)|Ruft die Anzahl der Felder in einem aktiven Resultset ab.|  
|[sqlsrv\_prepare](../content/sqlsrv_prepare.md)|Bereitet eine Transact\-SQL-Abfrage vor, ohne sie auszuführen Bindet implizit die Parameter.|  
|[sqlsrv\_query](../content/sqlsrv_query.md)|Bereitet eine Transact\-SQL-Abfrage vor und führt sie aus|  
|[sqlsrv\_rollback](../content/sqlsrv_rollback.md)|Führt ein Rollback für eine Transaktion aus|  
|[sqlsrv\_rows\_affected](../content/sqlsrv_rows_affected.md)|Gibt die Anzahl der veränderten Zeilen zurück|  
|[sqlsrv\_send\_stream\_data](../content/sqlsrv_send_stream_data.md)|Übermittelt bis zu acht Kilobyte \(8 KB\) Daten mit jedem Aufruf der Funktion an den Server|  
|[sqlsrv\_server\_info](../content/sqlsrv_server_info.md)|Stellt Informationen zum Server bereit|  
  
## Verweis  
[PHP-Handbuch](http://go.microsoft.com/fwlink/?LinkId=105500)  
  
## Siehe auch  
[Übersicht zum PHP-SQL-Treiber](../content/Overview-of-the-PHP-SQL-Driver.md)
[Konstanten&#40;Microsoft-Treiber für PHP für SQL Server&#41;](../content/Constants--Microsoft-Drivers-for-PHP-for-SQL-Server-.md)  
[Programmierhandbuch für den PHP-SQL-Treiber](../content/Programming-Guide-for-PHP-SQL-Driver.md)
[Erste Schritte mit dem PHP-SQL-Treiber](../content/Getting-Started-with-the-PHP-SQL-Driver.md)
  
