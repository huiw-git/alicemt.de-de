---
title: "JDBC 4.1-Kompatibilit&#228;t f&#252;r den JDBC-Treiber"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f087fd40-8451-478e-b465-43112c711515
caps.latest.revision: 6
caps.handback.revision: 5
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
# JDBC 4.1-Kompatibilit&#228;t f&#252;r den JDBC-Treiber
    
> [!NOTE]  
>  Versionen von Microsoft JDBC Driver für SQL Server vor Version 4.2 sind mit der Java Database Connectivity API 4.0\-Spezifikation kompatibel. Dieser Abschnitt trifft auf Versionen vor der Version 4.2 nicht zu.  
  
 Die Java Database Connectivity API 4.1\-Spezifikation wird von Microsoft JDBC Driver 4.2 für SQL Server mit den folgenden API\-Methoden unterstützt.  
  
 **SQLServerConnection\-Klasse**  
  
|Methode „New“|Beschreibung|JDBC\-Treiber\-Implementierung|  
|-------------------|------------------|------------------------------------|  
|void abort\(Executor executor\)|Beendet eine geöffnete Verbindung mit SQL Server.|Wird wie unter der java.sql.Connection\-Schnittstelle beschrieben implementiert. Weitere Details finden Sie unter [java.sql.Connection](http://docs.oracle.com/javase/7/docs/api/java/sql/Connection.html).|  
|void setSchema\(String schema\)|Legt das Schema für die aktuelle Verbindung fest.|SQL Server unterstützt das Festlegen des Schemas für die aktuelle Sitzung nicht. Der Treiber protokolliert stumm eine Warnmeldung, wenn diese Methode aufgerufen wird. Weitere Details finden Sie unter [java.sql.Connection](http://docs.oracle.com/javase/7/docs/api/java/sql/Connection.html).|  
|String „getSchema\(\)“|Gibt den Schemanamen für die aktuelle Verbindung zurück.|Da SQL Server das Festlegen des Schemas für die aktuelle Verbindung nicht unterstützt, gibt der Treiber stattdessen das Standardschema des Benutzers zurück. Weitere Details finden Sie unter [java.sql.Connection](http://docs.oracle.com/javase/7/docs/api/java/sql/Connection.html).|  
  
 **SQLServerDatabaseMetaData\-Klasse**  
  
|Methode „New“|Beschreibung|JDBC\-Treiber\-Implementierung|  
|-------------------|------------------|------------------------------------|  
|boolean generatedKeyAlwaysReturned\(\)|Gibt „true“ zurück, da der Treiber das Abrufen von generierten Schlüsseln unterstützt|Wird wie für java.sql beschrieben implementiert. DatabaseMetaData\-Schnittstelle. Weitere Details finden Sie unter [java.sql.DatabaseMetaData](http://docs.oracle.com/javase/7/docs/api/java/sql/DatabaseMetaData.html).|  
|ResultSet getPseudoColumns\(String catalog, String schemaPattern,String tableNamePattern,String columnNamePattern\)|Ruft eine Beschreibung der Pseudospalten bzw. ausgeblendeten Spalten ab|Gibt eine leere Ergebnismenge zurück, da Pseudospalten in SQL Server formal nicht definiert sind. Weitere Details finden Sie unter [java.sql.DatabaseMetaData](http://docs.oracle.com/javase/7/docs/api/java/sql/DatabaseMetaData.html).|  
  
 **SQLServerStatement\-Klasse**  
  
|Methode „New“|Beschreibung|JDBC\-Treiber\-Implementierung|  
|-------------------|------------------|------------------------------------|  
|void closeOnCompletion\(\)|Gibt an, dass diese Anweisung geschlossen wird, wenn alle ihre abhängigen Resultsets geschlossen werden.|Wird wie unter der java.sql.Statement\-Schnittstelle beschrieben implementiert. Weitere Details finden Sie unter [java.sql.Statement](http://docs.oracle.com/javase/7/docs/api/java/sql/Statement.html).|  
|boolean isCloseOnCompletion\(\)|Gibt einen Wert zurück, der anzeigt, ob diese Anweisung geschlossen wird, wenn alle ihre abhängigen Resultsets geschlossen werden.|Wird wie unter der java.sql.Statement\-Schnittstelle beschrieben implementiert. Weitere Details finden Sie unter [java.sql.Statement](http://docs.oracle.com/javase/7/docs/api/java/sql/Statement.html).|  
  
 Die Java Database Connectivity API 4.1\-Spezifikation wird von Microsoft JDBC Driver 4.2 für SQL Server mit den folgenden Funktionen unterstützt.  
  
|Neue Funktion|Beschreibung|  
|-------------------|------------------|  
|Neue Escape\-Funktion<br /><br /> Limited Return Rows Escape|Teilweise unterstützt<br /><br /> Escape\-Syntax: LIMIT \<rows\> \[OFFSET \<row\_offset\>\]<br /><br /> Die Escape\-Syntax besteht aus zwei Teilen: der obligatorische Teil ‚rows‘ gibt die Anzahl der zurückzugebenden Zeichen zurück, der optionale Teil ‚row\_offset‘ gibt die Anzahl der zu überspringenden Zeilen vor dem Beginn der Rückgabe an<br /><br /> Der Treiber unterstützt nur den obligatorischen Teil, indem er die Abfrage für die Verwendung von ‚TOP‘ anstelle von ‚LIMIT‘ transformiert \(SQL Server unterstützt ‚LIMIT‘ nicht\).<br /><br /> Der Treiber löst eine Ausnahme aus, wenn der optionale Teil ‚row\_offset‘ verwendet wird, da SQL Server nicht über ein Konstrukt zur Unterstützung dieser Anweisung verfügt.<br /><br /> Details finden Sie unter [Verwenden von SQL\-Escapesequenzen](https://msdn.microsoft.com/en-us/library/ms378045.aspx).|  
  
 Die Java Database Connectivity API 4.1\-Spezifikation wird von Microsoft JDBC Driver 4.2 für SQL Server mit den folgenden Datentypzuordnungen unterstützt.  
  
|Datentypzuordnungen|Beschreibung|  
|-------------------------|------------------|  
|In den Methoden „PreparedStatement.setObject\(\)“ und „PreparedStatement.setNull\(\)“ werden jetzt neue Datentypzuordnungen unterstützt.|1. Neue Java\- zu JDBC\-Typzuordnung<br /><br /> \(a\) java.math.BigInteger zu JDBC BIGINT<br /><br /> \(b\) java.util.Date und java.util.Calendar zu JDBC TIMESTAMP<br /><br /> 2. Neue Datentypkonvertierungen:<br /><br /> \(a\) java.math.BigInteger zu CHAR, VARCHAR, LONGVARCHAR und BIGINT<br /><br /> \(b\) java.util.Date und java.util.Calendar zu CHAR, VARCHAR, LONGVARCHAR, DATE, TIME und TIMESTAMP<br /><br /> Weitere Informationen finden Sie in der JDBC 4.1\-Spezifikation.|  
  
  