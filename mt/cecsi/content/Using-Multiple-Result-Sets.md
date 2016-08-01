---
title: "Verwenden von mehreren Resultsets"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ab6a3cfa-073b-44e9-afca-a8675cfe5fd1
caps.latest.revision: 33
caps.handback.revision: 31
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
# Verwenden von mehreren Resultsets
  Bei der Arbeit mit Inline\-SQL\-Prozeduren oder gespeicherten [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Prozeduren, die mehrere Resultsets zurückgeben, stellt [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] die [getResultSet](../content/getResultSet-Method--SQLServerStatement-.md)\-Methode der [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Klasse bereit, um die einzelnen zurückgegebenen Datensätze abzurufen. Beim Ausführen einer Anweisung, die mehr als ein Resultset zurückgibt, können Sie darüber hinaus die [execute](../content/execute-Method--SQLServerStatement-.md)\-Methode der SQLServerStatement\-Klasse verwenden, weil ein **boolean**\-Wert zurückgegeben wird, der angibt, ob es sich bei dem zurückgegebenen Wert um ein Resultset oder eine Updatezählung handelt.  
  
 Wenn die execute\-Methode **true** zurückgibt, wurde von der ausgeführten Anweisung mindestens ein Resultset zurückgegeben. Sie können die getResultSet\-Methode aufrufen, um auf das erste Resultset zuzugreifen. Um zu ermitteln, ob weitere Resultsets verfügbar sind, können Sie die [getMoreResults](../content/getMoreResults-Method--SQLServerStatement-.md)\-Methode aufrufen, die den **boolean**\-Wert **true** zurückgibt, falls weitere Resultsets verfügbar sind. Wenn mehr Resultsets verfügbar sind, können Sie erneut die getResultSet\-Methode aufrufen, um darauf zuzugreifen, und den Prozess fortsetzen, bis alle Resultsets verarbeitet wurden. Wenn die getMoreResults\-Methode **false** zurückgibt, sind keine weiteren Resultsets mehr vorhanden.  
  
 Wenn die execute\-Methode **false** zurückgibt, wurde von der ausgeführten Anweisung ein Updatezählwert zurückgegeben, der durch Aufruf der [getUpdateCount](../content/getUpdateCount-Method--SQLServerStatement-.md)\-Methode abgerufen werden kann.  
  
> [!NOTE]  
>  Weitere Informationen zu Updatezählungen finden Sie unter [Verwenden von gespeicherten Prozeduren mit einer Updatezählung](../content/Using-a-Stored-Procedure-with-an-Update-Count.md).  
  
 Im folgenden Beispiel werden eine offene Verbindung zur [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)][!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank an die Funktion übergeben und eine SQL\-Anweisung erstellt, die bei der Ausführung zwei Resultsets zurückgibt.  
  
 [!CODE [JDBC#UsingMultipleResultSets1](../CodeSnippet/SQLDrivers/jdbc#usingmultipleresultsets1)]  
  
 In diesem Fall ist bekannt, dass zwei Resultsets zurückgegeben werden. Der Code ist jedoch so geschrieben, dass alle Resultsets verarbeitet werden, wenn die Anzahl der zurückgegebenen Resultsets unbekannt ist, wie z. B. beim Aufrufen einer gespeicherten Prozedur. Ein Beispiel für den Aufruf einer gespeicherten Prozedur, die mehrere Resultsets sowie Updatewerte zurückgibt, finden Sie unter [Verarbeiten komplexer Anweisungen](../content/Handling-Complex-Statements.md).  
  
> [!NOTE]  
>  Wenn Sie die getMoreResults\-Methode der SQLServerStatement\-Klasse aufrufen, wird das zuvor zurückgegebene Resultset implizit geschlossen.  
  
## Siehe auch  
 [Verwenden von Anweisungen mit dem JDBC-Treiber](../content/Using-Statements-with-the-JDBC-Driver.md)  
  
  