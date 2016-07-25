---
title: "Beispiel f&#252;r den SQLXML-Datentyp"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8f2ff25b-71fd-46d7-b6de-d656095d2aad
caps.latest.revision: 21
caps.handback.revision: 16
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
# Beispiel f&#252;r den SQLXML-Datentyp
  Diese Beispielanwendung für [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] veranschaulicht das Speichern von XML\-Daten in einer relationalen Datenbank, das Abrufen von XML\-Daten aus einer Datenbank sowie das Analysieren von XML\-Daten mit dem Java\-Datentyp **SQLXML**.  
  
 In den Codebeispielen in diesem Abschnitt wird ein SAX \(Simple API for XML\)\-Parser verwendet. SAX ist ein öffentlich entwickelter Standard für die ereignisbasierte Analyse von XML\-Dokumenten. Sie stellt außerdem eine Anwendungsprogrammierschnittstelle für die Arbeit mit XML\-Daten bereit. Beachten Sie, dass in den Anwendungen ebenso jeder andere XML\-Parser wie DOM \(Document Object Model\) oder StAX \(Streaming API for XML\) usw. verwendet werden kann.  
  
 DOM \(Document Object Model\) stellt eine programmgesteuerte Darstellung der XML\-Dokumente, \-Fragmente, \-Knoten oder \-Knotensätze bereit. Es stellt außerdem eine Anwendungsprogrammierschnittstelle für die Arbeit mit XML\-Daten bereit. Entsprechend handelt es sich bei StAX \(Streaming API for XML\) um eine Java\-basierte API für die Pullanalyse von XML.  
  
> [!IMPORTANT]  
>  Um die SAX\-Parser\-API verwenden zu können, müssen Sie die SAX\-Standardimplementierung aus dem Paket "javax.xml" importieren.  
  
 Die Codedatei für dieses Beispiel heißt "sqlxmlExample.java" und befindet sich unter folgendem Pfad:  
  
 \<*Installationsverzeichnis*\>\\sqljdbc\_\<*Version*\>\\\<*Sprache*\>\\help\\samples\\datatypes  
  
## Anforderungen  
 Wenn Sie diese Beispielanwendung ausführen möchten, müssen Sie die Datei "sqljdbc4.jar" in den Klassenpfad aufnehmen. Wenn im Klassenpfad kein Eintrag für "sqljdbc4.jar" vorhanden ist, löst die Beispielanwendung die allgemeine Ausnahme "Klasse nicht gefunden" aus. Weitere Informationen zum Festlegen des Klassenpfads finden Sie unter [Verwenden des JDBC-Treibers](../content/Using-the-JDBC-Driver.md).  
  
 Außerdem benötigen Sie zum Ausführen dieser Beispielanwendung Zugriff auf die [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank.  
  
## Beispiel  
 Der folgende Beispielcode stellt eine Verbindung mit der [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Datenbank her und ruft dann die createSampleTables\-Methode auf.  
  
 Mit der createSampleTables\-Methode werden die Testtabellen TestTable1 und TestTable2 gelöscht, sofern vorhanden. Dann werden zwei Zeilen in TestTable1 eingefügt.  
  
 Darüber hinaus enthält das Codebeispiel die folgenden drei Methoden und eine zusätzliche Klasse mit dem Namen "ExampleContentHandler".  
  
 Die ExampleContentHandler\-Klasse implementiert einen benutzerdefinierten Inhaltshandler, der Methoden für Parserereignisse definiert.  
  
 Die showGetters\-Methode veranschaulicht das Analysieren der Daten im SQLXML\-Objekt mit SAX, ContentHandler und XMLReader. Zunächst erstellt das Codebeispiel eine Instanz eines benutzerdefinierten Inhaltshandlers, dem ExampleContentHandler. Dann wird eine SQL\-Anweisung erstellt und ausgeführt, die einen Datensatz aus TestTable1 zurückgibt. Anschließend werden im Codebeispiel ein SAX\-Parser abgerufen und die XML\-Daten analysiert.  
  
 Die showSetters\-Methode veranschaulicht das Festlegen der **xml**\-Spalte mit SAX, ContentHandler und ResultSet. Zunächst wird mit der [createSQLXML](../content/createSQLXML-Method--SQLServerConnection-.md)\-Methode der Connection\-Klasse ein leeres SQLXML\-Objekt erstellt. Dann wird eine Instanz eines Inhaltshandlers abgerufen, um die Daten in das SQLXML\-Objekt zu schreiben. Anschließend werden die Daten im Codebeispiel in TestTable1 geschrieben. Schließlich durchläuft der Beispielcode die Datenzeilen im Resultset und liest die XML\-Daten mithilfe der [getSQLXML](../content/getSQLXML-Method--SQLServerResultSet-.md)\-Methode.  
  
 Die showTransformer\-Methode veranschaulicht das Abrufen von XML\-Daten aus der einen Tabelle, die dann mit SAX und Transformer in eine andere Tabelle eingefügt werden. Zunächst wird das SQLXML\-Quellobjekt aus TestTable1 abgerufen. Dann wird mit der [createSQLXML](../content/createSQLXML-Method--SQLServerConnection-.md)\-Methode der Connection\-Klasse ein leeres SQLXML\-Zielobjekt erstellt. Daraufhin wird das SQLXML\-Zielobjekt aktualisiert, und die XML\-Daten werden in TestTable2 geschrieben. Schließlich durchläuft der Beispielcode die Datenzeilen im Resultset und liest die XML\-Daten in TestTable2 mithilfe der [getSQLXML](../content/getSQLXML-Method--SQLServerResultSet-.md)\-Methode.  
  
 [!CODE [JDBC#UsingSQLXML1](../CodeSnippet/SQLDrivers/jdbc#usingsqlxml1)]  
  
## Siehe auch  
 [Arbeiten mit Datentypen &#40;JDBC&#41;](../content/Working-with-Data-Types--JDBC-.md)  
  
  