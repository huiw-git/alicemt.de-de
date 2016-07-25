---
title: "ISQLServerResultSet-Elemente"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2a438d5d-2d6a-46a0-a2ae-f35fbae4a472
caps.latest.revision: 22
caps.handback.revision: 21
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
# ISQLServerResultSet-Elemente
    
## ISQLServerResultSet\-Elemente  
 Die folgenden Tabellen enthalten die Elemente, die von der [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Klasse verfügbar gemacht werden.  
  
### Konstruktoren  
 Keine  
  
### Felder  
  
|Name|Beschreibung|  
|----------|------------------|  
|[CONCUR\_SS\_OPTIMISTIC\_CC](../content/CONCUR_SS_OPTIMISTIC_CC-Field--SQLServerResultSet-.md)|Dient zum Angeben eines Typs der vollständigen Parallelität \(Lese\-\/Schreibzugriff\) für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ohne Zeilensperre.|  
|[CONCUR\_SS\_OPTIMISTIC\_CCVAL](../content/CONCUR_SS_OPTIMISTIC_CCVAL-Field--SQLServerResultSet-.md)|Dient zum Angeben eines Typs der vollständigen Parallelität \(Lese\-\/Schreibzugriff\) für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ohne Zeilensperre.|  
|[CONCUR\_SS\_SCROLL\_LOCKS](../content/CONCUR_SS_SCROLL_LOCKS-Field--SQLServerResultSet-.md)|Dient zum Angeben eines Typs der vollständigen Parallelität \(Lese\-\/Schreibzugriff\) für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] mit Zeilensperre.|  
|[TYPE\_SS\_DIRECT\_FORWARD\_ONLY](../content/TYPE_SS_DIRECT_FORWARD_ONLY-Field--SQLServerResultSet-.md)|Dient zum Angeben eines schnellen schreibgeschützten Vorwärtscursortyps für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)].|  
|[TYPE\_SS\_SCROLL\_DYNAMIC](../content/TYPE_SS_SCROLL_DYNAMIC-Field--SQLServerResultSet-.md)|Dient zum Angeben eines dynamischen Cursortyps für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)].|  
|[TYPE\_SS\_SCROLL\_KEYSET](../content/TYPE_SS_SCROLL_KEYSET-Field--SQLServerResultSet-.md)|Dient zum Angeben eines Keysetcursortyps für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)].|  
|[TYPE\_SS\_SCROLL\_STATIC](../content/TYPE_SS_SCROLL_STATIC-Field--SQLServerResultSet-.md)|Dient zum Angeben eines statischen Cursortyps für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)].|  
|[TYPE\_SS\_SERVER\_CURSOR\_FORWARD\_ONLY](../content/TYPE_SS_SERVER_CURSOR_FORWARD_ONLY-Field--SQLServerResultSet-.md)|Dient zum Angeben eines schnellen schreibgeschützten Vorwärtscursortyps für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)].|  
  
### Geerbte Felder  
  
|Klasse geerbt von:|Beschreibung|  
|------------------------|------------------|  
|java.sql.ResultSet|CLOSE\_CURSORS\_AT\_COMMIT, CONCUR\_READ\_ONLY, CONCUR\_UPDATABLE, FETCH\_FORWARD, FETCH\_REVERSE, FETCH\_UNKNOWN, HOLD\_CURSORS\_OVER\_COMMIT, TYPE\_FORWARD\_ONLY, TYPE\_SCROLL\_INSENSITIVE, TYPE\_SCROLL\_SENSITIVE|  
  
### Methoden  
  
|Name|Beschreibung|  
|----------|------------------|  
|[absolute](../content/absolute-Method--SQLServerResultSet-.md)|Versetzt den Cursor in die angegebene Zeile in diesem [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt.|  
|[afterLast](../content/afterLast-Method--SQLServerResultSet-.md)|Versetzt den Cursor an eine Position nach der letzten Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts.|  
|[beforeFirst](../content/beforeFirst-Method--SQLServerResultSet-.md)|Versetzt den Cursor an eine Position vor der ersten Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts.|  
|[cancelRowUpdates](../content/cancelRowUpdates-Method--SQLServerResultSet-.md)|Bricht die Aktualisierungen ab, die an der aktuellen Zeile in diesem [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt vorgenommen wurden.|  
|[clearWarnings](../content/clearWarnings-Method--SQLServerResultSet-.md)|Löscht alle für dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt gemeldeten Warnungen.|  
|[close](../content/close-Method--SQLServerResultSet-.md)|Gibt die Datenbank\- und JDBC\-Ressourcen dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts umgehend frei, sodass nicht darauf gewartet werden muss, bis dieser Vorgang beim automatischen Schließen ausgeführt wird.|  
|[deleteRow](../content/deleteRow-Method--SQLServerResultSet-.md)|Löscht die aktuelle Zeile aus diesem[SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt sowie aus der zugrunde liegenden Datenbank.|  
|[finalize](../content/finalize-Method--SQLServerResultSet-.md)|Schließt dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt explizit.|  
|[findColumn](../content/findColumn-Method--SQLServerResultSet-.md)|Ruft für den angegebenen Spaltennamen den Index der ersten übereinstimmenden Spalte in diesem [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt ab.|  
|[first](../content/first-Method--SQLServerResultSet-.md)|Versetzt den Cursor in die erste Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts.|  
|[getArray](../content/getArray-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Array\-Objekt ab.|  
|[getAsciiStream](../content/getAsciiStream-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als ASCII\-Zeichendatenstrom ab.|  
|[getBigDecimal](../content/getBigDecimal-Method--SQLServerResultSet-.md)|Ruft den Wert des angegebenen Spaltenindex in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als "java.math.BigDecimal" ab.|  
|[getBinaryStream](../content/getBinaryStream-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Binärdatenstrom nicht interpretierter Bytes ab.|  
|[getBlob](../content/getBlob-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Blob\-Objekt in der Programmiersprache Java ab.|  
|[getBoolean](../content/getBoolean-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Wert vom Typ **boolean** in der Programmiersprache Java ab.|  
|[getByte](../content/getByte-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Wert vom Typ **byte** in der Programmiersprache Java ab.|  
|[getBytes](../content/getBytes-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Array vom Typ **byte** in der Programmiersprache Java ab.|  
|[getCharacterStream](../content/getCharacterStream-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als java.io.Reader\-Objekt ab.|  
|[getClob](../content/getClob-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Clob\-Objekt in der Programmiersprache Java ab.|  
|[getConcurrency](../content/getConcurrency-Method--SQLServerResultSet-.md)|Ruft den Parallelitätsmodus dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts ab.|  
|[getCursorName](../content/getCursorName-Method--SQLServerResultSet-.md)|Ruft den Namen des von diesem [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt verwendeten SQL\-Cursors ab.|  
|[getDate](../content/getDate-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als java.sql.Date\-Objekt in der Programmiersprache Java ab.|  
|[getDateTimeOffset](../content/getDateTimeOffset--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte als[DateTimeOffset-Klasse](../content/DateTimeOffset-Class.md)\-Objekt ab.|  
|[getDouble](../content/getDouble-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Wert vom Typ **double** in der Programmiersprache Java ab.|  
|[getFetchDirection](../content/getFetchDirection-Method--SQLServerResultSet-.md)|Ruft die Abrufrichtung für dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt ab.|  
|[getFetchSize](../content/getFetchSize-Method--SQLServerResultSet-.md)|Ruft die Abrufgröße für dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt ab.|  
|[getFloat](../content/getFloat-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Wert vom Typ **float** in der Programmiersprache Java ab.|  
|[getHoldability](../content/getHoldability-Method--SQLServerResultSet-.md)|Ruft die Haltbarkeit dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts ab.|  
|[getInt](../content/getInt-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Wert vom Typ **int** in der Programmiersprache Java ab.|  
|[getLong](../content/getLong-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Wert vom Typ **long** in der Programmiersprache Java ab.|  
|[getMetaData](../content/getMetaData-Method--SQLServerResultSet-.md)|Ruft Anzahl, Typ und Eigenschaften der Spalten dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts ab.|  
|[getNCharacterStream](../content/getNCharacterStream-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile des [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Reader\-Objekt ab.|  
|[getNClob](../content/getNClob-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile des [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als **NClob**\-Objekt in der Programmiersprache Java ab.|  
|[getNString](../content/getNString-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile des [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als String in der Programmiersprache Java ab.|  
|[getObject](../content/getObject-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Objekt in der Programmiersprache Java ab.|  
|[getRef](../content/getRef-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Ref\-Objekt in der Programmiersprache Java ab.|  
|[getRow](../content/getRow-Method--SQLServerResultSet-.md)|Ruft die aktuelle Zeilennummer ab.|  
|[getShort](../content/getShort-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Wert vom Typ **short** in der Programmiersprache Java ab.|  
|[getStatement](../content/getStatement-Method--SQLServerResultSet-.md)|Ruft das [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt ab, von dem dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt erstellt wurde.|  
|[getString](../content/getString-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Wert vom Typ **String** in der Programmiersprache Java ab.|  
|[getSQLXML](../content/getSQLXML-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile des [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als **SQLXML**\-Objekt ab.|  
|[getTime](../content/getTime-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als java.sql.Time\-Objekt in der Programmiersprache Java ab.|  
|[getTimestamp](../content/getTimestamp-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als java.sql.Timestamp\-Objekt in der Programmiersprache Java ab.|  
|[getType](../content/getType-Method--SQLServerResultSet-.md)|Ruft den Cursortyp dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts ab.|  
|[getUnicodeStream](../content/getUnicodeStream-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Unicode\-Zeichendatenstrom ab.|  
|[getURL](../content/getURL-Method--SQLServerResultSet-.md)|Ruft den Wert der angegebenen Spalte in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als URL\-Objekt ab.|  
|[getWarnings](../content/getWarnings-Method--SQLServerResultSet-.md)|Ruft die erste Warnung ab, die von Aufrufen für dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt gemeldet wurde.|  
|[insertRow](../content/insertRow-Method--SQLServerResultSet-.md)|Fügt den Inhalt der Einfügezeile in dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt und in die Datenbank ein.|  
|[isAfterLast](../content/isAfterLast-Method--SQLServerResultSet-.md)|Ruft ab, ob sich der Cursor an einer Position nach der letzten Zeile in diesem [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt befindet.|  
|[isBeforeFirst](../content/isBeforeFirst-Method--SQLServerResultSet-.md)|Ruft ab, ob sich der Cursor an einer Position vor der ersten Zeile in diesem [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt befindet.|  
|[isClosed](../content/isClosed-Method--SQLServerResultSet-.md)|Gibt an, ob dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt geschlossen wurde.|  
|[isFirst](../content/isFirst-Method--SQLServerResultSet-.md)|Ruft ab, ob sich der Cursor in der ersten Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts befindet.|  
|[isLast](../content/isLast-Method--SQLServerResultSet-.md)|Ruft ab, ob sich der Cursor in der letzten Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts befindet.|  
|[last](../content/last-Method--SQLServerResultSet-.md)|Versetzt den Cursor in die letzte Zeile in diesem [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt.|  
|[moveToCurrentRow](../content/moveToCurrentRow-Method--SQLServerResultSet-.md)|Versetzt den Cursor an die gespeicherte Cursorposition \(üblicherweise die aktuelle Zeile\).|  
|[moveToInsertRow](../content/moveToInsertRow-Method--SQLServerResultSet-.md)|Versetzt den Cursor in die Einfügezeile.|  
|[next](../content/next-Method--SQLServerResultSet-.md)|Versetzt den Cursor von seiner aktuellen Position aus um eine Zeile nach unten.|  
|[previous](../content/previous-Method--SQLServerResultSet-.md)|Versetzt den Cursor in die vorherige Zeile in diesem [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt.|  
|[refreshRow](../content/refreshRow-Method--SQLServerResultSet-.md)|Aktualisiert die aktuelle Zeile mit dem aktuellen Wert aus der Datenbank.|  
|[relative](../content/relative-Method--SQLServerResultSet-.md)|Versetzt den Cursor relativ zur aktuellen Zeile um eine bestimmte \(positive oder negative\) Anzahl von Zeilen.|  
|[rowDeleted](../content/rowDeleted-Method--SQLServerResultSet-.md)|Ruft ab, ob eine Zeile gelöscht wurde.|  
|[rowInserted](../content/rowInserted-Method--SQLServerResultSet-.md)|Ruft ab, ob in der aktuellen Zeile eine Einfügung vorgenommen wurde.|  
|[rowUpdated](../content/rowUpdated-Method--SQLServerResultSet-.md)|Ruft ab, ob die aktuelle Zeile aktualisiert wurde.|  
|[setFetchDirection](../content/setFetchDirection-Method--SQLServerResultSet-.md)|Gibt Aufschluss über die Richtung, in der die Zeilen in diesem [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt verarbeitet werden.|  
|[setFetchSize](../content/setFetchSize-Method--SQLServerResultSet-.md)|Gibt für den JDBC\-Treiber an, wie viele Zeilen aus der Datenbank abgerufen werden sollen, wenn für dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt weitere Zeilen benötigt werden.|  
|[updateArray](../content/updateArray-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit einem Array\-Objekt.|  
|[updateAsciiStream](../content/updateAsciiStream-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit einem ASCII\-Datenstromwert.|  
|[updateBigDecimal](../content/updateBigDecimal-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit einem BigDecimal\-Objekt.|  
|[updateBinaryStream](../content/updateBinaryStream-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit einem Binärdatenstromwert.|  
|[updateBlob](../content/updateBlob-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit einem java.sql.Blob\-Wert.|  
|[updateBoolean](../content/updateBoolean-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit einem **boolean** \-Wert.|  
|[updateByte](../content/updateByte-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit einem Wert vom Typ **byte** .|  
|[updateBytes](../content/updateBytes-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit einem Array von **byte** \-Werten.|  
|[updateCharacterStream](../content/updateCharacterStream-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit einem Zeichendatenstromwert.|  
|[updateClob](../content/updateClob-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit einem java.sql.Clob\-Wert.|  
|[updateDate](../content/updateDate-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit einem Datumswert.|  
|[updateDateTimeOffset](../content/updateDateTimeOffset--SQLServerResultSet-.md)|Aktualisiert eine [DateTimeOffset-Klasse](../content/DateTimeOffset-Class.md)\-Spalte.|  
|[updateDouble](../content/updateDouble-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit einem **double** \-Wert.|  
|[updateFloat](../content/updateFloat-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit einem Wert vom Typ **float** .|  
|[updateInt](../content/updateInt-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit einem Wert vom Typ **int** .|  
|[updateLong](../content/updateLong-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit einem Wert vom Typ **long** .|  
|[updateNCharacterStream](../content/updateNCharacterStream-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit einem Zeichendatenstromwert.|  
|[updateNClob](../content/updateNClob-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit dem angegebenen Objektwert.|  
|[updateNString](../content/updateNString-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit einem **String**\-Wert.|  
|[updateNull](../content/updateNull-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit einem NULL\-Wert.|  
|[updateObject](../content/updateObject-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit einem Wert vom Typ **Object** .|  
|[updateRef](../content/updateRef-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit einem java.sql.Ref\-Wert.|  
|[updateRow](../content/updateRow-Method--SQLServerResultSet-.md)|Aktualisiert die zugrunde liegende Datenbank mit dem neuen Inhalt der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts.|  
|[updateShort](../content/updateShort-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit einem Wert vom Typ **short** .|  
|[updateString](../content/updateString-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit einem Wert vom Typ **String** .|  
|[updateSQLXML](../content/updateSQLXML-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit einem **SQLXML**\-Wert.|  
|[updateTime](../content/updateTime-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit einem Uhrzeitwert.|  
|[updateTimestamp](../content/updateTimestamp-Method--SQLServerResultSet-.md)|Aktualisiert die angegebene Spalte mit einem Zeitstempelwert.|  
|[wasNull](../content/wasNull-Method--SQLServerResultSet-.md)|Überprüft, ob es sich beim letzten gelesenen Wert um einen NULL\-Wert handelt.|  
  
### Geerbte Methoden  
  
|Klasse geerbt von:|Methoden|  
|------------------------|--------------|  
|java.lang.Object|clone, equals, getClass, hashCode, notify, notifyAll, toString, wait|  
|java.sql.Wrapper|isWrapperFor, unwrap|  
  
## Siehe auch  
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  