---
title: "getFunctionColumns-Methode (SQLServerDatabaseMetaData)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e2b0e0f7-717c-48e6-bcd2-a325d938a833
caps.latest.revision: 27
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
# getFunctionColumns-Methode (SQLServerDatabaseMetaData)
  Ruft eine Beschreibung der System\- oder Benutzerfunktionsparameter des angegebenen Katalogs sowie den Rückgabetyp ab.  
  
## Syntax  
  
```  
  
public ResultSet getFunctionColumns(java.lang.String catalog,  
                       java.lang.String schemaPattern,  
                       java.lang.String functionNamePattern  
                       java.lang.String columnNamePattern)  
```  
  
#### Parameter  
 *catalog*  
  
 Ein **String** mit dem Katalognamen. Bei einer leeren Zeichenfolge \(""\) enthält das Ergebnis die Funktionen ohne einen Katalog. Bei **null** wird der Katalogname nicht für die Suche verwendet.  
  
 *schemaPattern*  
  
 Ein **String** mit dem Schemanamenmuster. Bei einer leeren Zeichenfolge \(""\) enthält das Ergebnis die Funktionen ohne ein Schema. Bei **null** wird der Schemaname nicht für die Suche verwendet.  
  
 *functionNamePattern*  
  
 Ein **String** mit dem Namen einer Funktion.  
  
 *columnNamePattern*  
  
 Ein **String** mit dem Namen eines Parameters.  
  
## Rückgabewert  
 Ein [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getFunctionColumns\-Methode wird von der getFunctionColumns\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
 Von dieser Methode werden nur die Funktionen und Parameter zurückgegeben, die dem angegebenen Schema, Funktions\- und Parameternamen innerhalb des angegebenen Katalogs entsprechen.  
  
 Jede Zeile im Resultset enthält die folgenden Spalten für eine Parameterbeschreibung, eine Spaltenbeschreibung oder einen Rückgabetyp:  
  
|Name|Typ|Beschreibung|  
|----------|---------|------------------|  
|FUNCTION\_CAT|**String**|Der Name der Datenbank, in der die Funktion gespeichert ist.|  
|FUNCTION\_SCHEM|**String**|Das Schema für die Funktion.|  
|FUNCTION\_NAME|**String**|Der Name der Funktion.|  
|COLUMN\_NAME|**String**|Der Name eines Parameters oder einer Spalte.|  
|COLUMN\_TYPE|**short**|Der Typ der Spalte. Mögliche Werte:<br /><br /> -   functionColumnUnknown \(0\): Unbekannter Typ<br />-   functionColumnIn \(1\): Eingabeparameter<br />-   functionColumnInOut \(2\): Eingabe\-\/Ausgabeparameter<br />-   functionColumnOut \(3\): Ausgabeparameter<br />-   functionReturn \(4\): Funktionsrückgabewert<br />-   functionColumnResult \(5\): Ein Parameter oder eine Spalte ist eine Spalte im Resultset.|  
|DATA\_TYPE|**smallint**|Der SQL\-Datentypwert aus Java.sql.Types.|  
|TYPE\_NAME|**String**|Der Name des Datentyps.|  
|PRECISION|**int**|Die Gesamtanzahl von signifikanten Stellen.|  
|LENGTH|**int**|Die Länge der Daten in Bytes.|  
|SCALE|**short**|Die Anzahl von Stellen rechts des Dezimalzeichens.|  
|RADIX|**short**|Die Basis für numerische Typen.|  
|NULLABLE|**short**|Gibt an, ob der Parameter\- oder Rückgabewert einen **null**\-Wert enthalten kann.<br /><br /> Mögliche Werte:<br /><br /> -   functionNoNulls \(0\): NULL\-Wert ist nicht zulässig.<br />-   functionNullable \(1\): NULL\-Wert ist zulässig.<br />-   functionNullableUnknown \(2\): Unbekannt|  
|REMARKS|**String**|Die Kommentare zu einer Spalte oder einem Parameter.|  
|COLUMN\_DEF|**String**|Der Standardwert der Spalte. **Note:**  Diese Angabe ist in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verfügbar und JDBC\-Treiber\-spezifisch.|  
|SQL\_DATA\_TYPE|**smallint**|Diese Spalte entspricht \(mit Ausnahme der Datentypen **datetime** und ISO **interval**\) der **DATA\_TYPE**\-Spalte. **Note:**  Diese Angabe ist in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verfügbar und JDBC\-Treiber\-spezifisch.|  
|SQL\_DATETIME\_SUB|**smallint**|Der Subcode für **datetime** ISO **interval**, wenn der Wert von **SQL\_DATA\_TYPE** dem Wert **SQL\_DATETIME** oder **SQL\_INTERVAL** entspricht. Bei allen anderen Datentypen außer **datetime** und ISO **interval** ist diese Spalte NULL. **Note:**  Diese Angabe ist in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verfügbar und JDBC\-Treiber\-spezifisch.|  
|CHAR\_OCTET\_LENGTH|**int**|Die maximale Länge von binären oder zeichenbasierten Parametern oder Spalten. Für andere Datentypen ist der Wert NULL.|  
|ORDINAL\_POSITION|**int**|Stellt für Eingabe\- und Ausgabeparameter die Position \(beginnend mit "1"\) dar.<br /><br /> Für Resultsetspalten handelt es sich hierbei um die Position der Spalte im Resultset. Beginn ist der Wert "1".<br /><br /> Für den Rückgabewert ist der Wert "0".|  
|IS\_NULLABLE|**String**|Bestimmt die NULL\-Zulässigkeit eines Parameters oder einer Spalte.<br /><br /> Mögliche Werte:<br /><br /> **YES**: Der Parameter oder die Spalte kann NULL\-Werte enthalten.<br /><br /> **NO**: Der Parameter oder die Spalte kann keine NULL\-Werte enthalten.<br /><br /> Leere Zeichenfolge \(""\): Unbekannt|  
|SS\_TYPE\_CATALOG\_NAME|**String**|Der Name des Katalogs, der den benutzerdefinierten Typ \(UDT\) enthält.|  
|SS\_TYPE\_SCHEMA\_NAME|**String**|Der Name des Schemas, der den benutzerdefinierten Typ \(UDT\) enthält.|  
|SS\_UDT\_CATALOG\_NAME|**String**|Der benutzerdefinierte Typ \(UDT\) für den vollqualifizierten Namen.|  
|SS\_UDT\_SCHEMA\_NAME|**String**|Der Name des Katalogs, in dem eine XML\-Schemaauflistung definiert ist. Wenn der Katalogname nicht gefunden werden kann, enthält diese Variable eine leere Zeichenfolge.|  
|SS\_UDT\_ASSEMBLY\_TYPE\_NAME|**String**|Der Name des Schemas, in dem eine XML\-Schemaauflistung definiert ist. Wenn der Schemaname nicht gefunden werden kann, handelt es sich dabei um eine leere Zeichenfolge.|  
|SS\_XML\_SCHEMACOLLECTION\_CATALOG\_NAME|**String**|Name der XML\-Schemaauflistung. Wenn der Schemaname nicht gefunden werden kann, handelt es sich dabei um eine leere Zeichenfolge.|  
|SS\_XML\_SCHEMACOLLECTION\_SCHEMA\_NAME|**String**|Der Name des Katalogs, der den benutzerdefinierten Typ \(UDT\) enthält.|  
|SS\_XML\_SCHEMACOLLECTION\_NAME|**String**|Der Name des Schemas, der den benutzerdefinierten Typ \(UDT\) enthält.|  
|SS\_DATA\_TYPE|**tinyint**|Der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentyp, der von erweiterten gespeicherten Prozeduren verwendet wird.<br /><br /> **Hinweis** Weitere Informationen zu den Datentypen, die von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] zurückgegeben werden, finden Sie in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation unter "Datentypen \(Transact\-SQL\)".|  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  