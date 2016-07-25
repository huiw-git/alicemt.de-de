---
title: "Beispiel zum Lesen umfangreicher Daten"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6c986144-3854-4352-8331-e79eccbefc28
caps.latest.revision: 28
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
# Beispiel zum Lesen umfangreicher Daten
  Diese Beispielanwendung für [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] veranschaulicht, wie ein großer Wert in einer Spalte mithilfe der [getCharacterStream](../content/getCharacterStream-Method--SQLServerResultSet-.md)\-Methode aus einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank abgerufen wird.  
  
 Die Codedatei für dieses Beispiel heißt **readLargeData.java** und befindet sich unter folgendem Pfad:  
  
 \<*Installationsverzeichnis*\>\\sqljdbc\_\<*Version*\>\\\<*Sprache*\>\\help\\samples\\adaptive  
  
## Anforderungen  
 Zum Ausführen dieser Beispielanwendung benötigen Sie Zugriff auf die [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank. Außerdem müssen Sie die Datei **sqljdbc.jar** oder **sqljdbc4.jar** in den Klassenpfad aufnehmen. Wenn im Klassenpfad kein Eintrag für **sqljdbc.jar** oder **sqljdbc4.jar** vorhanden ist, löst die Beispielanwendung die allgemeine Ausnahme "Klasse nicht gefunden" aus. Weitere Informationen zum Festlegen des Klassenpfads finden Sie unter [Verwenden des JDBC-Treibers](../content/Using-the-JDBC-Driver.md).  
  
> [!NOTE]  
>  [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] enthält die Klassenbibliotheksdateien "sqljdbc.jar" und "sqljdbc4.jar" für die jeweilige Verwendung mit den bevorzugten JRE \(Java Runtime Environment\)\-Einstellungen. Weitere Informationen zum Auswählen der richtigen JAR\-Datei finden Sie unter [Systemanforderungen für den JDBC-Treiber](../content/System-Requirements-for-the-JDBC-Driver.md).  
  
## Beispiel  
 Der folgende Beispielcode stellt eine Verbindung zur [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Datenbank her. Im Beispielcode werden anschließend Beispieldaten erstellt, und die Tabelle **Production.Document** wird mithilfe einer parametrisierten Abfrage aktualisiert.  
  
 Außerdem wird im Beispielcode veranschaulicht, wie der Modus für die adaptive Pufferung mithilfe der [getResponseBuffering](../content/getResponseBuffering-Method--SQLServerStatement-.md)\-Methode der [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Klasse abgerufen wird. Beachten Sie, dass ab Version 2.0 des JDBC\-Treibers die **responseBuffering**\-Verbindungseigenschaft standardmäßig auf "adaptive" festgelegt ist.  
  
 Anschließend wird im Beispielcode eine SQL\-Anweisung mit dem [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt verwendet. Die SQL\-Anweisung wird ausgeführt, und die zurückgegebenen Daten werden in ein [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt eingefügt.  
  
 Schließlich durchläuft der Beispielcode die Datenzeilen im Resultset und greift mithilfe der [getCharacterStream](../content/getCharacterStream-Method--SQLServerResultSet-.md)\-Methode auf einige der darin enthaltenen Daten zu.  
  
 [!CODE [JDBC#UsingAdaptiveBuffering1](../CodeSnippet/SQLDrivers/jdbc#usingadaptivebuffering1)]  
  
## Siehe auch  
 [Arbeiten mit umfangreichen Daten](../content/Working-with-Large-Data.md)  
  
  