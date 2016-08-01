---
title: "SQLServerStatement-Elemente"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 828cbaa9-ea7a-4986-95c3-5ba0d7d01d83
caps.latest.revision: 28
caps.handback.revision: 27
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
  - sv-se
  - zh-cn
  - zh-tw
---
# SQLServerStatement-Elemente
  Die folgenden Tabellen enthalten die Elemente, die von der [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Klasse verfügbar gemacht werden.  
  
## Konstruktoren  
 Keine  
  
## Felder  
 Keine  
  
## Geerbte Felder  
  
|Name|Beschreibung|  
|----------|------------------|  
|java.sql.Statement|CLOSE\_ALL\_RESULTS, CLOSE\_CURRENT\_RESULT, EXECUTE\_FAILED, KEEP\_CURRENT\_RESULT, NO\_GENERATED\_KEYS, RETURN\_GENERATED\_KEYS, SUCCESS\_NO\_INFO|  
  
## Methoden  
  
|Name|Beschreibung|  
|----------|------------------|  
|[addBatch](../content/addBatch-Method--SQLServerStatement-.md)|Fügt den angegebenen SQL\-Befehl der aktuellen Liste mit Befehlen für dieses [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt hinzu.|  
|[cancel](../content/cancel-Method--SQLServerStatement-.md)|Bricht die SQL\-Anweisung ab, die derzeit von diesem [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt ausgeführt wird.|  
|[clearBatch](../content/clearBatch-Method--SQLServerStatement-.md)|Leert die aktuelle Liste mit SQL\-Befehlen für dieses [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt.|  
|[clearWarnings](../content/clearWarnings-Method--SQLServerStatement-.md)|Löscht alle für dieses [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt gemeldeten Warnungen.|  
|[close](../content/close-Method--SQLServerStatement-.md)|Gibt die Datenbank\- und JDBC\-Ressourcen dieses [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekts umgehend frei, sodass nicht auf deren automatische Freigabe gewartet werden muss.|  
|[execute](../content/execute-Method--SQLServerStatement-.md)|Führt die angegebene SQL\-Anweisung aus. Hierbei können mehrere Ergebnisse zurückgegeben werden.|  
|[executeBatch](../content/executeBatch-Method--SQLServerStatement-.md)|Übermittelt einen Befehlsbatch zur Ausführung an die Datenbank. Werden alle Befehle erfolgreich ausgeführt, wird ein Array mit Updatezählungen zurückgegeben.|  
|[executeQuery](../content/executeQuery-Method--SQLServerStatement-.md)|Führt die angegebene SQL\-Anweisung aus und gibt ein einzelnes [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt zurück.|  
|[executeUpdate](../content/executeUpdate-Method--SQLServerStatement-.md)|Führt die angegebene SQL\-Anweisung aus. Hierbei kann es sich um eine Anweisung vom Typ "INSERT", "UPDATE", "MERGE" oder "DELETE" oder um eine SQL\-Anweisung handeln, von der nichts zurückgegeben wird \(beispielsweise eine SQL\-DDL\-Anweisung\).|  
|[getConnection](../content/getConnection-Method--SQLServerStatement-.md)|Ruft das [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt ab, von dem dieses [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt erstellt wurde.|  
|[getFetchDirection](../content/getFetchDirection-Method--SQLServerStatement-.md)|Ruft die Richtung zum Abrufen von Zeilen aus Datenbanktabellen ab, die standardmäßig für Resultsets verwendet wird, die auf der Grundlage dieses [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekts generiert werden.|  
|[getFetchSize](../content/getFetchSize-Method--SQLServerStatement-.md)|Ruft die Anzahl von Resultsetzeilen ab, bei der es sich um die standardmäßige Abrufgröße für Resultsetobjekte handelt, die auf der Grundlage dieses [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekts generiert werden.|  
|[getGeneratedKeys](../content/getGeneratedKeys-Method--SQLServerStatement-.md)|Ruft sämtliche automatisch generierte Schlüssel ab, die aufgrund der Ausführung dieses [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekts erstellt werden.|  
|[getMaxFieldSize](../content/getMaxFieldSize-Method--SQLServerStatement-.md)|Ruft die maximale Anzahl von Bytes ab, die für Zeichen\- und Binärspaltenwerte in einem [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt zurückgegeben werden können, das von diesem [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt erstellt wird.|  
|[getMaxRows](../content/getMaxRows-Method--SQLServerStatement-.md)|Ruft die maximale Anzahl von Zeilen ab, die ein [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt enthalten kann, das von diesem [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt erstellt wird.|  
|[getMoreResults](../content/getMoreResults-Method--SQLServerStatement-.md)|Wechselt zum nächsten Ergebnis dieses [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekts.|  
|[getQueryTimeout](../content/getQueryTimeout-Method--SQLServerStatement-.md)|Ruft die Anzahl von Sekunden ab, die von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] auf die Ausführung dieses [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekts gewartet wird.|  
|[getResponseBuffering](../content/getResponseBuffering-Method--SQLServerStatement-.md)|Ruft den Antwortpuffermodus für dieses [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt ab.|  
|[getResultSet](../content/getResultSet-Method--SQLServerStatement-.md)|Ruft das aktuelle Ergebnis als [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt ab.|  
|[getResultSetConcurrency](../content/getResultSetConcurrency-Method--SQLServerStatement-.md)|Ruft die Resultsetparallelität für [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekte ab, die von diesem [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt generiert werden.|  
|[getResultSetHoldability](../content/getResultSetHoldability-Method--SQLServerStatement-.md)|Ruft die Holdability für Resultsets für [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekte ab, die von diesem [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt generiert werden.|  
|[getResultSetType](../content/getResultSetType-Method--SQLServerStatement-.md)|Ruft den Resultsettyp für [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekte ab, die von diesem [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt generiert werden.|  
|[getUpdateCount](../content/getUpdateCount-Method--SQLServerStatement-.md)|Ruft das aktuelle Ergebnis als Updatezählung ab.|  
|[getWarnings](../content/getWarnings-Method--SQLServerStatement-.md)|Ruft die erste Warnung ab, die von Aufrufen für dieses [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt gemeldet wurde.|  
|[isClosed](../content/isClosed-Method--SQLServerStatement-.md)|Gibt an, ob dieses [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt geschlossen wurde.|  
|[isPoolable](../content/isPoolable-Method--SQLServerStatement-.md)|Gibt einen Wert zurück, durch den angegeben wird, ob dem vom Benutzer bereitgestellten Anwendungspool eine Anweisung hinzugefügt werden kann.|  
|[isWrapperFor](../content/isWrapperFor-Method--SQLServerStatement-.md)|Gibt an, ob es sich bei diesem Anweisungsobjekt um einen Wrapper für die angegebene Schnittstelle handelt.|  
|[setCursorName](../content/setCursorName-Method--SQLServerStatement-.md)|Legt den SQL\-Cursornamen auf die angegebene Zeichenfolge fest, die dann für nachfolgende Ausführungsmethoden verwendet wird.|  
|[setEscapeProcessing](../content/setEscapeProcessing-Method--SQLServerStatement-.md)|Legt den Escapeverarbeitungsmodus fest.|  
|[setFetchDirection](../content/setFetchDirection-Method--SQLServerStatement-.md)|Gibt für den JDBC\-Treiber die Richtung an, in der die Resultsetzeilen verarbeitet werden sollen.|  
|[setFetchSize](../content/setFetchSize-Method--SQLServerStatement-.md)|Gibt für den JDBC\-Treiber an, wie viele Zeilen aus der Datenbank abgerufen werden sollen, wenn weitere Zeilen benötigt werden.|  
|[setMaxFieldSize](../content/setMaxFieldSize-Method--SQLServerStatement-.md)|Legt das Limit für die maximale Anzahl von Bytes in einer [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Spalte, in der Zeichen\- oder Binärwerte gespeichert werden, auf die angegebene Anzahl von Bytes fest.|  
|[setMaxRows](../content/setMaxRows-Method--SQLServerStatement-.md)|Legt das Limit für die maximale Anzahl von Zeilen, die ein beliebiges [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt enthalten kann, auf die angegebene Anzahl fest.|  
|[setPoolable](../content/setPoolable-Method--SQLServerStatement-.md)|Sendet eine Anforderung, dass dem Pool eine Anweisung hinzugefügt bzw. nicht hinzugefügt werden soll.|  
|[setQueryTimeout](../content/setQueryTimeout-Method--SQLServerStatement-.md)|Legt die Anzahl von Sekunden, die vom Treiber auf die Ausführung eines [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekts gewartet wird, auf die angegebene Anzahl von Sekunden fest.|  
|[setResponseBuffering](../content/setResponseBuffering-Method--SQLServerStatement-.md)|Legt den Antwortpuffermodus für dieses [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt auf **String full** oder auf **adaptive** \(jeweils ohne Berücksichtigung der Groß\-\/Kleinschreibung\) fest.|  
|[unwrap](../content/unwrap-Method--SQLServerStatement-.md)|Gibt ein Objekt zurück, das die angegebene Schnittstelle implementiert, um den Zugriff auf die [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-spezifischen Methoden zu ermöglichen.|  
  
## Geerbte Methoden  
  
|Klasse geerbt von:|Methoden|  
|------------------------|--------------|  
|java.lang.Object|clone, equals, getClass, hashCode, notify, notifyAll, toString, wait|  
|java.sql.Wrapper|isWrapperFor, unwrap|  
  
## Siehe auch  
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  