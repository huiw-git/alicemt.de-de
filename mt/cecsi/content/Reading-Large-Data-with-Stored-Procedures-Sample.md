---
title: "Beispiel zum Lesen umfangreicher Daten mit gespeicherten Prozeduren"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 58c76635-a117-4661-8781-d6cb231c5809
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
# Beispiel zum Lesen umfangreicher Daten mit gespeicherten Prozeduren
  In dieser Beispielanwendung für [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] wird das Abrufen eines großen OUT\-Parameters aus einer gespeicherten Prozedur veranschaulicht.  
  
 Die Codedatei für dieses Beispiel heißt **executeStoredProcedure.java** und befindet sich unter folgendem Pfad:  
  
 \<*Installationsverzeichnis*\>\\sqljdbc\_\<*Version*\>\\\<*Sprache*\>\\help\\samples\\adaptive  
  
## Anforderungen  
 Zum Ausführen dieser Beispielanwendung benötigen Sie Zugriff auf die [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank. Außerdem müssen Sie die Datei **sqljdbc.jar** oder **sqljdbc4.jar** in den Klassenpfad aufnehmen. Wenn im Klassenpfad kein Eintrag für **sqljdbc.jar** oder **sqljdbc4.jar** vorhanden ist, löst die Beispielanwendung die allgemeine Ausnahme "Klasse nicht gefunden" aus. Weitere Informationen zum Festlegen des Klassenpfads finden Sie unter [Verwenden des JDBC-Treibers](../content/Using-the-JDBC-Driver.md).  
  
> [!NOTE]  
>  [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] enthält die Klassenbibliotheksdateien "sqljdbc.jar" und "sqljdbc4.jar" für die jeweilige Verwendung mit den bevorzugten JRE \(Java Runtime Environment\)\-Einstellungen. Weitere Informationen zum Auswählen der richtigen JAR\-Datei finden Sie unter [Systemanforderungen für den JDBC-Treiber](../content/System-Requirements-for-the-JDBC-Driver.md).  
  
 Außerdem müssen Sie die folgende Prozedur in der [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank erstellen:  
  
```  
CREATE PROCEDURE GetLargeDataValue   
  (@Document_ID int,   
   @Document_ID_out int OUTPUT,   
   @Document_Title varchar(50) OUTPUT,  
   @Document_Summary nvarchar(max) OUTPUT)  
  
AS   
BEGIN    
   SELECT @Document_ID_out = DocumentID,   
          @Document_Title = Title,  
          @Document_Summary = DocumentSummary   
    FROM  Production.Document  
    WHERE DocumentID = @Document_ID  
END  
```  
  
## Beispiel  
 Der folgende Beispielcode stellt eine Verbindung zur [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Datenbank her. Im Beispielcode werden anschließend Beispieldaten erstellt, und die Tabelle **Production.Document** wird mithilfe einer parametrisierten Abfrage aktualisiert. Dann ruft der Beispielcode den Modus für die adaptive Pufferung mithilfe der [getResponseBuffering](../content/getResponseBuffering-Method--SQLServerStatement-.md)\-Methode der [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Klasse ab und führt die gespeicherte GetLargeDataValue\-Prozedur aus. Beachten Sie, dass ab Version 2.0 des JDBC\-Treibers die **responseBuffering**\-Verbindungseigenschaft standardmäßig auf "adaptive" festgelegt ist.  
  
 Schließlich zeigt der Beispielcode die mit den OUT\-Parametern zurückgegebenen Daten an. Darüber hinaus wird die Verwendung der `mark`\-Methode und der `reset`\-Methode im Datenstrom zum erneuten Lesen eines beliebigen Teils der Daten veranschaulicht.  
  
 [!CODE [JDBC#UsingAdaptiveBuffering2](../CodeSnippet/SQLDrivers/jdbc#usingadaptivebuffering2)]  
  
## Siehe auch  
 [Arbeiten mit umfangreichen Daten](../content/Working-with-Large-Data.md)  
  
  