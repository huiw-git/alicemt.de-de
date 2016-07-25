---
title: "Ausf&#252;hren von Batchvorg&#228;ngen"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1a576d95-7da6-4b7b-8b32-59e5b4d354c4
caps.latest.revision: 22
caps.handback.revision: 19
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
# Ausf&#252;hren von Batchvorg&#228;ngen
  Um die Leistung bei mehreren Updates einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank zu verbessern, bietet [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] die Möglichkeit, mehrere Updates als einzelne Arbeitseinheit \(auch Batch genannt\) zu übermitteln.  
  
 Zum Übermitteln von Batchupdates können die Klassen [SQLServerStatement](../content/SQLServerStatement-Class.md), [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md) und [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md) verwendet werden. Mit der [addBatch](../content/addBatch-Method--SQLServerPreparedStatement-.md)\-Methode können Sie einen Befehl hinzufügen. Mit der [clearBatch](../content/clearBatch-Method--SQLServerPreparedStatement-.md)\-Methode können Sie die Liste der Befehle löschen. Mit der [executeBatch](../content/executeBatch-Method--SQLServerStatement-.md)\-Methode können Sie alle zu verarbeitenden Befehle übermitteln. In einem Batch können nur DDL\- \(Data Definition Language\) und DML\-Anweisungen \(Data Manipulation Language\) ausgeführt werden, die eine einfache Updatezählung zurückgeben.  
  
 Die executeBatch\-Methode gibt ein Array mit **int**\-Werten zurück, die der Updatezählung der einzelnen Befehle entsprechen. Wenn ein Befehl fehlschlägt, wird eine BatchUpdateException ausgegeben. Sie sollten dann mit der getUpdateCounts\-Methode der BatchUpdateException\-Klasse das Array mit den Updatezählungen abrufen. Wenn ein Befehl fehlschlägt, wird die Verarbeitung der restlichen Befehle vom Treiber fortgesetzt. Wenn ein Befehl einen Syntaxfehler enthält, schlagen die Anweisungen im Batch allerdings fehl.  
  
> [!NOTE]  
>  Wenn keine Updatezählungen verwendet werden müssen, können Sie zuerst eine SET NOCOUNT ON\-Anweisung an [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ausgeben. Dadurch wird das Verkehrsaufkommen im Netzwerk verringert und zusätzlich die Leistung der Anwendung verbessert.  
  
 Erstellen Sie als Beispiel die folgende Tabelle in der [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)][!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank:  
  
```  
CREATE TABLE TestTable   
   (Col1 int IDENTITY,   
    Col2 varchar(50),   
    Col3 int);  
```  
  
 Im folgenden Beispiel werden eine offene Verbindung zur [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank an die Funktion übergeben, mit der addBatch\-Methode werden die auszuführenden Anweisungen erstellt, und die executeBatch\-Methode wird aufgerufen, um den Stapel an die Datenbank zu übermitteln.  
  
```  
public static void executeBatchUpdate(Connection con) {  
   try {  
      Statement stmt = con.createStatement();  
      stmt.addBatch("INSERT INTO TestTable (Col2, Col3) VALUES ('X', 100)");  
      stmt.addBatch("INSERT INTO TestTable (Col2, Col3) VALUES ('Y', 200)");  
      stmt.addBatch("INSERT INTO TestTable (Col2, Col3) VALUES ('Z', 300)");  
      int[] updateCounts = stmt.executeBatch();  
      stmt.close();  
   }  
   catch (Exception e) {  
      e.printStackTrace();  
   }  
}  
```  
  
## Siehe auch  
 [Verwenden von Anweisungen mit dem JDBC-Treiber](../content/Using-Statements-with-the-JDBC-Driver.md)  
  
  