---
title: "SQLServerDatabaseMetaData-Elemente"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 327ba0bc-438a-494c-b119-1cd4a096bb58
caps.latest.revision: 24
caps.handback.revision: 23
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
# SQLServerDatabaseMetaData-Elemente
    
## SQLServerDatabaseMetaData\-Elemente  
 Die folgenden Tabellen enthalten die Elemente, die von der [SQLServerDatabaseMetaData](../content/SQLServerDatabaseMetaData-Class.md)\-Klasse verfügbar gemacht werden.  
  
### Konstruktoren  
 Keine  
  
### Felder  
 Keine  
  
### Geerbte Felder  
  
|Name|Beschreibung|  
|----------|------------------|  
|java.sql.DatabaseMetaData|attributeNoNulls, attributeNullable, attributeNullableUnknown, bestRowNotPseudo, bestRowPseudo, bestRowSession, bestRowTemporary, bestRowTransaction, bestRowUnknown, columnNoNulls, columnNullable, columnNullableUnknown, importedKeyCascade, importedKeyInitiallyDeferred, importedKeyInitiallyImmediate, importedKeyNoAction, importedKeyNotDeferrable, importedKeyRestrict, importedKeySetDefault, importedKeySetNull, procedureColumnIn, procedureColumnInOut, procedureColumnOut, procedureColumnResult, procedureColumnReturn, procedureColumnUnknown, procedureNoNulls, procedureNoResult, procedureNullable, procedureNullableUnknown, procedureResultUnknown, procedureReturnsResult, sqlStateSQL, sqlStateSQL99, sqlStateXOpen, tableIndexClustered, tableIndexHashed, tableIndexOther, tableIndexStatistic, typeNoNulls, typeNullable, typeNullableUnknown, typePredBasic, typePredChar, typePredNone, typeSearchable, versionColumnNotPseudo, versionColumnPseudo, versionColumnUnknown|  
  
### Methoden  
  
|Name|Beschreibung|  
|----------|------------------|  
|[allProceduresAreCallable](../content/allProceduresAreCallable-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob der aktuelle Benutzer zum Aufrufen aller Prozeduren berechtigt ist, die von der [getProcedures](../content/getProcedures-Method--SQLServerDatabaseMetaData-.md)\-Methode zurückgegeben werden.|  
|[allTablesAreSelectable](../content/allTablesAreSelectable-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob der aktuelle Benutzer zum Verwenden aller Tabellen berechtigt ist, die von der [getTables](../content/getTables-Method--SQLServerDatabaseMetaData-.md)\-Methode in einer SELECT\-Anweisung zurückgegeben werden.|  
|[autoCommitFailureClosesAllResultSets](../content/autoCommitFailureClosesAllResultSets-Method--SQLServerDatabaseMetaData-.md)|Gibt an, ob vom JDBC\-Treiber alle geöffneten Resultsets \(einschließlich Resultsets mit Haltbarkeit\) geschlossen werden, wenn ein automatischer Commit aktiviert und eine Ausnahme ausgelöst wird.|  
|[dataDefinitionCausesTransactionCommit](../content/dataDefinitionCausesTransactionCommit-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob durch eine Datendefinitionsanweisung innerhalb einer Transaktion ein Commit der Transaktion erzwungen wird.|  
|[dataDefinitionIgnoredInTransactions](../content/dataDefinitionIgnoredInTransactions-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank eine Datendefinitionsanweisung innerhalb einer Transaktion ignoriert wird.|  
|[deletesAreDetected](../content/deletesAreDetected-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob das Löschen einer sichtbaren Zeile durch Aufrufen der [rowDeleted](../content/rowDeleted-Method--SQLServerResultSet-.md)\-Methode der [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Klasse ermittelt werden kann.|  
|[doesMaxRowSizeIncludeBlobs](../content/doesMaxRowSizeIncludeBlobs-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob der Rückgabewert für die [getMaxRowSize](../content/getMaxRowSize-Method--SQLServerDatabaseMetaData-.md)\-Methode die SQL\-Datentypen "LONGVARCHAR" und "LONGVARBINARY" beinhaltet.|  
|[getAttributes](../content/getAttributes-Method--SQLServerDatabaseMetaData-.md)|Ruft eine Beschreibung des angegebenen Attributs vom angegebenen Typ für einen benutzerdefinierten Typ ab, der im angegebenen Schema und Katalog verfügbar ist.|  
|[getBestRowIdentifier](../content/getBestRowIdentifier-Method--SQLServerDatabaseMetaData-.md)|Ruft eine Beschreibung der optimalen Gruppe von Spalten einer Tabelle ab, durch die eine Zeile eindeutig identifiziert wird.|  
|[getCatalogs](../content/getCatalogs-Method--SQLServerDatabaseMetaData-.md)|Ruft die Katalognamen ab, die auf dem Server verfügbar sind, mit dem eine Verbindung besteht.|  
|[getCatalogSeparator](../content/getCatalogSeparator-Method--SQLServerDatabaseMetaData-.md)|Ruft den **String** ab, der von dieser Datenbank als Trennzeichen zwischen Katalog\- und Tabellenname verwendet wird.|  
|[getCatalogTerm](../content/getCatalogTerm-Method--SQLServerDatabaseMetaData-.md)|Ruft den bevorzugten Begriff des Datenbankherstellers für "catalog" ab.|  
|[getClientInfoProperties](../content/getClientInfoProperties-Method--SQLServerDatabaseMetaData-.md)|Ruft eine Liste mit den Eigenschaften für Clientinformationen ab, die vom Treiber unterstützt werden.|  
|[getColumnPrivileges](../content/getColumnPrivileges-Method--SQLServerDatabaseMetaData-.md)|Ruft eine Beschreibung der Zugriffsrechte für die Spalten in einer Tabelle ab.|  
|[getColumns](../content/getColumns-Method--SQLServerDatabaseMetaData-.md)|Ruft eine Beschreibung der Tabellenspalten ab, die im angegebenen Katalog verfügbar sind.|  
|[getConnection](../content/getConnection-Method--SQLServerDatabaseMetaData-.md)|Ruft die Verbindung ab, von der dieses Metadatenobjekt erstellt wurde.|  
|[getCrossReference](../content/getCrossReference-Method--SQLServerDatabaseMetaData-.md)|Ruft eine Beschreibung der Fremdschlüsselspalten in der angegebenen Fremdschlüsseltabelle ab, von der auf die Primärschlüsselspalten der angegebenen Primärschlüsseltabelle verwiesen wird.|  
|[getDatabaseMajorVersion](../content/getDatabaseMajorVersion-Method--SQLServerDatabaseMetaData-.md)|Ruft die Hauptversionsnummer der zugrunde liegenden Datenbank ab.|  
|[getDatabaseMinorVersion](../content/getDatabaseMinorVersion-Method--SQLServerDatabaseMetaData-.md)|Ruft die Nebenversionsnummer der zugrunde liegenden Datenbank ab.|  
|[getDatabaseProductName](../content/getDatabaseProductName-Method--SQLServerDatabaseMetaData-.md)|Ruft den Namen dieses Datenbankprodukts ab.|  
|[getDatabaseProductVersion](../content/getDatabaseProductVersion-Method--SQLServerDatabaseMetaData-.md)|Ruft die Versionsnummer dieses Datenbankprodukts ab.|  
|[getDefaultTransactionIsolation](../content/getDefaultTransactionIsolation-Method--SQLServerDatabaseMetaData-.md)|Ruft die standardmäßige Transaktionsisolationsstufe für diese Datenbank ab.|  
|[getDriverMajorVersion](../content/getDriverMajorVersion-Method--SQLServerDatabaseMetaData-.md)|Ruft die Hauptversionsnummer dieses JDBC\-Treibers ab.|  
|[getDriverMinorVersion](../content/getDriverMinorVersion-Method--SQLServerDatabaseMetaData-.md)|Ruft die Nebenversionsnummer dieses JDBC\-Treibers ab.|  
|[getDriverName](../content/getDriverName-Method--SQLServerDatabaseMetaData-.md)|Ruft den Namen dieses JDBC\-Treibers ab.|  
|[getDriverVersion](../content/getDriverVersion-Method--SQLServerDatabaseMetaData-.md)|Ruft die Versionsnummer dieses JDBC\-Treibers ab.|  
|[getExportedKeys](../content/getExportedKeys-Method--SQLServerDatabaseMetaData-.md)|Ruft eine Beschreibung der Fremdschlüsselspalten ab, von denen auf die Primärschlüsselspalten der angegebenen Tabelle verwiesen wird.|  
|[getExtraNameCharacters](../content/getExtraNameCharacters-Method--SQLServerDatabaseMetaData-.md)|Ruft alle zusätzlichen Zeichen ab, die in Bezeichnernamen ohne Anführungszeichen verwendet werden können \(beispielsweise Zeichen, die über "a \- z", "A \- Z", "0 \- 9" und "\_" hinausgehen\).|  
|[getFunctions](../content/getFunctions-Method--SQLServerDatabaseMetaData-.md)|Ruft eine Beschreibung der System\- und Benutzerfunktionen ab.|  
|[getFunctionColumns](../content/getFunctionColumns-Method--SQLServerDatabaseMetaData-.md)|Ruft eine Beschreibung der System\- oder Benutzerfunktionsparameter des angegebenen Katalogs sowie den Rückgabetyp ab.|  
|[getIdentifierQuoteString](../content/getIdentifierQuoteString-Method--SQLServerDatabaseMetaData-.md)|Ruft den **String** ab, mit dem SQL\-Bezeichner in Anführungszeichen gesetzt werden.|  
|[getImportedKeys](../content/getImportedKeys-Method--SQLServerDatabaseMetaData-.md)|Ruft eine Beschreibung der Primärschlüsselspalten ab, auf die von den Fremdschlüsselspalten einer Tabelle verwiesen wird.|  
|[getIndexInfo](../content/getIndexInfo-Method--SQLServerDatabaseMetaData-.md)|Ruft eine Beschreibung der Indizes und der Statistik der angegebenen Tabelle ab.|  
|[getJDBCMajorVersion](../content/getJDBCMajorVersion-Method--SQLServerDatabaseMetaData-.md)|Ruft die JDBC\-Hauptversionsnummer für diesen Treiber ab.|  
|[getJDBCMinorVersion](../content/getJDBCMinorVersion-Method--SQLServerDatabaseMetaData-.md)|Ruft die JDBC\-Nebenversionsnummer für diesen Treiber ab.|  
|[getMaxBinaryLiteralLength](../content/getMaxBinaryLiteralLength-Method--SQLServerDatabaseMetaData-.md)|Ruft die maximale Anzahl von Hexadezimalzeichen ab, die bei dieser Datenbank für ein Inline\-Binärliteral zulässig sind.|  
|[getMaxCatalogNameLength](../content/getMaxCatalogNameLength-Method--SQLServerDatabaseMetaData-.md)|Ruft die maximale Anzahl von Zeichen ab, die bei dieser Datenbank für einen Katalognamen zulässig sind.|  
|[getMaxCharLiteralLength](../content/getMaxCharLiteralLength-Method--SQLServerDatabaseMetaData-.md)|Ruft die maximale Anzahl von Zeichen ab, die bei dieser Datenbank für ein Zeichenliteral zulässig sind.|  
|[getMaxColumnNameLength](../content/getMaxColumnNameLength-Method--SQLServerDatabaseMetaData-.md)|Ruft die maximale Anzahl von Zeichen ab, die bei dieser Datenbank für einen Spaltennamen zulässig sind.|  
|[getMaxColumnsInGroupBy](../content/getMaxColumnsInGroupBy-Method--SQLServerDatabaseMetaData-.md)|Ruft die maximale Anzahl von Spalten ab, die bei dieser Datenbank in einer GROUP BY\-Klausel zulässig sind.|  
|[getMaxColumnsInIndex](../content/getMaxColumnsInIndex-Method--SQLServerDatabaseMetaData-.md)|Ruft die maximale Anzahl von Spalten ab, die bei dieser Datenbank in einem Index zulässig sind.|  
|[getMaxColumnsInOrderBy](../content/getMaxColumnsInOrderBy-Method--SQLServerDatabaseMetaData-.md)|Ruft die maximale Anzahl von Spalten ab, die bei dieser Datenbank in einer ORDER BY\-Klausel zulässig sind.|  
|[getMaxColumnsInSelect](../content/getMaxColumnsInSelect-Method--SQLServerDatabaseMetaData-.md)|Ruft die maximale Anzahl von Spalten ab, die bei dieser Datenbank in einer SELECT\-Liste zulässig sind.|  
|[getMaxColumnsInTable](../content/getMaxColumnsInTable-Method--SQLServerDatabaseMetaData-.md)|Ruft die maximale Anzahl von Spalten ab, die bei dieser Datenbank in einer Tabelle zulässig sind.|  
|[getMaxConnections](../content/getMaxConnections-Method--SQLServerDatabaseMetaData-.md)|Ruft die maximal mögliche Anzahl gleichzeitiger Verbindungen mit dieser Datenbank ab.|  
|[getMaxCursorNameLength](../content/getMaxCursorNameLength-Method--SQLServerDatabaseMetaData-.md)|Ruft die maximale Anzahl von Zeichen ab, die bei dieser Datenbank für einen Cursornamen zulässig sind.|  
|[getMaxIndexLength](../content/getMaxIndexLength-Method--SQLServerDatabaseMetaData-.md)|Ruft die maximale Anzahl von Bytes ab, die bei dieser Datenbank in einem Index \(einschließlich aller Indexteile\) zulässig sind.|  
|[getMaxProcedureNameLength](../content/getMaxProcedureNameLength-Method--SQLServerDatabaseMetaData-.md)|Ruft die maximale Anzahl von Zeichen ab, die bei dieser Datenbank für einen Prozedurnamen zulässig sind.|  
|[getMaxRowSize](../content/getMaxRowSize-Method--SQLServerDatabaseMetaData-.md)|Ruft die maximale Anzahl von Bytes ab, die bei dieser Datenbank in einer einzelnen Zeile zulässig sind.|  
|[getMaxSchemaNameLength](../content/getMaxSchemaNameLength-Method--SQLServerDatabaseMetaData-.md)|Ruft die maximale Anzahl von Zeichen ab, die bei dieser Datenbank für einen Schemanamen zulässig sind.|  
|[getMaxStatementLength](../content/getMaxStatementLength-Method--SQLServerDatabaseMetaData-.md)|Ruft die maximale Anzahl von Zeichen ab, die bei dieser Datenbank für eine SQL\-Anweisung zulässig sind.|  
|[getMaxStatements](../content/getMaxStatements-Method--SQLServerDatabaseMetaData-.md)|Ruft die maximale Anzahl aktiver Anweisungen an diese Datenbank ab, die gleichzeitig geöffnet sein können.|  
|[getMaxTableNameLength](../content/getMaxTableNameLength-Method--SQLServerDatabaseMetaData-.md)|Ruft die maximale Anzahl von Zeichen ab, die bei dieser Datenbank für einen Tabellennamen zulässig sind.|  
|[getMaxTablesInSelect](../content/getMaxTablesInSelect-Method--SQLServerDatabaseMetaData-.md)|Ruft die maximale Anzahl von Tabellen ab, die bei dieser Datenbank in einer SELECT\-Anweisung zulässig sind.|  
|[getMaxUserNameLength](../content/getMaxUserNameLength-Method--SQLServerDatabaseMetaData-.md)|Ruft die maximale Anzahl von Zeichen ab, die bei dieser Datenbank für einen Benutzernamen zulässig sind.|  
|[getNumericFunctions](../content/getNumericFunctions-Method--SQLServerDatabaseMetaData-.md)|Ruft eine durch Trennzeichen getrennte Liste mit mathematischen Funktionen ab, die für diese Datenbank verfügbar sind.|  
|[getPrimaryKeys](../content/getPrimaryKeys-Method--SQLServerDatabaseMetaData-.md)|Ruft eine Beschreibung der Primärschlüsselspalten der angegebenen Tabelle ab.|  
|[getProcedureColumns](../content/getProcedureColumns-Method--SQLServerDatabaseMetaData-.md)|Ruft eine Beschreibung der Parameter gespeicherter Prozeduren und Ergebnisspalten ab.|  
|[getProcedures](../content/getProcedures-Method--SQLServerDatabaseMetaData-.md)|Ruft eine Beschreibung der gespeicherten Prozeduren ab, die im angegebenen Katalog, Schema oder Namensmuster für gespeicherte Prozeduren verfügbar sind.|  
|[getProcedureTerm](../content/getProcedureTerm-Method--SQLServerDatabaseMetaData-.md)|Ruft den bevorzugten Begriff für "procedure" in dieser Datenbank ab.|  
|[getResultSetHoldability](../content/getResultSetHoldability-Method--SQLServerDatabaseMetaData-.md)|Ruft die Standardhaltbarkeit von Resultsets für diese Datenbank ab.|  
|[getRowIdLifetime](../content/getRowIdLifetime-Method--SQLServerDatabaseMetaData-.md)|Gibt einen Status zurück, mit dem angegeben wird, ob der SQL\-Datentyp "RowId" unterstützt wird. Sofern unterstützt, wird die Lebensdauer zurückgegeben, für die ein RowId\-Objekt gültig ist.|  
|[getSchemas](../content/getSchemas-Method---.md)|Ruft die Schemanamen ab, die in der aktuellen Datenbank verfügbar sind.|  
|[getSchemaTerm](../content/getSchemaTerm-Method--SQLServerDatabaseMetaData-.md)|Ruft den bevorzugten Begriff für "schema" in dieser Datenbank ab.|  
|[getSearchStringEscape](../content/getSearchStringEscape-Method--SQLServerDatabaseMetaData-.md)|Ruft den **String** ab, mit dem sich Platzhalterzeichen mit Escapezeichen versehen lassen.|  
|[getSQLKeywords](../content/getSQLKeywords-Method--SQLServerDatabaseMetaData-.md)|Ruft eine durch Trennzeichen getrennte Liste mit allen SQL\-Schlüsselwörtern dieser Datenbank ab, bei denen es sich nicht gleichzeitig um SQL92\-Schlüsselwörter handelt.|  
|[getSQLStateType](../content/getSQLStateType-Method--SQLServerDatabaseMetaData-.md)|Gibt an, ob "SQLSTATE" \(zurückgegeben von der SQLException.getSQLState\-Methode\) den Wert "X\/Open" \(jetzt "Open Group"\), "SQL CLI", "SQL99" \(JDBC 3.0\) oder "SQL:2003" \(JDBC 4.0\) besitzt.|  
|[getStringFunctions](../content/getStringFunctions-Method--SQLServerDatabaseMetaData-.md)|Ruft eine durch Trennzeichen getrennte Liste mit **String** \-Funktionen ab, die für diese Datenbank verfügbar sind.|  
|[getSuperTables](../content/getSuperTables-Method--SQLServerDatabaseMetaData-.md)|Ruft eine Beschreibung der Tabellenhierarchien ab, die in einem bestimmten Schema in dieser Datenbank definiert sind.|  
|[getSuperTypes](../content/getSuperTypes-Method--SQLServerDatabaseMetaData-.md)|Ruft eine Beschreibung der benutzerdefinierten Typhierarchien ab, die in einem bestimmten Schema in dieser Datenbank definiert sind.|  
|[getSystemFunctions](../content/getSystemFunctions-Method--SQLServerDatabaseMetaData-.md)|Ruft eine durch Trennzeichen getrennte Liste mit Systemfunktionen ab, die für diese Datenbank verfügbar sind.|  
|[getTablePrivileges](../content/getTablePrivileges-Method--SQLServerDatabaseMetaData-.md)|Ruft eine Beschreibung der Zugriffsrechte für die einzelnen Tabellen ab, die im angegebenen Katalog, Schema oder Tabellennamenmuster verfügbar sind.|  
|[getTables](../content/getTables-Method--SQLServerDatabaseMetaData-.md)|Ruft eine Beschreibung der Tabellen ab, die im angegebenen Katalog, Schema oder Tabellennamenmuster verfügbar sind.|  
|[getTableTypes](../content/getTableTypes-Method--SQLServerDatabaseMetaData-.md)|Ruft die Tabellentypen ab, die in der aktuellen Datenbank verfügbar sind.|  
|[getTimeDateFunctions](../content/getTimeDateFunctions-Method--SQLServerDatabaseMetaData-.md)|Ruft eine durch Trennzeichen getrennte Liste mit den Uhrzeit\- und Datumsfunktionen ab, die für diese Datenbank verfügbar sind.|  
|[getTypeInfo](../content/getTypeInfo-Method--SQLServerDatabaseMetaData-.md)|Ruft eine Beschreibung aller standardmäßigen SQL\-Typen ab, die von der aktuellen Datenbank unterstützt werden.|  
|[getUDTs](../content/getUDTs-Method--SQLServerDatabaseMetaData-.md)|Ruft eine Beschreibung der benutzerdefinierten Typen ab, die in einem bestimmten Schema definiert sind.|  
|[getURL](../content/getURL-Method--SQLServerDatabaseMetaData-.md)|Ruft die URL für diese Datenbank ab.|  
|[getUserName](../content/getUserName-Method--SQLServerDatabaseMetaData-.md)|Ruft den Benutzernamen gemäß der Angabe für diese Datenbank ab.|  
|[getVersionColumns](../content/getVersionColumns-Method--SQLServerDatabaseMetaData-.md)|Ruft eine Beschreibung der Spalten einer Tabelle ab, die automatisch aktualisiert wird, wenn ein Wert in einer Zeile aktualisiert wird.|  
|[insertsAreDetected](../content/insertsAreDetected-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob das Einfügen einer sichtbaren Zeile durch Aufrufen der [rowInserted](../content/rowInserted-Method--SQLServerResultSet-.md)\-Methode der [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Klasse ermittelt werden kann.|  
|[isCatalogAtStart](../content/isCatalogAtStart-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob sich ein Katalog am Beginn eines vollqualifizierten Tabellennamens befindet.|  
|[isReadOnly](../content/isReadOnly-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob die Datenbank schreibgeschützt ist.|  
|[locatorsUpdateCopy](../content/locatorsUpdateCopy-Method--SQLServerDatabaseMetaData-.md)|Gibt an, ob Aktualisierungen für ein LOB an einer Kopie oder direkt am LOB vorgenommen werden.|  
|[nullPlusNonNullIsNull](../content/nullPlusNonNullIsNull-Method--SQLServerDatabaseMetaData-.md)|Gibt an, ob von dieser Datenbank unterstützt wird, dass Verkettungen zwischen NULL\-Werten und Werten ungleich NULL einen NULL\-Wert ergeben.|  
|[nullsAreSortedAtEnd](../content/nullsAreSortedAtEnd-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob NULL\-Werte unabhängig von der Sortierreihenfolge am Ende sortiert werden.|  
|[nullsAreSortedAtStart](../content/nullsAreSortedAtStart-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob NULL\-Werte unabhängig von der Sortierreihenfolge am Anfang sortiert werden.|  
|[nullsAreSortedHigh](../content/nullsAreSortedHigh-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob NULL\-Werte bei der Sortierung als hohe Werte behandelt werden.|  
|[nullsAreSortedLow](../content/nullsAreSortedLow-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob NULL\-Werte bei der Sortierung als niedrige Werte behandelt werden.|  
|[othersDeletesAreVisible](../content/othersDeletesAreVisible-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von anderen ausgeführte Löschvorgänge sichtbar sind.|  
|[othersInsertsAreVisible](../content/othersInsertsAreVisible-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von anderen ausgeführte Einfügevorgänge sichtbar sind.|  
|[othersUpdatesAreVisible](../content/othersUpdatesAreVisible-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von anderen ausgeführte Aktualisierungen sichtbar sind.|  
|[ownDeletesAreVisible](../content/ownDeletesAreVisible-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob die eigenen Löschvorgänge eines Resultsets sichtbar sind.|  
|[ownInsertsAreVisible](../content/ownInsertsAreVisible-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob die eigenen Einfügevorgänge eines Resultsets sichtbar sind.|  
|[ownUpdatesAreVisible](../content/ownUpdatesAreVisible-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob die eigenen Aktualisierungen des Resultsets sichtbar sind.|  
|[storesLowerCaseIdentifiers](../content/storesLowerCaseIdentifiers-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob bei SQL\-Bezeichnern mit gemischter Groß\-\/Kleinschreibung, die nicht in Anführungszeichen gesetzt sind, die Groß\-\/Kleinschreibung nicht berücksichtigt wird und die Bezeichner in Kleinbuchstaben gespeichert werden.|  
|[storesLowerCaseQuotedIdentifiers](../content/storesLowerCaseQuotedIdentifiers-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob bei SQL\-Bezeichnern mit gemischter Groß\-\/Kleinschreibung, die in Anführungszeichen gesetzt sind, die Groß\-\/Kleinschreibung nicht berücksichtigt wird und die Bezeichner in Kleinbuchstaben gespeichert werden.|  
|[storesMixedCaseIdentifiers](../content/storesMixedCaseIdentifiers-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob bei SQL\-Bezeichnern mit gemischter Groß\-\/Kleinschreibung, die nicht in Anführungszeichen gesetzt sind, die Groß\-\/Kleinschreibung nicht berücksichtigt wird und die Bezeichner mit gemischter Groß\-\/Kleinschreibung gespeichert werden.|  
|[storesMixedCaseQuotedIdentifiers](../content/storesMixedCaseQuotedIdentifiers-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob bei SQL\-Bezeichnern mit gemischter Groß\-\/Kleinschreibung, die in Anführungszeichen gesetzt sind, die Groß\-\/Kleinschreibung nicht berücksichtigt wird und die Bezeichner mit gemischter Groß\-\/Kleinschreibung gespeichert werden.|  
|[storesUpperCaseIdentifiers](../content/storesUpperCaseIdentifiers-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob bei SQL\-Bezeichnern mit gemischter Groß\-\/Kleinschreibung, die nicht in Anführungszeichen gesetzt sind, die Groß\-\/Kleinschreibung nicht berücksichtigt wird und die Bezeichner in Großbuchstaben gespeichert werden.|  
|[storesUpperCaseQuotedIdentifiers](../content/storesUpperCaseQuotedIdentifiers-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob bei SQL\-Bezeichnern mit gemischter Groß\-\/Kleinschreibung, die in Anführungszeichen gesetzt sind, die Groß\-\/Kleinschreibung nicht berücksichtigt wird und die Bezeichner in Großbuchstaben gespeichert werden.|  
|[supportsAlterTableWithAddColumn](../content/supportsAlterTableWithAddColumn-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank "ALTER TABLE" mit "add column" unterstützt wird.|  
|[supportsAlterTableWithDropColumn](../content/supportsAlterTableWithDropColumn-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank "ALTER TABLE" mit "drop column" unterstützt wird.|  
|[supportsANSI92EntryLevelSQL](../content/supportsANSI92EntryLevelSQL-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank die ANSI92\-SQL\-Einstiegsgrammatik unterstützt wird.|  
|[supportsANSI92FullSQL](../content/supportsANSI92FullSQL-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank die vollständige ANSI92\-SQL\-Grammatik unterstützt wird.|  
|[supportsANSI92IntermediateSQL](../content/supportsANSI92IntermediateSQL-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank die ANSI92\-SQL\-Zwischengrammatik unterstützt wird.|  
|[supportsBatchUpdates](../content/supportsBatchUpdates-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank Batchaktualisierungen unterstützt werden.|  
|[supportsCatalogsInDataManipulation](../content/supportsCatalogsInDataManipulation-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob in einer Datenbearbeitungsanweisung ein Katalogname verwendet werden kann.|  
|[supportsCatalogsInIndexDefinitions](../content/supportsCatalogsInIndexDefinitions-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob in einer Indexdefinitionsanweisung ein Katalogname verwendet werden kann.|  
|[supportsCatalogsInPrivilegeDefinitions](../content/supportsCatalogsInPrivilegeDefinitions-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob in einer Berechtigungsdefinitionsanweisung ein Katalogname verwendet werden kann.|  
|[supportsCatalogsInProcedureCalls](../content/supportsCatalogsInProcedureCalls-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob in einer Prozeduraufrufanweisung ein Katalogname verwendet werden kann.|  
|[supportsCatalogsInTableDefinitions](../content/supportsCatalogsInTableDefinitions-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob in einer Tabellendefinitionsanweisung ein Katalogname verwendet werden kann.|  
|[supportsColumnAliasing](../content/supportsColumnAliasing-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank Spaltenaliasing unterstützt wird.|  
|[supportsConvert](../content/supportsConvert-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank die CONVERT\-Funktion für SQL\-Typen unterstützt wird.|  
|[supportsCoreSQLGrammar](../content/supportsCoreSQLGrammar-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank die ODBC\-SQL\-Kerngrammatik unterstützt wird.|  
|[supportsCorrelatedSubqueries](../content/supportsCorrelatedSubqueries-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank korrelierte Unterabfragen unterstützt werden.|  
|[supportsDataDefinitionAndDataManipulationTransactions](../content/supportsDataDefinitionAndDataManipulationTransactions-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank in einer Transaktion sowohl Datendefinitions\- als auch Datenbearbeitungsanweisungen unterstützt werden.|  
|[supportsDataManipulationTransactionsOnly](../content/supportsDataManipulationTransactionsOnly-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank in einer Transaktion nur Datenbearbeitungsanweisungen unterstützt werden.|  
|[supportsDifferentTableCorrelationNames](../content/supportsDifferentTableCorrelationNames-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob sich abhängige Tabellennamen \(sofern diese unterstützt werden\) von den Namen der Tabellen unterscheiden müssen.|  
|[supportsExpressionsInOrderBy](../content/supportsExpressionsInOrderBy-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank Ausdrücke in ORDER BY\-Listen unterstützt werden.|  
|[supportsExtendedSQLGrammar](../content/supportsExtendedSQLGrammar-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank die erweiterte ODBC\-SQL\-Grammatik unterstützt wird.|  
|[supportsFullOuterJoins](../content/supportsFullOuterJoins-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob geschachtelte äußere Joins von dieser Datenbank vollständig unterstützt werden.|  
|[supportsGetGeneratedKeys](../content/supportsGetGeneratedKeys-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob automatisch generierte Schlüssel nach dem Ausführen einer Anweisung abgerufen werden können.|  
|[supportsGroupBy](../content/supportsGroupBy-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank eine Form der GROUP BY\-Klausel unterstützt wird.|  
|[supportsGroupByBeyondSelect](../content/supportsGroupByBeyondSelect-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank die Verwendung von Spalten, die sich nicht in einer SELECT\-Anweisung befinden, in einer GROUP BY\-Klausel unterstützt wird, wenn gewährleistet ist, dass alle Spalten aus der SELECT\-Anweisung in der GROUP BY\-Klausel enthalten sind.|  
|[supportsGroupByUnrelated](../content/supportsGroupByUnrelated-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank die Verwendung einer Spalte, die sich nicht in der SELECT\-Anweisung befindet, in einer GROUP BY\-Klausel unterstützt wird.|  
|[supportsIntegrityEnhancementFacility](../content/supportsIntegrityEnhancementFacility-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank die SQL\-Integritätserweiterungsfunktion unterstützt wird.|  
|[supportsLikeEscapeClause](../content/supportsLikeEscapeClause-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank das Angeben einer LIKE\-Escapeklausel unterstützt wird.|  
|[supportsLimitedOuterJoins](../content/supportsLimitedOuterJoins-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob äußere Joins von dieser Datenbank in eingeschränktem Maß unterstützt werden.|  
|[supportsMinimumSQLGrammar](../content/supportsMinimumSQLGrammar-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank die minimale ODBC\-SQL\-Grammatik unterstützt wird.|  
|[supportsMixedCaseIdentifiers](../content/supportsMixedCaseIdentifiers-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob bei SQL\-Bezeichnern mit gemischter Groß\-\/Kleinschreibung, die nicht in Anführungszeichen gesetzt sind, die Groß\-\/Kleinschreibung nicht berücksichtigt wird und die Bezeichner mit gemischter Groß\-\/Kleinschreibung gespeichert werden.|  
|[supportsMixedCaseQuotedIdentifiers](../content/supportsMixedCaseQuotedIdentifiers-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob bei SQL\-Bezeichnern mit gemischter Groß\-\/Kleinschreibung, die in Anführungszeichen gesetzt sind, die Groß\-\/Kleinschreibung nicht berücksichtigt wird und die Bezeichner mit gemischter Groß\-\/Kleinschreibung gespeichert werden.|  
|[supportsMultipleOpenResults](../content/supportsMultipleOpenResults-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von einem [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt gleichzeitig mehrere [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Objekte zurückgegeben werden können.|  
|[supportsMultipleResultSets](../content/supportsMultipleResultSets-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank das Abrufen mehrerer [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekte im Zuge eines einzelnen Aufrufs der [execute](../content/execute-Method---.md)\-Methode der [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Klasse unterstützt wird.|  
|[supportsMultipleTransactions](../content/supportsMultipleTransactions-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob bei dieser Datenbank gleichzeitig mehrere Transaktionen für unterschiedliche Verbindungen geöffnet sein können.|  
|[supportsNamedParameters](../content/supportsNamedParameters-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank benannte Parameter in aufrufbaren Anweisungen unterstützt werden.|  
|[supportsNonNullableColumns](../content/supportsNonNullableColumns-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob Spalten in dieser Datenbank als Spalten definiert werden können, in denen keine NULL\-Werte zulässig sind.|  
|[supportsOpenCursorsAcrossCommit](../content/supportsOpenCursorsAcrossCommit-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank unterstützt wird, dass Cursor über Commits hinaus geöffnet bleiben.|  
|[supportsOpenCursorsAcrossRollback](../content/supportsOpenCursorsAcrossRollback-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank unterstützt wird, dass Cursor über Rollbacks hinaus geöffnet bleiben.|  
|[supportsOpenStatementsAcrossCommit](../content/supportsOpenStatementsAcrossCommit-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank unterstützt wird, dass Anweisungen über Commits hinaus geöffnet bleiben.|  
|[supportsOpenStatementsAcrossRollback](../content/supportsOpenStatementsAcrossRollback-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank unterstützt wird, dass Anweisungen über Rollbacks hinaus geöffnet bleiben.|  
|[supportsOrderByUnrelated](../content/supportsOrderByUnrelated-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank die Verwendung einer Spalte, die sich nicht in der SELECT\-Anweisung befindet, in einer ORDER BY\-Klausel unterstützt wird.|  
|[supportsOuterJoins](../content/supportsOuterJoins-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank eine Form von äußeren Joins unterstützt wird.|  
|[supportsPositionedDelete](../content/supportsPositionedDelete-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob positionierte DELETE\-Anweisungen von dieser Datenbank unterstützt werden.|  
|[supportsPositionedUpdate](../content/supportsPositionedUpdate-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob positionierte UPDATE\-Anweisungen von dieser Datenbank unterstützt werden.|  
|[supportsResultSetConcurrency](../content/supportsResultSetConcurrency-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank der angegebene Parallelitätstyp in Kombination mit dem angegebenen Resultsettyp unterstützt wird.|  
|[supportsResultSetHoldability](../content/supportsResultSetHoldability-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank die angegebene Resultsethaltbarkeit unterstützt wird.|  
|[supportsResultSetType](../content/supportsResultSetType-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank der angegebene Resultsettyp unterstützt wird.|  
|[supportsSavepoints](../content/supportsSavepoints-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank Sicherungspunkte unterstützt werden.|  
|[supportsSchemasInDataManipulation](../content/supportsSchemasInDataManipulation-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob in einer Datenbearbeitungsanweisung ein Schemaname verwendet werden kann.|  
|[supportsSchemasInIndexDefinitions](../content/supportsSchemasInIndexDefinitions-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob in einer Indexdefinitionsanweisung ein Schemaname verwendet werden kann.|  
|[supportsSchemasInPrivilegeDefinitions](../content/supportsSchemasInPrivilegeDefinitions-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob in einer Berechtigungsdefinitionsanweisung ein Schemaname verwendet werden kann.|  
|[supportsSchemasInProcedureCalls](../content/supportsSchemasInProcedureCalls-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob in einer Prozeduraufrufanweisung ein Schemaname verwendet werden kann.|  
|[supportsSchemasInTableDefinitions](../content/supportsSchemasInTableDefinitions-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob in einer Tabellendefinitionsanweisung ein Schemaname verwendet werden kann.|  
|[supportsSelectForUpdate](../content/supportsSelectForUpdate-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob positionierte SELECT FOR UPDATE\-Anweisungen von dieser Datenbank unterstützt werden.|  
|[supportsStatementPooling](../content/supportsStatementPooling-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank Anweisungspools unterstützt werden.|  
|[supportsStoredFunctionsUsingCallSyntax](../content/supportsStoredFunctionsUsingCallSyntax-Method--SQLServerDatabaseMetaData-.md)|Gibt an, ob von der aktuellen Datenbank das Aufrufen benutzer\- oder herstellerdefinierter Funktionen mithilfe der Escapesyntax für gespeicherte Prozeduren unterstützt wird.|  
|[supportsStoredProcedures](../content/supportsStoredProcedures-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank gespeicherte Prozeduraufrufe unterstützt werden, bei denen die Escapesyntax für gespeicherte Prozeduren verwendet wird.|  
|[supportsSubqueriesInComparisons](../content/supportsSubqueriesInComparisons-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank Unterabfragen in Vergleichsausdrücken unterstützt werden.|  
|[supportsSubqueriesInExists](../content/supportsSubqueriesInExists-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank Unterabfragen in EXISTS\-Ausdrücken unterstützt werden.|  
|[supportsSubqueriesInIns](../content/supportsSubqueriesInIns-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank Unterabfragen in IN\-Ausdrücken unterstützt werden.|  
|[supportsSubqueriesInQuantifieds](../content/supportsSubqueriesInQuantifieds-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank Unterabfragen in quantifizierten Ausdrücken unterstützt werden.|  
|[supportsTableCorrelationNames](../content/supportsTableCorrelationNames-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob abhängige Tabellennamen von dieser Datenbank unterstützt werden.|  
|[supportsTransactionIsolationLevel](../content/supportsTransactionIsolationLevel-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank die angegebene Transaktionsisolationsstufe unterstützt wird.|  
|[supportsTransactions](../content/supportsTransactions-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank Transaktionen unterstützt werden.|  
|[supportsUnion](../content/supportsUnion-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank "SQL UNION" unterstützt wird.|  
|[supportsUnionAll](../content/supportsUnionAll-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank "SQL UNION ALL" unterstützt wird.|  
|[updatesAreDetected](../content/updatesAreDetected-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob das Aktualisieren einer sichtbaren Zeile durch Aufrufen der [rowUdated](../content/rowUpdated-Method--SQLServerResultSet-.md)\-Methode der [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Klasse ermittelt werden kann.|  
|[usesLocalFilePerTable](../content/usesLocalFilePerTable-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob von dieser Datenbank für jede Tabelle eine Datei verwendet wird.|  
|[usesLocalFiles](../content/usesLocalFiles-Method--SQLServerDatabaseMetaData-.md)|Ruft ab, ob Tabellen von dieser Datenbank in einer lokalen Datei gespeichert werden.|  
  
### Geerbte Methoden  
  
|Klasse geerbt von:|Methoden|  
|------------------------|--------------|  
|java.lang.Object|clone, equals, finalize, getClass, hashCode, notify, notifyAll, toString, wait|  
|java.sql.Wrapper|isWrapperFor, unwrap|  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  