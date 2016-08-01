---
title: "SQLServerCallableStatement-Elemente"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apitype: Assembly
ms.assetid: 5ebdc186-e50f-4d14-bbf4-95af5051e4a4
caps.latest.revision: 50
caps.handback.revision: 49
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
# SQLServerCallableStatement-Elemente
  Die folgenden Tabellen enthalten die Elemente, die von der [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Klasse verfügbar gemacht werden.  
  
## Konstruktoren  
 Keine  
  
## Felder  
  
|Klasse geerbt von:|Methoden|  
|------------------------|--------------|  
|java.sql.Statement|CLOSE\_ALL\_RESULTS, CLOSE\_CURRENT\_RESULT, EXECUTE\_FAILED, KEEP\_CURRENT\_RESULT, NO\_GENERATED\_KEYS, RETURN\_GENERATED\_KEYS, SUCCESS\_NO\_INFO|  
  
## Geerbte Felder  
 Keine  
  
## Methoden  
  
|Name|Beschreibung|  
|----------|------------------|  
|[addBatch](../content/addBatch-Method--SQLServerPreparedStatement-.md)|\(Geerbt von [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md).\) Fügt dem Befehlsbatch für dieses CallableStatement\-Objekt einen Parametersatz hinzu.|  
|[cancel](../content/cancel-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Bricht die SQL\-Anweisung ab, die derzeit von diesem CallableStatement\-Objekt ausgeführt wird.|  
|[clearBatch](../content/clearBatch-Method--SQLServerPreparedStatement-.md)|\(Geerbt von [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md).\) Leert die aktuelle Liste mit SQL\-Befehlen für dieses CallableStatement\-Objekt.|  
|[clearParameters](../content/clearParameters-Method--SQLServerPreparedStatement-.md)|\(Geerbt von [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md).\) Löscht umgehend die aktuellen Parameterwerte.|  
|[clearWarnings](../content/clearWarnings-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Löscht alle für dieses CallableStatement\-Objekt gemeldeten Warnungen.|  
|[close](../content/close-Method--SQLServerPreparedStatement-.md)|\(Geerbt von [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md).\) Gibt die Datenbank\- und JDBC\-Ressourcen dieses CallableStatement\-Objekts umgehend frei, sodass nicht auf deren automatische Freigabe gewartet werden muss.|  
|[execute](../content/execute-Method--SQLServerPreparedStatement-.md)|\(Geerbt von [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md).\) Führt die SQL\-Anweisung in diesem CallableStatement\-Objekt aus. Hierbei kann es sich um eine beliebige Art von SQL\-Anweisung handeln.|  
|[executeBatch](../content/executeBatch-Method--SQLServerPreparedStatement-.md)|\(Geerbt von [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md).\) Übermittelt einen Befehlsbatch zur Ausführung an die Datenbank. Werden alle Befehle erfolgreich ausgeführt, wird ein Array mit Updatezählungen zurückgegeben.|  
|[executeQuery](../content/executeQuery-Method--SQLServerPreparedStatement-.md)|\(Geerbt von [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md).\) Führt die SQL\-Abfrage in diesem CallableStatement\-Objekt aus und gibt das durch die Abfrage generierte [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt zurück.|  
|[executeUpdate](../content/executeUpdate-Method--SQLServerPreparedStatement-.md)|\(Geerbt von [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md).\) Führt die SQL\-Anweisung in diesem CallableStatement\-Objekt aus. Hierbei muss es sich um eine SQL\-Anweisung vom Typ "INSERT", "UPDATE", "MERGE" oder "DELETE" oder um eine SQL\-Anweisung handeln, von der nichts zurückgegeben wird \(beispielsweise eine DDL\-Anweisung\).|  
|[getConnection](../content/getConnection-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft das [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt ab, von dem dieses CallableStatement\-Objekt erstellt wurde.|  
|[getDateTimeOffset](../content/getDateTimeOffset-Method--SQLServerCallableStatement-.md)|Ruft den Wert der angegebenen Spalte als [DateTimeOffset-Klasse](../content/DateTimeOffset-Class.md)\-Objekt ab.|  
|[getFetchDirection](../content/getFetchDirection-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft die Richtung zum Abrufen von Zeilen aus Datenbanktabellen ab, die standardmäßig für Resultsets verwendet wird, die auf der Grundlage dieses CallableStatement\-Objekts generiert werden.|  
|[getFetchSize](../content/getFetchSize-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft die Anzahl von Resultsetzeilen ab, bei der es sich um die standardmäßige Abrufgröße für Resultsetobjekte handelt, die auf der Grundlage dieses CallableStatement\-Objekts generiert werden.|  
|[getGeneratedKeys](../content/getGeneratedKeys-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft sämtliche automatisch generierte Schlüssel ab, die aufgrund der Ausführung dieses CallableStatement\-Objekts erstellt werden.|  
|[getMaxFieldSize](../content/getMaxFieldSize-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft die maximale Anzahl von Bytes ab, die für Zeichen\- und Binärspaltenwerte in einem [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt zurückgegeben werden können, das von diesem CallableStatement\-Objekt erstellt wurde.|  
|[getMaxRows](../content/getMaxRows-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft die maximale Anzahl von Zeilen ab, die ein [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt enthalten kann, das von diesem CallableStatement\-Objekt erstellt wurde.|  
|[getMetaData](../content/getMetaData-Method--SQLServerPreparedStatement-.md)|\(Geerbt von [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md).\) Ruft ein [SQLServerResultSetMetaData-Klasse](../content/SQLServerResultSetMetaData-Class.md)\-Objekt mit Informationen zu den Spalten des [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts ab, das beim Ausführen dieses CallableStatement\-Objekts zurückgegeben wird.|  
|[getMoreResults](../content/getMoreResults-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Wechselt zum nächsten Ergebnis dieses CallableStatement\-Objekts.|  
|[getParameterMetaData](../content/getParameterMetaData-Method--SQLServerPreparedStatement-.md)|\(Geerbt von [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md).\) Ruft Anzahl, Typ und Eigenschaften der Parameter für dieses CallableStatement\-Objekt ab.|  
|[getArray](../content/getArray-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen Parameters als Array\-Objekt ab.|  
|[getAsciiStream](../content/getAsciiStream-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen Parameters als **ASCII**\-Zeichendatenstrom ab.|  
|[getBigDecimal](../content/getBigDecimal-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen Parameters als "java.math.BigDecimal" ab.|  
|[getBinaryStream](../content/getBinaryStream-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen Parameters als Binärdatenstrom mit unterbrechungsfreien Bytes ab.|  
|[getBlob](../content/getBlob-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen JDBC\-Blob\-Parameters als Blob\-Objekt in der Programmiersprache Java ab.|  
|[getboolean](../content/getBoolean-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen Parameters als Wert vom Typ **Boolean** ab.|  
|[getByte](../content/getByte-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen Parameters als Wert vom Typ **byte** ab.|  
|[getBytes](../content/getBytes-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen Parameters als Bytearray ab.|  
|[getCharacterStream](../content/getCharacterStream-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen Parameters als java.io.Reader\-Objekt ab.|  
|[getClob](../content/getClob-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen JDBC\-Blob\-Parameters als Clob\-Objekt in der Programmiersprache Java ab.|  
|[getDate](../content/getDate-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen Parameters als java.sql.Date\-Objekt in der Programmiersprache Java ab.|  
|[getDateTimeOffset](../content/getDateTimeOffset-Method--SQLServerCallableStatement-.md)|Ruft den Wert der angegebenen Spalte als [DateTimeOffset-Klasse](../content/DateTimeOffset-Class.md)\-Objekt ab.|  
|[getDouble](../content/getDouble-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen Parameters als Wert vom Typ **double** in der Programmiersprache Java ab.|  
|[getFloat](../content/getFloat-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen Parameters als Wert vom Typ **float** in der Programmiersprache Java ab.|  
|[getInt](../content/getInt-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen Parameters als Wert vom Typ **int** in der Programmiersprache Java ab.|  
|[getLong](../content/getLong-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen Parameters als Wert vom Typ **long** in der Programmiersprache Java ab.|  
|[getNCharacterStream](../content/getNCharacterStream-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen Parameters als Reader\-Objekt ab.|  
|[getNClob](../content/getNClob-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen JDBC\-**NCLOB**\-Parameters als **NClob**\-Objekt in der Programmiersprache Java ab.|  
|[getNString](../content/getNString-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen Parameters vom Typ **NCHAR**, **NVARCHAR** oder **LONGNVARCHAR** als String in der Programmiersprache Java ab.|  
|[getObject](../content/getObject-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen Parameters als Objekt in der Programmiersprache Java ab.|  
|[getQueryTimeout](../content/getQueryTimeout-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft die Anzahl von Sekunden ab, die von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] auf die Ausführung dieses CallableStatement\-Objekts gewartet wird.|  
|[getRef](../content/getRef-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen Parameters als Ref\-Objekt in der Programmiersprache Java ab.|  
|[getResponseBuffering](../content/getResponseBuffering-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft den Antwortpuffermodus für dieses [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt ab.|  
|[getResultSet](../content/getResultSet-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft das aktuelle Ergebnis als [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt ab.|  
|[getResultSetConcurrency](../content/getResultSetConcurrency-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft die Resultsetparallelität für [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekte ab, die von diesem CallableStatement\-Objekt generiert werden.|  
|[getResultSetHoldability](../content/getResultSetHoldability-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft die Resultsethaltbarkeit für [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekte ab, die von diesem CallableStatement\-Objekt generiert werden.|  
|[getResultSetType](../content/getResultSetType-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft den Resultsettyp für [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekte ab, die von diesem CallableStatement\-Objekt generiert werden.|  
|[getShort](../content/getShort-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen Parameters als Wert vom Typ **short** in der Programmiersprache Java ab.|  
|[getString](../content/getString-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen Parameters als Wert vom Typ **String** in der Programmiersprache Java ab.|  
|[getSQLXML](../content/getSQLXML-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen Parameters als java.sql.SQLXML\-Objekt ab.|  
|[getTime](../content/getTime-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen Parameters als java.sql.Time\-Objekt in der Programmiersprache Java ab.|  
|[getTimestamp](../content/getTimestamp-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen Parameters als java.sql.Timestamp\-Objekt in der Programmiersprache Java ab.|  
|[getUpdateCount](../content/getUpdateCount-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft das aktuelle Ergebnis als Updatezählung ab.|  
|[getURL](../content/getURL-Method--SQLServerCallableStatement-.md)|Ruft den Wert des angegebenen Parameters als URL\-Objekt in der Programmiersprache Java ab.|  
|[getWarnings](../content/getWarnings-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Ruft die erste Warnung ab, die von Aufrufen für dieses CallableStatement\-Objekt gemeldet wurde.|  
|[isClosed](../content/isClosed-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Gibt an, ob dieses Statement\-Objekt geschlossen wurde.|  
|[isPoolable](../content/isPoolable-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Gibt einen Wert zurück, durch den angegeben wird, ob dem vom Benutzer bereitgestellten Anwendungspool eine Anweisung hinzugefügt werden kann.|  
|[isWrapperFor](../content/isWrapperFor-Method--SQLServerCallableStatement-.md)|Gibt an, ob es sich bei diesem Anweisungsobjekt um einen Wrapper für die angegebene Schnittstelle handelt.|  
|[registerOutParameter](../content/registerOutParameter-Method--SQLServerCallableStatement-.md)|Registriert den OUT\-Parameter.|  
|[setArray](../content/setArray-Method--SQLServerPreparedStatement-.md)|\(Geerbt von [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md).\) Legt die angegebene Parameternummer auf das angegebene Array\-Objekt fest.|  
|[setAsciiStream](../content/setAsciiStream--SQLServerCallableStatement-.md)|Legt den angegebenen Parameter auf den angegebenen Eingabedatenstrom fest.|  
|[setBigDecimal](../content/setBigDecimal-Method--SQLServerCallableStatement-.md)|Legt die angegebene Parameternummer auf das angegebene BigDecimal\-Objekt fest.|  
|[setBinaryStream](../content/setBinaryStream--SQLServerCallableStatement-.md)|Legt den angegebenen Parameter auf den angegebenen Eingabedatenstrom fest.|  
|[setBlob](../content/setBlob-Method--SQLServerPreparedStatement-.md)|\(Geerbt von [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md).\) Legt den angegebenen Parameter auf das angegebene Blob\-Objekt fest.|  
|[setboolean](../content/setBoolean-Method--SQLServerCallableStatement-.md)|Legt den angegebenen Parameter auf den angegebenen Wert vom Typ **Boolean** fest.|  
|[setByte](../content/setByte-Method--SQLServerCallableStatement-.md)|Legt den angegebenen Parameter auf den angegebenen Wert vom Typ **byte** fest.|  
|[setBytes](../content/setBytes-Method--SQLServerCallableStatement-.md)|Legt den angegebenen Parameter auf das angegebene Array von **byte**\-Werten fest.|  
|[setCharacterStream](../content/setCharacterStream-Method--SQLServerCallableStatement-.md)|Legt den angegebenen Parameter auf das angegebene Reader\-Objekt fest.|  
|[setClob](../content/setClob-Method--SQLServerCallableStatement-.md)|\(Geerbt von [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md).\) Legt den angegebenen Parameter auf das angegebene Objekt fest.|  
|[setCursorName](../content/setCursorName-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Legt den SQL\-Cursornamen auf die angegebene Zeichenfolge fest, die dann für nachfolgende Ausführungsmethoden verwendet wird.|  
|[setDate](../content/setDate-Method--SQLServerCallableStatement-.md)|Legt den angegebenen Parameter auf den angegebenen Datumswert fest.|  
|[setDateTimeOffset](../content/setDateTimeOffset-Method--SQLServerCallableStatement-.md)|Legt den Wert der Spalte fest, die für den [DateTimeOffset-Klasse](../content/DateTimeOffset-Class.md)\-Wert angegeben wurde.|  
|[setDouble](../content/setDouble-Method--SQLServerCallableStatement-.md)|Legt den angegebenen Parameter auf den angegebenen Wert vom Typ **double** fest.|  
|[setEscapeProcessing](../content/setEscapeProcessing-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Legt den Escapeverarbeitungsmodus fest.|  
|[setFetchDirection](../content/setFetchDirection-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Gibt für den JDBC\-Treiber die Richtung an, in der die Resultsetzeilen verarbeitet werden sollen.|  
|[setFetchSize](../content/setFetchSize-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Gibt für den JDBC\-Treiber an, wie viele Zeilen aus der Datenbank abgerufen werden sollen, wenn weitere Zeilen benötigt werden.|  
|[setFloat](../content/setFloat-Method--SQLServerCallableStatement-.md)|Legt den angegebenen Parameter auf den angegebenen Wert vom Typ **float** fest.|  
|[setInt](../content/setInt-Method--SQLServerCallableStatement-.md)|Legt den angegebenen Parameter auf den angegebenen Wert vom Typ **int** fest.|  
|[setLong](../content/setLong-Method--SQLServerCallableStatement-.md)|Legt den angegebenen Parameter auf den angegebenen Wert vom Typ **long** fest.|  
|[setMaxFieldSize](../content/setMaxFieldSize-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Legt das Limit für die maximale Anzahl von Bytes in einer [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Spalte, in der Zeichen\- oder Binärwerte gespeichert werden, auf die angegebene Anzahl von Bytes fest.|  
|[setMaxRows](../content/setMaxRows-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Legt das Limit für die maximale Anzahl von Zeilen, die ein beliebiges [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt enthalten kann, auf die angegebene Anzahl fest.|  
|[setNCharacterStream](../content/setNCharacterStream-Method--SQLServerCallableStatement-.md)|Legt den angegebenen Parameter auf das angegebene Reader\-Objekt fest.|  
|[setNClob](../content/setNClob-Method--SQLServerCallableStatement-.md)|Legt den angegebenen Parameter auf das angegebene Objekt fest.|  
|[setNString](../content/setNString-Method--SQLServerCallableStatement-.md)|Legt den angegebenen Parameter auf das angegebene String\-Objekt fest.|  
|[setNull](../content/setNull-Method--SQLServerCallableStatement-.md)|Legt den angegebenen Parameter unter Berücksichtigung des festzulegenden Parametertyps auf einen NULL\-Wert fest.|  
|[setObject](../content/setObject-Method--SQLServerCallableStatement-.md)|Legt den Wert des angegebenen Parameters unter Verwendung des angegebenen Objekts fest.|  
|[setPoolable](../content/setPoolable-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Sendet eine Anforderung, dass dem Pool eine Anweisung hinzugefügt bzw. nicht hinzugefügt werden soll. Standardmäßig kann ein SQLServerCallableStatement\-Objekt beim Erstellen einem Pool hinzugefügt werden.|  
|[setQueryTimeout](../content/setQueryTimeout-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Legt die Anzahl von Sekunden, die vom Treiber auf die Ausführung eines CallableStatement\-Objekts gewartet wird, auf die angegebene Anzahl von Sekunden fest.|  
|[setRef](../content/setRef-Method--SQLServerPreparedStatement-.md)|\(Geerbt von [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md).\) Legt den angegebenen Parameter auf das angegebene Ref\-Objekt fest.|  
|[setResponseBuffering](../content/setResponseBuffering-Method--SQLServerStatement-.md)|\(Geerbt von [SQLServerStatement](../content/SQLServerStatement-Class.md).\) Legt den Antwortpuffermodus für dieses [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt auf **String full** oder auf **adaptive** \(jeweils ohne Berücksichtigung der Groß\- und Kleinschreibung\) fest.|  
|[setShort](../content/setShort-Method--SQLServerCallableStatement-.md)|Legt den angegebenen Parameter auf den angegebenen Wert vom Typ **short** fest.|  
|[setString](../content/setString-Method--SQLServerCallableStatement-.md)|Legt den angegebenen Parameter auf den angegebenen Java\-Wert vom Typ **String** fest.|  
|[setSQLXML](../content/setSQLXML-Method--SQLServerCallableStatement-.md)|Legt den angegebenen Parameter auf das angegebene **SQLXML**\-Objekt fest.|  
|[setTime](../content/setTime-Method--SQLServerCallableStatement-.md)|Legt den angegebenen Parameter auf den angegebenen Uhrzeitwert fest.|  
|[setTimestamp](../content/setTimestamp-Method--SQLServerCallableStatement-.md)|Legt den angegebenen Parameter auf den angegebenen Zeitstempelwert fest.|  
|[setUnicodeStream](../content/setUnicodeStream-Method--SQLServerPreparedStatement-.md)|\(Geerbt von [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md).\) Legt die angegebene Parameternummer auf den angegebenen Eingabedatenstrom mit der angegebenen Anzahl von Bytes fest.|  
|[setURL](../content/setURL-Method--SQLServerCallableStatement-.md)|Legt den angegebenen Parameter auf den angegebenen URL\-Wert fest.|  
|[unwrap](../content/unwrap-Method--SQLServerCallableStatement-.md)|Gibt ein Objekt zurück, das die angegebene Schnittstelle implementiert, um den Zugriff auf die [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-spezifischen Methoden zu ermöglichen.|  
|[wasNull](../content/wasNull-Method--SQLServerCallableStatement-.md)|Ruft ab, ob der letzte gelesene OUT\-Parameter den Wert "SQL NULL" besaß.|  
  
## Geerbte Methoden  
  
|Klasse geerbt von:|Methoden|  
|------------------------|--------------|  
|com.microsoft.sqlserver.jdbc.SQLServerPreparedStatement|addBatch, clearBatch, clearParameters, close, execute, executeBatch, executeQuery, executeUpdate, getMetaData, getParameterMetaData, setArray, setAsciiStream, setBigDecimal, setBinaryStream, setBlob, setboolean, setByte, setBytes, setCharacterStream, setClob, setDate, setDouble, setFloat, setInt, setLong, setNull, setObject, setRef, setShort, setString, setTime, setTimestamp, setUnicodeStream, setURL|  
|com.microsoft.sqlserver.jdbc.SQLServerStatement|cancel, clearWarnings, execute, executeUpdate, getConnection, getFetchDirection, getFetchSize, getGeneratedKeys, getMaxFieldSize, getMaxRows, getMoreResults, getQueryTimeout, getResultSet, getResultSetConcurrency, getResultSetHoldability, getResultSetType, getUpdateCount, getWarnings, isPoolable, setCursorName, setEscapeProcessing, setFetchDirection, setFetchSize, setMaxFieldSize, setMaxRows, setPoolable, setQueryTimeout|  
|class java.lang.Object|clone, equals, finalize, getClass, hashCode, notify, notifyAll, toString, wait,|  
|java.sql.PreparedStatement|addBatch, clearParameters, execute, executeQuery, executeUpdate, getMetaData, getParameterMetaData, getSQLXML, setArray, setAsciiStream, setBigDecimal, setBinaryStream, setBlob, setboolean, setByte, setBytes, setCharacterStream, setClob, setDate, setDate, setDouble, setFloat, setInt, setLong, setNull, setObject, setRef, setShort, setString, setSQLXML, setTime, setTimestamp, setUnicodeStream, setURL|  
|java.sql.Statement|addBatch, cancel, clearBatch, clearWarnings, close, execute, executeBatch, executeQuery, executeUpdate, getConnection, getFetchDirection, getFetchSize, getGeneratedKeys, getMaxFieldSize, getMaxRows, getMoreResults, getQueryTimeout, getResultSet, getResultSetConcurrency, getResultSetHoldability, getResultSetType, getUpdateCount, getWarnings, setCursorName, setEscapeProcessing, setFetchDirection, setFetchSize, setMaxFieldSize, setMaxRows, setQueryTimeout|  
|java.sql.Wrapper|isWrapperFor, unwrap|  
  
## Siehe auch  
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  