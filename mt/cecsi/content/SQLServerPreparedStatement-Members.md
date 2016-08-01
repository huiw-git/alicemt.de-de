---
title: "SQLServerPreparedStatement-Elemente"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2363902f-d4c6-4cd4-a5fc-86079eb9e418
caps.latest.revision: 38
caps.handback.revision: 37
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
# SQLServerPreparedStatement-Elemente
  Die folgenden Tabellen enthalten die Elemente, die von der [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\-Klasse verfügbar gemacht werden.  
  
## Konstruktoren  
 Keine  
  
## Felder  
 Keine  
  
## Geerbte Felder  
  
|Klasse geerbt von:|Methoden|  
|------------------------|--------------|  
|java.sql.Statement|CLOSE\_ALL\_RESULTS, CLOSE\_CURRENT\_RESULT, EXECUTE\_FAILED, KEEP\_CURRENT\_RESULT, NO\_GENERATED\_KEYS, RETURN\_GENERATED\_KEYS, SUCCESS\_NO\_INFO|  
  
## Methoden  
  
|Name|Beschreibung|  
|----------|------------------|  
|[addBatch](../content/addBatch-Method--SQLServerPreparedStatement-.md)|Fügt dem Befehlsbatch für dieses Statement\-Objekt einen Parametersatz hinzu.|  
|[cancel](../content/cancel-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Bricht die SQL\-Anweisung ab, die derzeit von diesem Statement\-Objekt ausgeführt wird.|  
|[clearBatch](../content/clearBatch-Method--SQLServerPreparedStatement-.md)|Leert die aktuelle Liste mit SQL\-Befehlen für dieses [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt.|  
|[clearParameters](../content/clearParameters-Method--SQLServerPreparedStatement-.md)|Löscht umgehend die aktuellen Parameterwerte.|  
|[clearWarnings](../content/clearWarnings-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Löscht alle für dieses Statement\-Objekt gemeldeten Warnungen.|  
|[close](../content/close-Method--SQLServerPreparedStatement-.md)|Gibt die Datenbank\- und JDBC\-Ressourcen dieses Statement\-Objekts umgehend frei, sodass nicht auf deren automatische Freigabe gewartet werden muss.|  
|[execute](../content/execute-Method--SQLServerPreparedStatement-.md)|Führt die SQL\-Anweisung in diesem Statement\-Objekt aus. Hierbei kann es sich um eine beliebige Art von SQL\-Anweisung handeln.|  
|[executeBatch](../content/executeBatch-Method--SQLServerPreparedStatement-.md)|Übermittelt einen Befehlsbatch zur Ausführung an die Datenbank. Werden alle Befehle erfolgreich ausgeführt, wird ein Array mit Updatezählungen zurückgegeben.|  
|[executeQuery](../content/executeQuery-Method--SQLServerPreparedStatement-.md)|Führt die SQL\-Abfrage in diesem Statement\-Objekt aus und gibt das durch die Abfrage generierte [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt zurück.|  
|[executeUpdate](../content/executeUpdate-Method--SQLServerPreparedStatement-.md)|Führt die SQL\-Anweisung in diesem Statement\-Objekt aus. Hierbei muss es sich um eine SQL\-Anweisung vom Typ "INSERT", "UPDATE", "MERGE" oder "DELETE" oder um eine SQL\-Anweisung handeln, von der nichts zurückgegeben wird \(beispielsweise eine DDL\-Anweisung\).|  
|[getConnection](../content/getConnection-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft das [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt ab, von dem dieses Statement\-Objekt erstellt wurde.|  
|[getFetchDirection](../content/getFetchDirection-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft die Richtung zum Abrufen von Zeilen aus Datenbanktabellen ab, die standardmäßig für Resultsets verwendet wird, die auf der Grundlage dieses Statement\-Objekts generiert werden.|  
|[getFetchSize](../content/getFetchSize-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft die Anzahl von Resultsetzeilen ab, bei der es sich um die standardmäßige Abrufgröße für Resultsetobjekte handelt, die auf der Grundlage dieses Statement\-Objekts generiert werden.|  
|[getGeneratedKeys](../content/getGeneratedKeys-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft sämtliche automatisch generierte Schlüssel ab, die aufgrund der Ausführung dieses Statement\-Objekts erstellt werden.|  
|[getMaxFieldSize](../content/getMaxFieldSize-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft die maximale Anzahl von Bytes ab, die für Zeichen\- und Binärspaltenwerte in einem [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt zurückgegeben werden können, das von diesem Statement\-Objekt erstellt wurde.|  
|[getMaxRows](../content/getMaxRows-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft die maximale Anzahl von Zeilen ab, die ein [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt enthalten kann, das von diesem Statement\-Objekt erstellt wurde.|  
|[getMetaData](../content/getMetaData-Method--SQLServerPreparedStatement-.md)|Ruft ein [SQLServerResultSetMetaData-Klasse](../content/SQLServerResultSetMetaData-Class.md)\-Objekt mit Informationen zu den Spalten des [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts ab, das beim Ausführen dieses Statement\-Objekts zurückgegeben wird.|  
|[getMoreResults](../content/getMoreResults-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Wechselt zum nächsten Ergebnis dieses Statement\-Objekts.|  
|[getParameterMetaData](../content/getParameterMetaData-Method--SQLServerPreparedStatement-.md)|Ruft Anzahl, Typ und Eigenschaften der Parameter für dieses Statement\-Objekt ab.|  
|[getResponseBuffering](../content/getResponseBuffering-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft den Antwortpuffermodus für dieses [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt ab.|  
|[getQueryTimeout](../content/getQueryTimeout-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft die Anzahl von Sekunden ab, die von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] auf die Ausführung dieses Statement\-Objekts gewartet wird.|  
|[getResultSet](../content/getResultSet-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft das aktuelle Ergebnis als [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt ab.|  
|[getResultSetConcurrency](../content/getResultSetConcurrency-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft die Resultsetparallelität für [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekte ab, die von diesem Statement\-Objekt generiert werden.|  
|[getResultSetHoldability](../content/getResultSetHoldability-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft die Holdability für Resultsets für [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekte ab, die von diesem Statement\-Objekt generiert werden.|  
|[getResultSetType](../content/getResultSetType-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft den Resultsettyp für [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekte ab, die von diesem Statement\-Objekt generiert werden.|  
|[getUpdateCount](../content/getUpdateCount-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft das aktuelle Ergebnis als Updatezählung ab.|  
|[getWarnings](../content/getWarnings-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft die erste Warnung ab, die von Aufrufen für dieses Statement\-Objekt gemeldet wurde.|  
|[isClosed](../content/isClosed-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Gibt an, ob dieses Statement\-Objekt geschlossen wurde.|  
|[isPoolable](../content/isPoolable-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Gibt einen Wert zurück, durch den angegeben wird, ob dem vom Benutzer bereitgestellten Anwendungspool eine Anweisung hinzugefügt werden kann.|  
|[isWrapperFor](../content/isWrapperFor-Method--SQLServerPreparedStatement-.md)|Gibt an, ob es sich bei diesem Anweisungsobjekt um einen Wrapper für die angegebene Schnittstelle handelt.|  
|[setArray](../content/setArray-Method--SQLServerPreparedStatement-.md)|Legt die angegebene Parameternummer auf das angegebene Array\-Objekt fest.|  
|[setAsciiStream](../content/setAsciiStream-Method--SQLServerPreparedStatement-.md)|Legt die angegebene Parameternummer auf das angegebene InputStream\-Objekt fest.|  
|[setBigDecimal](../content/setBigDecimal-Method--SQLServerPreparedStatement-.md)|Legt die angegebene Parameternummer auf das angegebene BigDecimal\-Objekt fest.|  
|[setBinaryStream](../content/setBinaryStream-Method--SQLServerPreparedStatement-.md)|Legt den angegebenen Parameter auf den angegebenen Eingabedatenstrom fest.|  
|[setBlob](../content/setBlob-Method--SQLServerPreparedStatement-.md)|Legt den angegebenen Parameter auf das angegebene Blob\-Objekt fest.|  
|[setboolean](../content/setBoolean-Method--SQLServerPreparedStatement-.md)|Legt den angegebenen Parameter auf den angegebenen Wert vom Typ **Boolean** fest.|  
|[setByte](../content/setByte-Method--SQLServerPreparedStatement-.md)|Legt den angegebenen Parameter auf den angegebenen Wert vom Typ **byte** fest.|  
|[setBytes](../content/setBytes-Method--SQLServerPreparedStatement-.md)|Legt den angegebenen Parameter auf das angegebene Bytearray fest.|  
|[setCharacterStream](../content/setCharacterStream-Method--SQLServerPreparedStatement-.md)|Legt den angegebenen Parameter auf das angegebene Reader\-Objekt fest.|  
|[setClob](../content/setClob-Method--SQLServerPreparedStatement-.md)|Legt den angegebenen Parameter auf das angegebene Clob\-Objekt fest.|  
|[setCursorName](../content/setCursorName-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Legt den SQL\-Cursornamen auf die angegebene Zeichenfolge fest, die dann für nachfolgende Ausführungsmethoden verwendet wird.|  
|[setDate](../content/setDate-Method--SQLServerPreparedStatement-.md)|Legt den angegebenen Parameter auf den angegebenen Datumswert fest.|  
|[setDateTimeOffset](../content/setDateTimeOffset-Method--SQLServerPreparedStatement-.md)|Legt den Wert der Spalte fest, die für den [DateTimeOffset-Klasse](../content/DateTimeOffset-Class.md)\-Wert angegeben wurde.|  
|[setDouble](../content/setDouble-Method--SQLServerPreparedStatement-.md)|Legt den angegebenen Parameter auf den angegebenen Wert vom Typ **double** fest.|  
|[setEscapeProcessing](../content/setEscapeProcessing-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Legt den Escapeverarbeitungsmodus fest.|  
|[setFetchDirection](../content/setFetchDirection-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Gibt für den JDBC\-Treiber die Richtung an, in der die Resultsetzeilen verarbeitet werden sollen.|  
|[setFetchSize](../content/setFetchSize-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Gibt für den JDBC\-Treiber an, wie viele Zeilen aus der Datenbank abgerufen werden sollen, wenn weitere Zeilen benötigt werden.|  
|[setFloat](../content/setFloat-Method--SQLServerPreparedStatement-.md)|Legt den angegebenen Parameter auf den angegebenen Wert vom Typ **float** fest.|  
|[setInt](../content/setInt-Method--SQLServerPreparedStatement-.md)|Legt den angegebenen Parameter auf den angegebenen Wert vom Typ **int** fest.|  
|[setLong](../content/setLong-Method--SQLServerPreparedStatement-.md)|Legt den angegebenen Parameter auf den angegebenen Wert vom Typ **long** fest.|  
|[setMaxFieldSize](../content/setMaxFieldSize-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Legt das Limit für die maximale Anzahl von Bytes in einer [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Spalte, in der Zeichen\- oder Binärwerte gespeichert werden, auf die angegebene Anzahl von Bytes fest.|  
|[setMaxRows](../content/setMaxRows-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Legt das Limit für die maximale Anzahl von Zeilen, die ein beliebiges [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt enthalten kann, auf die angegebene Anzahl fest.|  
|[setNCharacterStream](../content/setNCharacterStream-Method--SQLServerPreparedStatement-.md)|Legt den angegebenen Parameter auf das angegebene Reader\-Objekt fest.|  
|[setNClob](../content/setNClob-Method--SQLServerPreparedStatement-.md)|Legt den angegebenen Parameter auf das angegebene Objekt fest.|  
|[setNull](../content/setNull-Method--SQLServerPreparedStatement-.md)|Legt den angegebenen Parameter unter Berücksichtigung des festzulegenden Parametertyps auf einen NULL\-Wert fest.|  
|[setNString](../content/setNString-Method--int--java.lang.String-.md)|Legt den angegebenen Parameter auf das angegebene **String**\-Objekt fest.|  
|[setObject](../content/setObject-Method--SQLServerPreparedStatement-.md)|Legt den Wert des angegebenen Parameters unter Verwendung des angegebenen Objekts fest.|  
|[setPoolable](../content/setPoolable-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Sendet eine Anforderung, dass dem Pool eine Anweisung hinzugefügt bzw. nicht hinzugefügt werden soll. Standardmäßig kann ein SQLServerPreparedStatement\-Objekt beim Erstellen einem Pool hinzugefügt werden.|  
|[setQueryTimeout](../content/setQueryTimeout-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Legt die Anzahl von Sekunden, die vom Treiber auf die Ausführung eines Statement\-Objekts gewartet wird, auf die angegebene Anzahl von Sekunden fest.|  
|[setRef](../content/setRef-Method--SQLServerPreparedStatement-.md)|Legt den angegebenen Parameter auf das angegebene Ref\-Objekt fest.|  
|[setResponseBuffering](../content/setResponseBuffering-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Legt den Antwortpuffermodus für dieses [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt auf **String full** oder auf **adaptive** \(jeweils ohne Berücksichtigung der Groß\- und Kleinschreibung\) fest.|  
|[setShort](../content/setShort-Method--SQLServerPreparedStatement-.md)|Legt den angegebenen Parameter auf den angegebenen Wert vom Typ **short** fest.|  
|[setString](../content/setString-Method--SQLServerPreparedStatement-.md)|Legt den angegebenen Parameter auf den angegebenen Wert vom Typ **String** fest.|  
|[setSQLXML](../content/setSQLXML-Method--SQLServerPreparedStatement-.md)|Legt den angegebenen Parameter auf das angegebene **SQLXML**\-Objekt fest.|  
|[setTime](../content/setTime-Method--SQLServerPreparedStatement-.md)|Legt den angegebenen Parameter auf den angegebenen Uhrzeitwert fest.|  
|[setTimestamp](../content/setTimestamp-Method--SQLServerPreparedStatement-.md)|Legt den angegebenen Parameter auf den angegebenen Zeitstempelwert fest.|  
|[setUnicodeStream](../content/setUnicodeStream-Method--SQLServerPreparedStatement-.md)|Legt die angegebene Parameternummer auf den angegebenen Eingabedatenstrom mit der angegebenen Anzahl von Bytes fest.|  
|[setURL](../content/setURL-Method--SQLServerPreparedStatement-.md)|Legt den angegebenen Parameter auf den angegebenen URL\-Wert fest.|  
|[unwrap](../content/unwrap-Method--SQLServerPreparedStatement-.md)|Gibt ein Objekt zurück, das die angegebene Schnittstelle implementiert, um den Zugriff auf die [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-spezifischen Methoden zu ermöglichen.|  
  
## Geerbte Methoden  
  
|Klasse geerbt von:|Methoden|  
|------------------------|--------------|  
|com.microsoft.sqlserver.jdbc.SQLServerStatement|cancel, clearWarnings, execute, executeUpdate, getConnection, getFetchDirection, getFetchSize, getGeneratedKeys, getMaxFieldSize, getMaxRows, getMoreResults, getQueryTimeout, getResultSet, getResultSetConcurrency, getResultSetHoldability, getResultSetType, getUpdateCount, getWarnings, isPoolable, setCursorName, setEscapeProcessing, setFetchDirection, setFetchSize, setMaxFieldSize, setMaxRows, setPoolable, setQueryTimeout|  
|java.lang.Object|clone, equals, getClass, hashCode, notify, notifyAll, toString, wait|  
|java.sql.Statement|cancel, clearWarnings, execute, executeUpdate, getConnection, getFetchDirection, getFetchSize, getGeneratedKeys, getMaxFieldSize, getMaxRows, getMoreResults, getQueryTimeout, getResultSet, getResultSetConcurrency, getResultSetHoldability, getResultSetType, getUpdateCount, getWarnings, setCursorName, setEscapeProcessing, setFetchDirection, setFetchSize, setMaxFieldSize, setMaxRows, setQueryTimeout|  
|java.sql.Wrapper|isWrapperFor, unwrap|  
  
## Siehe auch  
 [SQLServerPreparedStatement-Klasse](../content/SQLServerPreparedStatement-Class.md)  
  
  