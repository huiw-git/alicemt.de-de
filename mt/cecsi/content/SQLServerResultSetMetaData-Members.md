---
title: "SQLServerResultSetMetaData-Elemente"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 37587981-2979-49a3-a6ab-df4bfb9b8748
caps.latest.revision: 14
caps.handback.revision: 13
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
# SQLServerResultSetMetaData-Elemente
  Die folgenden Tabellen enthalten die Elemente, die von der [SQLServerResultSetMetaData](../content/SQLServerResultSetMetaData-Class.md)\-Klasse verfügbar gemacht werden.  
  
## Konstruktoren  
 Keine  
  
## Felder  
 Keine  
  
## Geerbte Felder  
  
|Name|Beschreibung|  
|----------|------------------|  
|java.sql.ResultSetMetaData|columnNoNulls, columnNullable, columnNullableUnknown|  
  
## Methoden  
  
|Name|Beschreibung|  
|----------|------------------|  
|[getCatalogName](../content/getCatalogName-Method--SQLServerResultSetMetaData-.md)|Ruft den Katalognamen für die Tabelle mit der angegebenen Spalte ab.|  
|[getColumnClassName](../content/getColumnClassName-Method--SQLServerResultSetMetaData-.md)|Gibt den vollqualifizierten Namen der Java\-Klasse zurück, deren Instanzen erstellt werden, wenn die [getObject](../content/getObject-Method--SQLServerResultSet-.md)\-Methode der [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Klasse aufgerufen wird, um einen Wert aus der Spalte abzurufen.|  
|[getColumnCount](../content/getColumnCount-Method--SQLServerResultSetMetaData-.md)|Gibt die Anzahl von Spalten im Resultset zurück.|  
|[getColumnDisplaySize](../content/getColumnDisplaySize-Method--SQLServerResultSetMetaData-.md)|Gibt die normale maximale Breite der angegebenen Spalte in Zeichen zurück.|  
|[getColumnLabel](../content/getColumnLabel-Method--SQLServerResultSetMetaData-.md)|Ruft für die angegebene Spalte den vorgeschlagenen Titel für Ausdrucke und Anzeigen ab.|  
|[getColumnName](../content/getColumnName-Method--SQLServerResultSetMetaData-.md)|Ruft den Namen der angegebenen Spalte ab.|  
|[getColumnType](../content/getColumnType-Method--SQLServerResultSetMetaData-.md)|Ruft den SQL\-Typ der angegebenen Spalte ab.|  
|[getColumnTypeName](../content/getColumnTypeName-Method--SQLServerResultSetMetaData-.md)|Ruft den datenbankspezifischen Typnamen der angegebenen Spalte ab.|  
|[getPrecision](../content/getPrecision-Method--SQLServerResultSetMetaData-.md)|Ruft die Anzahl von Dezimalstellen für die angegebene Spalte ab.|  
|[getScale](../content/getScale-Method--SQLServerResultSetMetaData-.md)|Ruft für die angegebene Spalte die Anzahl von Stellen hinter dem Dezimalzeichen ab.|  
|[getSchemaName](../content/getSchemaName-Method--SQLServerResultSetMetaData-.md)|Ruft den Tabellenschemanamen für die angegebene Spalte ab.|  
|[getTableName](../content/getTableName-Method--SQLServerResultSetMetaData-.md)|Ruft den Tabellennamen der angegebenen Spalte ab.|  
|[isAutoIncrement](../content/isAutoIncrement-Method--SQLServerResultSetMetaData-.md)|Gibt an, ob die angegebene Spalte automatisch nummeriert wird, wodurch sie schreibgeschützt wird.|  
|[isCaseSensitive](../content/isCaseSensitive-Method--SQLServerResultSetMetaData-.md)|Gibt an, ob in einer Spalte die Groß\-\/Kleinschreibung berücksichtigt wird.|  
|[isCurrency](../content/isCurrency-Method--SQLServerResultSetMetaData-.md)|Gibt an, ob es sich bei der angegebenen Spalte um einen Währungswert handelt.|  
|[isDefinitelyWritable](../content/isDefinitelyWritable-Method--SQLServerResultSetMetaData-.md)|Gibt an, ob ein Schreibvorgang in der angegebenen Spalte definitiv erfolgreich sein wird.|  
|[isNullable](../content/isNullable-Method--SQLServerResultSetMetaData-.md)|Gibt die NULL\-Zulässigkeit von Werten in der angegebenen Spalte an.|  
|[isReadOnly](../content/isReadOnly-Method--SQLServerResultSetMetaData-.md)|Gibt an, ob die angegebene Spalte definitiv schreibgeschützt ist.|  
|[isSearchable](../content/isSearchable-Method--SQLServerResultSetMetaData-.md)|Gibt an, ob die angegebene Spalte in einer SQL\-Klausel vom Typ "WHERE" verwendet werden kann.|  
|[isSigned](../content/isSigned-Method--SQLServerResultSetMetaData-.md)|Gibt an, ob es sich bei den Werten in der angegebenen Spalte um Zahlen mit Vorzeichen handelt.|  
|[isSparseColumnSet](../content/isSparseColumnSet-Method--SQLServerResultSetMetaData-.md)|Gibt an, ob eine Spalte in einem Resultset ein Satz von Spalten mit geringer Dichte ist.|  
|[isWritable](../content/isWritable-Method--SQLServerResultSetMetaData-.md)|Gibt an, ob ein Schreibvorgang in der angegebenen Spalte möglich ist.|  
  
## Geerbte Methoden  
  
|Klasse geerbt von:|Methoden|  
|------------------------|--------------|  
|java.lang.Object|clone, equals, finalize, getClass, hashCode, notify, notifyAll, toString, wait|  
|java.sql.Wrapper|isWrapperFor, unwrap|  
  
## Siehe auch  
 [SQLServerResultSetMetaData-Klasse](../content/SQLServerResultSetMetaData-Class.md)  
  
  