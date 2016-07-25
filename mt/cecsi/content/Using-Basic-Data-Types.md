---
title: "Verwenden von Standarddatentypen"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d7044936-5b8c-4def-858c-28a11ef70a97
caps.latest.revision: 73
caps.handback.revision: 72
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
# Verwenden von Standarddatentypen
  [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] verwendet die JDBC\-Standarddatentypen für die Konvertierung der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentypen in ein Format, das von der Programmiersprache Java verarbeitet werden kann, und umgekehrt. Der JDBC\-Treiber bietet Unterstützung für die JDBC 4.0\-API, die den **SQLXML**\-Datentyp und nationale \(Unicode\-\)Datentypen wie **NCHAR**, **NVARCHAR**, **LONGNVARCHAR** und **NCLOB** enthält.  
  
## Datentypzuordnungen  
 Die folgende Tabelle enthält eine Liste der Standardzuordnungen zwischen den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Standarddatentypen sowie den JDBC\- und Java\-Datentypen:  
  
|SQL Server\-Typen|JDBC\-Typen \(java.sql.Types\)|Java\-Typen|  
|-----------------------|------------------------------------|-----------------|  
|bigint|BIGINT|Long|  
|binary|BINARY|byte\[\]|  
|bit|BIT|boolean|  
|char|CHAR|Zeichenfolge|  
|date|DATE|java.sql.Date|  
|datetime|TIMESTAMP|java.sql.Timestamp|  
|datetime2|TIMESTAMP|java.sql.Timestamp|  
|datetimeoffset \(2\)|microsoft.sql.Types.DATETIMEOFFSET|microsoft.sql.DateTimeOffset|  
|decimal|DECIMAL|java.math.BigDecimal|  
|float|DOUBLE|double|  
|image|LONGVARBINARY|byte\[\]|  
|int|INTEGER|int|  
|money|DECIMAL|java.math.BigDecimal|  
|nchar|CHAR<br /><br /> NCHAR \(Java SE 6.0\)|Zeichenfolge|  
|ntext|LONGVARCHAR<br /><br /> LONGNVARCHAR \(Java SE 6.0\)|Zeichenfolge|  
|numeric|NUMERIC|java.math.BigDecimal|  
|nvarchar|VARCHAR<br /><br /> NVARCHAR \(Java SE 6.0\)|Zeichenfolge|  
|nvarchar\(max\)|VARCHAR<br /><br /> NVARCHAR \(Java SE 6.0\)|Zeichenfolge|  
|real|REAL|float|  
|smalldatetime|TIMESTAMP|java.sql.Timestamp|  
|smallint|SMALLINT|short|  
|smallmoney|DECIMAL|java.math.BigDecimal|  
|text|LONGVARCHAR|Zeichenfolge|  
|time|TIME \(1\)|java.sql.Time \(1\)|  
|timestamp|BINARY|byte\[\]|  
|tinyint|TINYINT|short|  
|udt|VARBINARY|byte\[\]|  
|uniqueidentifier|CHAR|Zeichenfolge|  
|varbinary|VARBINARY|byte\[\]|  
|varbinary\(max\)|VARBINARY|byte\[\]|  
||||  
|varchar|VARCHAR|Zeichenfolge|  
|varchar\(max\)|VARCHAR|Zeichenfolge|  
|xml|LONGVARCHAR<br /><br /> LONGNVARCHAR \(Java SE 6.0\)|Zeichenfolge<br /><br /> SQLXML|  
  
 \(1\) Zur Verwendung von java.sql.Time mit dem Zeittyp [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] müssen Sie die Verbindungseigenschaft **sendTimeAsDatetime** auf false setzen.  
  
 \(2\) Mit **datetimeoffset** können Sie programmatisch auf [DateTimeOffset-Klasse](../content/DateTimeOffset-Class.md)\-Werte zugreifen.  
  
 Der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentyp "sqlvariant" wird vom JDBC\-Treiber zurzeit nicht unterstützt. Wenn Daten mit einer Abfrage aus einer Tabelle mit einer Spalte abgerufen werden, die den sqlvariant\-Datentyp enthält, wird eine Ausnahme ausgegeben.  
  
 Die folgenden Abschnitte enthalten Beispiele für die Verwendung des JDBC\-Treibers und der Standarddatentypen. Ein ausführlicheres Beispiel für die Verwendung der Standarddatentypen in einer Java\-Anwendung finden Sie unter [Standarddatentypen - Beispiel](../content/Basic-Data-Types-Sample.md).  
  
## Abrufen von Daten als Zeichenfolge  
 Wenn Sie Daten von einer Datenquelle abrufen müssen, die einem der JDBC\-Standarddatentypen zugeordnet ist und als Zeichenfolge angezeigt werden soll, oder stark typisierte Daten nicht erforderlich sind, können Sie die [getString](../content/getString-Method--SQLServerResultSet-.md)\-Methode der [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Klasse verwenden, wie z. B.:  
  
 [!CODE [JDBC#UsingBasicDataTypes1](../CodeSnippet/SQLDrivers/jdbc#usingbasicdatatypes1)]  
  
## Abrufen von Daten nach Datentyp  
 Wenn Sie Daten von einer Datenquelle abrufen müssen und den Typ der abgerufenen Daten kennen, verwenden Sie eine der get\<Type\>\-Methoden der SQLServerResultSet\-Klasse, die so genannten *Abrufmethoden*. Sie können bei den get\<Type\>\-Methoden einen Spaltennamen oder einen Spaltenindex verwenden, wie im Folgenden dargestellt:  
  
 [!CODE [JDBC#UsingBasicDataTypes2](../CodeSnippet/SQLDrivers/jdbc#usingbasicdatatypes2)]  
  
> [!NOTE]  
>  Die Methoden getUnicodeStream und getBigDecimal mit Skalierung sind veraltet und werden vom JDBC\-Treiber nicht unterstützt.  
  
## Aktualisieren von Daten nach Datentyp  
 Wenn Sie den Wert eines Felds in einer Datenquelle aktualisieren müssen, verwenden Sie eine der update\<Type\>\-Methoden der SQLServerResultSet\-Klasse. Im folgenden Beispiel wird die [updateInt](../content/updateInt-Method--SQLServerResultSet-.md)\-Methode zusammen mit der [updateRow](../content/updateRow-Method--SQLServerResultSet-.md)\-Methode verwendet, um die Daten in der Datenquelle zu aktualisieren:  
  
 [!CODE [JDBC#UsingBasicDataTypes3](../CodeSnippet/SQLDrivers/jdbc#usingbasicdatatypes3)]  
  
> [!NOTE]  
>  Der JDBC\-Treiber kann keine SQL Server\-Spalte mit einem Spaltennamen aktualisieren, dessen Länge mehr als 127 Zeichen beträgt. Wenn ein Update einer Spalte, deren Name mehr als 127 Zeichen umfasst, ausgeführt werden soll, wird eine Ausnahme ausgegeben.  
  
## Aktualisieren von Daten durch parametrisierte Abfragen  
 Wenn Sie Daten in einer Datenquelle durch eine parametrisierte Abfrage aktualisieren müssen, können Sie den Datentyp der Parameter mit einer der set\<Type\>\-Methoden der [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\-Klasse, den so genannten *Festlegungsmethoden*, festlegen. Im folgenden Beispiel werden die parametrisierte Abfrage mit der [prepareStatement](../content/prepareStatement-Method--SQLServerConnection-.md)\-Methode vorkompiliert und dann der string\-Wert des Parameters vor dem Aufrufen der [setString](../content/setString-Method--SQLServerPreparedStatement-.md)\-Methode mit der [executeUpdate](../content/executeUpdate-Method---.md)\-Methode festgelegt.  
  
 [!CODE [JDBC#UsingBasicDataTypes4](../CodeSnippet/SQLDrivers/jdbc#usingbasicdatatypes4)]  
  
 Weitere Informationen zu parametrisierten Abfragen finden Sie unter [Verwenden von SQL-Anweisungen mit Parametern](../content/Using-an-SQL-Statement-with-Parameters.md).  
  
## Übergeben von Parametern an gespeicherte Prozeduren  
 Wenn Sie typisierte Parameter an eine gespeicherte Prozedur übergeben müssen, können Sie die Parameter mit einer der set\<Type\>\-Methoden der [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Klasse anhand eines Namens oder eines Index festlegen. Im folgenden Beispiel werden der Aufruf der gespeicherten Prozedur mit der [prepareCall](../content/prepareCall-Method--SQLServerConnection-.md)\-Methode eingerichtet und dann die Parameter für den Aufruf vor dem Aufrufen der [setString](../content/setString-Method--SQLServerCallableStatement-.md)\-Methode mit der [executeQuery](../content/executeQuery-Method--SQLServerStatement-.md)\-Methode festgelegt.  
  
 [!CODE [JDBC#UsingBasicDataTypes5](../CodeSnippet/SQLDrivers/jdbc#usingbasicdatatypes5)]  
  
> [!NOTE]  
>  In diesem Beispiel wird ein Resultset zurückgegeben, das die Ergebnisse der gespeicherten Prozedur enthält.  
  
 Weitere Informationen zum Verwenden des JDBC\-Treibers mit gespeicherten Prozeduren und Eingabeparametern finden Sie unter [Verwenden von gespeicherten Prozeduren mit Eingabeparametern](../content/Using-a-Stored-Procedure-with-Input-Parameters.md).  
  
## Abrufen von Parametern von gespeicherten Prozeduren  
 Wenn Sie Parameter wieder von einer gespeicherten Prozedur abrufen müssen, müssen Sie zuerst mit der [registerOutParameter](../content/registerOutParameter-Method--SQLServerCallableStatement-.md)\-Methode der SQLServerCallableStatement\-Klasse anhand Name oder Index einen out\-Parameter registrieren und den zurückgegebenen out\-Parameter nach dem Aufruf der gespeicherten Prozedur einer geeigneten Variablen zuordnen. Im folgenden Beispiel werden der Aufruf der gespeicherten Prozedur mit der prepareCall\-Methode eingerichtet, der out\-Parameter mit der registerOutParameter\-Methode eingerichtet und dann die Parameter für den Aufruf vor dem Aufrufen der executeQuery\-Methode mit der [setString](../content/setString-Method--SQLServerCallableStatement-.md)\-Methode festgelegt. Der vom out\-Parameter der gespeicherten Prozedur zurückgegebene Wert wird mit der [getShort](../content/getShort-Method--SQLServerCallableStatement-.md)\-Methode abgerufen.  
  
 [!CODE [JDBC#UsingBasicDataTypes6](../CodeSnippet/SQLDrivers/jdbc#usingbasicdatatypes6)]  
  
> [!NOTE]  
>  Zusätzlich zum zurückgegebenen out\-Parameter kann auch ein Resultset zurückgegeben werden, das die Ergebnisse der gespeicherten Prozedur enthält.  
  
 Weitere Informationen zum Verwenden des JDBC\-Treibers mit gespeicherten Prozeduren und Ausgabeparametern finden Sie unter [Verwenden von gespeicherten Prozeduren mit Ausgabeparametern](../content/Using-a-Stored-Procedure-with-Output-Parameters.md).  
  
## Siehe auch  
 [Grundlegendes zu den Datentypen in JDBC Driver](../content/Understanding-the-JDBC-Driver-Data-Types.md)  
  
  