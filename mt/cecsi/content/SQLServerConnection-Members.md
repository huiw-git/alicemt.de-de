---
title: "SQLServerConnection-Elemente"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3115a533-756b-4c78-aee9-4ba7253c85e0
caps.latest.revision: 25
caps.handback.revision: 24
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
# SQLServerConnection-Elemente
  Die folgenden Tabellen enthalten die Elemente, die von der [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Klasse verfügbar gemacht werden.  
  
## Konstruktoren  
 Keine  
  
## Felder  
  
|Name|Beschreibung|  
|----------|------------------|  
|[TRANSACTION\_SNAPSHOT](../content/TRANSACTION_SNAPSHOT-Field--SQLServerConnection-.md)|Dient zum Angeben der Transaktionsisolationsstufe für Momentaufnahmen.|  
  
## Geerbte Felder  
  
|Klasse geerbt von:|Beschreibung|  
|------------------------|------------------|  
|java.sql.Connection|TRANSACTION\_NONE, TRANSACTION\_READ\_COMMITTED, TRANSACTION\_READ\_UNCOMMITTED, TRANSACTION\_REPEATABLE\_READ, TRANSACTION\_SERIALIZABLE|  
  
## Methoden  
  
|Name|Beschreibung|  
|----------|------------------|  
|[clearWarnings](../content/clearWarnings-Method--SQLServerConnection-.md)|Löscht alle für dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt gemeldeten Warnungen.|  
|[close](../content/close-Method--SQLServerConnection-.md)|Gibt die Datenbank für dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt sowie die JDBC\-Ressourcen umgehend frei, sodass nicht auf deren automatische Freigabe gewartet werden muss.|  
|[commit](../content/commit-Method--SQLServerConnection-.md)|Macht alle Änderungen, die seit dem letzten Commit oder Rollback vorgenommen wurden, zu dauerhaften Änderungen und hebt sämtliche Datenbanksperren auf, die derzeit von diesem [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt aufrecht erhalten werden.|  
|[createBlob](../content/createBlob-Method--SQLServerConnection-.md)|Erstellt ein **java.sql.Blob**\-Objekt ohne Daten.|  
|[createClob](../content/createClob-Method--SQLServerConnection-.md)|Erstellt ein **java.sql.Clob**\-Objekt ohne Daten.|  
|[createNClob](../content/createNClob-Method--SQLServerConnection-.md)|Erstellt ein **java.sql.NClob**\-Objekt ohne Daten.|  
|[createStatement](../content/createStatement-Method--SQLServerConnection-.md)|Erstellt ein [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt zum Senden von SQL\-Anweisungen an die Datenbank.|  
|[createSQLXML](../content/createSQLXML-Method--SQLServerConnection-.md)|Erstellt ein **java.sql.SQLXML**\-Objekt ohne Daten.|  
|[getAutoCommit](../content/getAutoCommit-Method--SQLServerConnection-.md)|Ruft für dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt den aktuellen Modus für automatische Commits ab.|  
|[getCatalog](../content/getCatalog-Method--SQLServerConnection-.md)|Ruft den aktuellen Katalognamen für dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt ab.|  
|[getClientConnectionID-Methode &#40;SQLServerConnection&#41;](../content/getClientConnectionID-Method--SQLServerConnection-.md)|Ruft die Verbindungs\-ID des letzten Versuchs der Verbindungsherstellung ab, wobei es keine Rolle spielt, ob dieser Versuch erfolgreich war oder fehlgeschlagen ist.|  
|[getClientInfo](../content/getClientInfo-Method--SQLServerConnection-.md)|Ruft Informationen zu den Eigenschaften für Clientinformationen ab, die vom JDBC\-Treiber unterstützt werden.|  
|[getHoldability](../content/getHoldability-Method--SQLServerConnection-.md)|Ruft die aktuelle Haltbarkeit von [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekten ab, die unter Verwendung dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekts erstellt werden.|  
|[getMetaData](../content/getMetaData-Method--SQLServerConnection-.md)|Ruft ein [SQLServerDatabaseMetaData](../content/SQLServerDatabaseMetaData-Class.md)\-Objekt mit Metadaten zu der Datenbank ab, für die dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt eine Verbindung darstellt.|  
|[getTransactionIsolation](../content/getTransactionIsolation-Method--SQLServerConnection-.md)|Ruft die aktuelle Transaktionsisolationsstufe für dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt ab.|  
|[getTypeMap](../content/getTypeMap-Method--SQLServerConnection-.md)|Ruft das Map\-Objekt ab, das diesem [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt zugeordnet ist.|  
|[getWarnings](../content/getWarnings-Method--SQLServerConnection-.md)|Ruft die erste Warnung ab, die von Aufrufen für dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt gemeldet wurde.|  
|[isClosed](../content/isClosed-Method--SQLServerConnection-.md)|Gibt an, ob dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt geschlossen wurde.|  
|[isReadOnly](../content/isReadOnly-Method--SQLServerConnection-.md)|Gibt an, ob dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt schreibgeschützt ist.|  
|[isValid](../content/isValid-Method--SQLServerConnection-.md)|Gibt an, ob dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt noch geöffnet und gültig ist.|  
|[nativeSQL](../content/nativeSQL-Method--SQLServerConnection-.md)|Konvertiert die angegebene SQL\-Anweisung zur systemeigenen SQL\-Grammatik des Datenbankservers.|  
|[prepareCall](../content/prepareCall-Method--SQLServerConnection-.md)|Erstellt ein [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Objekt zum Aufrufen von in der Datenbank gespeicherten Prozeduren.|  
|[prepareStatement](../content/prepareStatement-Method--SQLServerConnection-.md)|Erstellt ein [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\-Objekt zum Senden von parametrisierten SQL\-Anweisungen an die Datenbank.|  
|[releaseSavepoint](../content/releaseSavepoint-Method--SQLServerConnection-.md)|Entfernt das angegebene [SQLServerSavepoint](../content/SQLServerSavepoint-Class.md)\-Objekt aus der aktuellen Transaktion.|  
|[rollback](../content/rollback-Method--SQLServerConnection-.md)|Macht alle im Rahmen der aktuellen Transaktion vorgenommenen Änderungen rückgängig und hebt sämtliche Datenbanksperren auf, die derzeit von diesem [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt aufrecht erhalten werden.|  
|[setAutoCommit](../content/setAutoCommit-Method--SQLServerConnection-.md)|Legt für dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt den aktuellen Modus für automatische Commits auf den angegebenen Zustand fest.|  
|[setCatalog](../content/setCatalog-Method--SQLServerConnection-.md)|Legt den angegebenen Katalognamen fest, um einen Teilbereich der Datenbank dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekts auszuwählen, in dem gearbeitet werden soll.|  
|[setClientInfo](../content/setClientInfo-Method--SQLServerConnection-.md)|Legt den Wert der Eigenschaften für Clientinformationen fest.|  
|[setHoldability](../content/setHoldability-Method--SQLServerConnection-.md)|Ändert die Haltbarkeit von [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekten, die unter Verwendung dieses [SQLServerSavepoint](../content/SQLServerSavepoint-Class.md)\-Objekts erstellt werden, zur angegebenen Haltbarkeit.|  
|[setReadOnly](../content/setReadOnly-Method--SQLServerConnection-.md)|Versetzt dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt in den schreibgeschützten Modus, damit vom JDBC\-Treiber die Datenbankoptimierungen aktiviert werden.|  
|[setSavepoint](../content/setSavepoint-Method--SQLServerConnection-.md)|Erstellt in der aktuellen Transaktion einen unbenannten Sicherungspunkt und gibt das neue [SQLServerSavepoint](../content/SQLServerSavepoint-Class.md)\-Objekt zurück, das für den Sicherungspunkt steht.|  
|[setTransactionIsolation](../content/setTransactionIsolation-Method--SQLServerConnection-.md)|Ändert die Transaktionsisolationsstufe für dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt zur angegebenen Stufe.|  
|[setTypeMap](../content/setTypeMap-Method--SQLServerConnection-.md)|Installiert das angegebene TypeMap\-Objekt als Typzuordnung für dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt.|  
  
## Geerbte Methoden  
  
|Klasse geerbt von:|Methoden|  
|------------------------|--------------|  
|java.lang.Object|clone, equals, finalize, getClass, hashCode, notify, notifyAll, toString, wait|  
|java.lang.Wrapper|isWrapperFor, unwrap|  
  
## Siehe auch  
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  