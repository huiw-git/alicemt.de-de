---
title: "Programmieren mit SQLXML"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4d2cc57c-7293-4d92-b8b1-525e2b35f591
caps.latest.revision: 23
caps.handback.revision: 22
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
# Programmieren mit SQLXML
  In diesem Abschnitt wird beschrieben, wie Sie die API\-Methoden von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] zum Speichern und Abrufen eines XML\-Dokuments in bzw. aus einer relationalen Datenbank mit **SQLXML**\-Objekten verwenden.  
  
 Außerdem sind Informationen über die Typen von SQLXML\-Objekten und eine Liste wichtiger Richtlinien und Einschränkungen für die Verwendung von SQLXML\-Objekten enthalten.  
  
## Lesen und Schreiben von XML\-Daten mit SQLXML\-Objekten  
 In der folgenden Liste ist aufgeführt, wie Sie die API\-Methoden von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] zum Lesen und Schreiben von XML\-Daten mit SQLXML\-Objekten verwenden.  
  
-   Zum Erstellen eines SQLXML\-Objekts verwenden Sie die [createSQLXML](../content/createSQLXML-Method--SQLServerConnection-.md)\-Methode der [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Klasse. Beachten Sie, dass mit dieser Methode ein SQLXML\-Objekt ohne Daten erstellt wird. Rufen Sie eine der folgenden, in der SQLXML\-Schnittstelle definierten Methoden auf, um dem SQLXML\-Objekt **xml**\-Daten hinzuzufügen: setResult, setCharacterStream, setBinaryStream oder setString.  
  
-   Zum Abrufen des eigentlichen SQLXML\-Objekts verwenden Sie die getSQLXML\-Methoden der [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Klasse oder der [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Klasse.  
  
-   Verwenden Sie eine der folgenden, in der SQLXML\-Schnittstelle definierten Methoden, um **xml**\-Daten aus dem SQLXML\-Objekt abzurufen: getSource, getCharacterStream, getBinaryStream oder getString.  
  
-   Zum Aktualisieren der **xml**\-Daten in einem SQLXML\-Objekt verwenden Sie die [updateSQLXML](../content/updateSQLXML-Method--SQLServerResultSet-.md)\-Methode der [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Klasse.  
  
-   Zum Speichern eines SQLXML\-Objekts in einer Datenbank\-Tabellenspalte vom Typ **xml** verwenden Sie die setSQLXML\-Methoden der [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\-Klasse oder der [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Klasse.  
  
 Der Beispielcode im [Beispiel für den SQLXML\-Datentyp](../content/SQLXML-Data-Type-Sample.md) veranschaulicht die Ausführung dieser allgemeinen API\-Aufgaben.  
  
## Lesbare und schreibbare SQLXML\-Objekte  
 In der folgenden Tabelle sind die Typen von SQLXML\-Objekten aufgeführt, die von den von der JDBC\-API bereitgestellten Methoden zum Festlegen, Abrufen und Aktualisieren unterstützt werden. Die Spalten der Tabelle haben die folgende Bedeutung:  
  
-   In der Spalte **Methodenname** werden die unterstützten Methoden zum Abrufen, Festlegen und Aktualisieren in der JDBC\-API aufgeführt.  
  
-   Die Spalte **SQLXML\-Abrufobjekt** stellt ein SQLXML\-Objekt dar, das entweder mit der [getSQLXML](../content/getSQLXML-Method--SQLServerCallableStatement-.md)\-Methode der [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Klasse oder der [getSQLXML](../content/getSQLXML-Method--SQLServerResultSet-.md)\-Methode der [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Klasse erstellt wird.  
  
-   Die Spalte **SQLXML\-Festlegungsobjekt** stellt ein SQLXML\-Objekt dar, das von der [createSQLXML](../content/createSQLXML-Method--SQLServerConnection-.md)\-Methode der [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Klasse erstellt wird. Beachten Sie, dass die unten aufgeführten Festlegungsmethoden nur ein von der [createSQLXML](../content/createSQLXML-Method--SQLServerConnection-.md)\-Methode erstelltes SQLXML\-Objekt akzeptieren.  
  
|Methodenname|SQLXML\-Abrufobjekt<br /><br /> \(Lesbar\)|SQLXML\-Festlegungsobjekt<br /><br /> \(Schreibbar\)|  
|------------------|----------------------------------------|--------------------------------------------------|  
|CallableStatement.setSQLXML\(\)|Nicht unterstützt|Unterstützt|  
|CallableStatement.setObject\(\)|Nicht unterstützt|Unterstützt|  
|PreparedStatement.setSQLXML\(\)|Nicht unterstützt|Unterstützt|  
|PreparedStatement.setObject\(\)|Nicht unterstützt|Unterstützt|  
|ResultSet.updateSQLXML\(\)|Nicht unterstützt|Unterstützt|  
|ResultSet.updateObject\(\)|Nicht unterstützt|Unterstützt|  
|ResultSet.getSQLXML\(\)|Unterstützt|Nicht unterstützt|  
|CallableStatement.getSQLXML\(\)|Unterstützt|Nicht unterstützt|  
  
 Wie in der Tabelle oben angegeben ist, können die SQLXML\-Festlegungsmethoden nicht mit den lesbaren SQLXML\-Objekten verwendet werden. Entsprechend können die Abrufmethoden nicht mit den schreibbaren SQLXML\-Objekten verwendet werden.  
  
 Wenn die setObject\-Methode von der Anwendung durch Angeben eines Skalierungs\- oder Längenparameters mit einem SQLXML\-Objekt aufgerufen wird, wird der Skalierungs\- oder Längenparameter ignoriert.  
  
## Richtlinien und Einschränkungen für die Verwendung von SQLXML\-Objekten  
 Anwendungen können mit SQLXML\-Objekten XML\-Daten aus einer Datenbank lesen oder in diese schreiben. Die folgende Liste enthält Informationen über bestimmte Einschränkungen und Richtlinien für die Verwendung von SQLXML\-Objekten.  
  
-   Ein SQLXML\-Objekt kann nur für die Dauer der Transaktion gültig sein, für die es erstellt wurde.  
  
-   Ein von einer Abrufmethode empfangenes SQLXML\-Objekt kann nur zum Lesen von Daten verwendet werden.  
  
-   Ein vom Verbindungsobjekt erstelltes SQLXML\-Objekt kann nur zum Schreiben von Daten verwendet werden.  
  
-   Die Anwendung kann zum Lesen von Daten nur eine Abrufmethode für ein lesbares SQLXML\-Objekt aufrufen. Nach dem Aufruf der Abrufmethode führen alle weiteren Abruf\- oder Festlegungsmethoden für das gleiche SQLXML\-Objekt zu einem Fehler.  
  
-   Die Anwendung kann nur die free\-Methode für das SQLXML\-Objekt aufrufen, nachdem für dieses ein Lese\- oder Schreibvorgang ausgeführt wurde. Es ist jedoch weiterhin möglich, den zurückgegebenen Datenstrom oder die zurückgegebene Quelle zu verarbeiten, solange die zugrunde liegende Spalte oder der zugrunde liegende Parameter aktiv ist. Wenn die zugrunde liegende Spalte oder der zugrunde liegende Parameter nicht mehr aktiv ist, wird der Datenstrom oder die Quelle geschlossen, der bzw. die dem SQLXML\-Objekt zugeordnet ist. Wenn die zugrunde liegende Spalte oder der zugrunde liegende Parameter nicht mehr gültig ist, stehen die zugrunde liegenden Daten den Abrufmethoden des Datenstroms, der SAX \(Simple API for XML\) und der StAX \(Streaming API for XML\) nicht zur Verfügung.  
  
-   Die Anwendung kann nur eine Festlegungsmethode für ein schreibbares SQLXML\-Objekt aufrufen. Nach dem Aufruf der Festlegungsmethode führen alle weiteren Abruf\- oder Festlegungsmethoden für das gleiche SQLXML\-Objekt zu einem Fehler.  
  
-   Damit Daten für das SQLXML\-Objekt festgelegt werden können, muss die Anwendung die entsprechende Festlegungsmethode und die Funktionen im zurückgegebenen Objekt verwenden.  
  
-   Die getSQLXML\-Methoden der [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Klasse und der [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Klasse geben **null**\-Daten zurück, wenn die zugrunde liegende Spalte **null** ist.  
  
-   Die Festlegungsobjekte können für die Dauer der Verbindung gültig sein, in der sie erstellt wurden.  
  
-   Es ist nicht zulässig, dass Anwendungen mithilfe der von der SQLXML\-Schnittstelle bereitgestellten Festlegungsmethoden einen **null**\-Wert festlegen. Die Anwendungen können mithilfe der von der SQLXML\-Schnittstelle bereitgestellten Festlegungsmethoden eine leere Zeichenfolge \(""\) festlegen. Zum Festlegen eines **null**\-Werts müssen die Anwendungen eine der folgenden Methoden aufrufen:  
  
    -   Die setNull\-Methoden der [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Klasse und der [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\-Klasse.  
  
    -   Die setObject\-Methoden der [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Klasse und der [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\-Klasse.  
  
    -   Die setSQLXML\-Methoden der [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Klasse und der [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\-Klasse mit einem **null**\-Parameterwert.  
  
-   Für die Arbeit mit XML\-Dokumenten wird aus Leistungsgründen die Verwendung der SAX \(Simple API for XML\)\- und StAX \(Streaming API for XML\)\-Parser anstelle von DOM \(Document Object Model\)\-Parsern empfohlen.  
  
 XML\-Parser können leere Werte nicht behandeln. SQL Server erlaubt Anwendungen jedoch das Abrufen und Speichern leerer Werte aus bzw. in Datenbankspalten mit dem XML\-Datentyp. Dies bedeutet, dass beim Analysieren der XML\-Daten vom Parser eine Ausnahme ausgelöst wird, wenn der zugrunde liegende Wert leer ist. Bei DOM\-Ausgaben fängt der JDBC\-Treiber die Ausnahme ab und löst einen Fehler aus. Bei SAX\- und StAX\-Ausgaben stammt der Fehler direkt vom Parser.  
  
## Adaptive Pufferung und SQLXML\-Unterstützung  
 Die vom SQLXML\-Objekt zurückgegebenen Binär\- und Zeichendatenströme richten sich nach den Modi für die adaptive oder vollständige Pufferung. Wenn die XML\-Parser hingegen keine Datenströme sind, berücksichtigen sie die Einstellungen für adaptive oder vollständige Pufferung nicht. Weitere Informationen zur adaptiven Pufferung finden Sie unter [Verwenden der adaptiven Pufferung](../content/Using-Adaptive-Buffering.md).  
  
## Siehe auch  
 [Unterstützen von XML-Daten](../content/Supporting-XML-Data.md)  
  
  