---
title: "Verwenden von gespeicherten Prozeduren mit einer Updatez&#228;hlung"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 64cf4877-5995-4bfc-8865-b7618a5c8d01
caps.latest.revision: 26
caps.handback.revision: 24
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
# Verwenden von gespeicherten Prozeduren mit einer Updatez&#228;hlung
  Zum Ändern von Daten in einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank mit einer gespeicherten Prozedur stellt [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] die [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Klasse bereit. Mithilfe der SQLServerCallableStatement\-Klasse können Sie gespeicherte Prozeduren aufrufen, die Daten in der Datenbank ändern und die Anzahl der betroffenen Zeilen zurückgeben \(die so genannte Updatezählung\).  
  
 Nachdem der Aufruf der gespeicherten Prozedur mit der SQLServerCallableStatement\-Klasse eingerichtet wurde, können Sie die gespeicherte Prozedur mit der [execute](../content/execute-Method--SQLServerStatement-.md)\-Methode oder der [executeUpdate](../content/executeUpdate-Method--SQLServerStatement-.md)\-Methode aufrufen. Die executeUpdate\-Methode gibt im Gegensatz zur execute\-Methode einen **int**\-Wert zurück, der die von der gespeicherten Prozedur betroffenen Zeilen enthält. Wenn Sie die execute\-Methode verwenden und die Anzahl der betroffenen Zeilen ermitteln möchten, können Sie nach dem Ausführen der gespeicherten Prozedur die [getUpdateCount](../content/getUpdateCount-Method--SQLServerStatement-.md)\-Methode aufrufen.  
  
> [!NOTE]  
>  Wenn der JDBC\-Treiber alle Updatezählungen zurückgeben soll, einschließlich der Updatezählungen, die von eventuell ausgelösten Triggern zurückgegeben werden, müssen Sie die lastUpdateCount\-Verbindungseigenschaft auf "false" setzen. Weitere Informationen zur lastUpdateCount\-Eigenschaft finden Sie unter [Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md).  
  
 Erstellen Sie als Beispiel die folgende Tabelle und gespeicherte Prozedur, und fügen Sie Beispieldaten in der [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank ein:  
  
```  
CREATE TABLE TestTable   
   (Col1 int IDENTITY,   
    Col2 varchar(50),   
    Col3 int);  
  
CREATE PROCEDURE UpdateTestTable  
   @Col2 varchar(50),  
   @Col3 int  
AS  
BEGIN  
   UPDATE TestTable  
   SET Col2 = @Col2, Col3 = @Col3  
END;  
INSERT INTO dbo.TestTable (Col2, Col3) VALUES ('b', 10);  
```  
  
 Im folgenden Beispiel wird eine offene Verbindung mit der [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank an die Funktion übergeben, mit der execute\-Methode die gespeicherte Prozedur **UpdateTestTable** aufgerufen und anschließend mit der getUpdateCount\-Methode die Anzahl der von der gespeicherten Prozedur betroffenen Zeilen zurückgegeben.  
  
 [!CODE [JDBC#UsingSprocWithUpdateCount1](../CodeSnippet/SQLDrivers/jdbc#usingsprocwithupdatecount1)]  
  
## Siehe auch  
 [Verwenden von Anweisungen mit gespeicherten Prozeduren](../content/Using-Statements-with-Stored-Procedures.md)  
  
  