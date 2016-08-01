---
title: "Beispiel zum Aktualisieren umfangreicher Daten"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 76ecc05f-a77d-40a2-bab9-91a7fcf17347
caps.latest.revision: 27
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
# Beispiel zum Aktualisieren umfangreicher Daten
  Diese Beispielanwendung für [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] veranschaulicht, wie eine umfangreiche Spalte in einer Datenbank aktualisiert wird.  
  
 Die Codedatei für dieses Beispiel heißt "updateLargeData.java" und befindet sich unter folgendem Pfad:  
  
 \<*Installationsverzeichnis*\>\\sqljdbc\_\<*Version*\>\\\<*Sprache*\>\\help\\samples\\adaptive  
  
## Anforderungen  
 Zum Ausführen dieser Beispielanwendung benötigen Sie Zugriff auf die [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)][!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank. Außerdem müssen Sie die Datei "sqljdbc4.jar" in den Klassenpfad aufnehmen. Wenn im Klassenpfad kein Eintrag für "sqljdbc4.jar" vorhanden ist, löst die Beispielanwendung die allgemeine Ausnahme "Klasse nicht gefunden" aus. Weitere Informationen zum Festlegen des Klassenpfads finden Sie unter [Verwenden des JDBC-Treibers](../content/Using-the-JDBC-Driver.md).  
  
> [!NOTE]  
>  In[!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] sind die Klassenbibliotheksdateien "sqljdbc.jar" und "sqljdbc4.jar" für die jeweilige Verwendung mit den bevorzugten JRE \(Java Runtime Environment\)\-Einstellungen enthalten. Dieses Beispiel verwendet die Methoden [isWrapperFor](../content/isWrapperFor-Method--SQLServerStatement-.md) und [unwrap](../content/unwrap-Method--SQLServerStatement-.md), die in der JDBC 4.0\-API neu eingeführt wurden, für den Zugriff auf die treiberspezifischen Antwortpuffermethoden. Zum Kompilieren und Ausführen dieses Beispiels benötigen Sie die "sqljdbc4.jar"\-Klassenbibliothek, die die Unterstützung für JDBC 4.0 bereitstellt. Weitere Informationen zum Auswählen der richtigen JAR\-Datei finden Sie unter [Systemanforderungen für den JDBC-Treiber](../content/System-Requirements-for-the-JDBC-Driver.md).  
  
## Beispiel  
 Der folgende Beispielcode stellt eine Verbindung zur [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)][!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Datenbank her. Danach wird ein Statement\-Objekt erstellt und mithilfe der [isWrapperFor](../content/isWrapperFor-Method--SQLServerStatement-.md)\-Methode überprüft, ob das Statement\-Objekt ein Wrapper für die angegebene [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Klasse ist. Die [unwrap](../content/unwrap-Method--SQLServerStatement-.md)\-Methode wird für den Zugriff auf treiberspezifische Antwortpuffermethoden verwendet.  
  
 Dann legt der Beispielcode den Antwortpuffermodus auf "**adaptive**" fest. Hierzu wird die [setResponseBuffering](../content/setResponseBuffering-Method--SQLServerStatement-.md)\-Methode der [SQLServerStatement](../content/SQLServerStatement-Class.md).Klasse verwendet. Außerdem wird veranschaulicht, wie der Modus für die adaptive Pufferung abgerufen wird.  
  
 Anschließend wird die SQL\-Anweisung ausgeführt, und die zurückgegebenen Daten werden in ein aktualisierbares [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt eingefügt.  
  
 Schließlich werden die Datenzeilen durchlaufen, die im Resultset enthalten sind. Wenn eine leere Dokumentzusammenfassung erkannt wird, wird die Datenzeile mit einer Kombination aus [updateString](../content/updateString-Method--SQLServerResultSet-.md)\- und [updateRow](../content/updateRow-Method--SQLServerResultSet-.md)\-Methode aktualisiert und erneut in der Datenbank gespeichert. Wenn bereits Daten vorhanden sind, werden einige der enthaltenen Daten mithilfe der [getString](../content/getString-Method--SQLServerResultSet-.md)\-Methode angezeigt.  
  
 Das Standardverhalten des Treibers ist "**adaptive**". Für das aktualisierbare Resultset mit Vorwärtscursor und bei Daten, deren Größe die des Anwendungsspeichers übersteigt, muss der Modus für die adaptive Pufferung von der Anwendung jedoch explizit mithilfe der [setResponseBuffering](../content/setResponseBuffering-Method--SQLServerStatement-.md)\-Methode der [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Klasse festgelegt werden.  
  
 [!CODE [JDBC#UsingAdaptiveBuffering3](../CodeSnippet/SQLDrivers/jdbc#usingadaptivebuffering3)]  
  
## Siehe auch  
 [Arbeiten mit umfangreichen Daten](../content/Working-with-Large-Data.md)  
  
  