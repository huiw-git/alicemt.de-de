---
title: "Verwenden von SQL-Anweisungen mit Parametern"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3202b88f-ce13-44dd-982c-c6a3b0260378
caps.latest.revision: 11
caps.handback.revision: 8
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
# Verwenden von SQL-Anweisungen mit Parametern
    
## Verwenden von SQL\-Anweisungen mit Parametern  
 Wenn Sie Daten in einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank mit einer SQL\-Anweisung verarbeiten möchten, die IN\-Parameter enthält, können Sie mit der [executeQuery](../content/executeQuery-Method--SQLServerPreparedStatement-.md)\-Methode der [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\-Klasse ein [SQLServerResultSet](../content/SQLServerResultSet-Class.md) zurückgeben, das die angeforderten Daten enthält. Sie müssen dazu zuerst mit der [prepareStatement](../content/prepareStatement-Method--SQLServerConnection-.md)\-Methode der [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Klasse ein SQLServerPreparedStatement\-Objekt erstellen.  
  
 Beim Erstellen der SQL\-Anweisung werden die IN\-Parameter mit dem ? \(Fragezeichen\) angegeben, das als Platzhalter für die Parameterwerte fungiert, die später an die SQL\-Anweisung übergeben werden. Mit den Festlegungsmethoden der SQLServerPreparedStatement\-Klasse können Sie für einen Parameter einen Wert angeben. Die verwendete Festlegungsmethode hängt vom Datentyp des Werts ab, der an die SQL\-Anweisung übergeben werden soll.  
  
 Wenn Sie einen Wert an die Festlegungsmethode übergeben, müssen Sie nicht nur den Wert angeben, der in der SQL\-Anweisung verwendet werden soll, sondern auch die ordinale Position des Parameters in der SQL\-Anweisung. Wenn die SQL\-Anweisung beispielsweise einen einzigen Parameter enthält, ist der Ordinalwert 1. Wenn die Anweisung zwei Parameter enthält, ist der erste Ordinalwert 1 und der zweite Ordinalwert 2.  
  
 Im folgenden Beispiel werden eine offene Verbindung zur [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)][!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank an die Funktion übergeben, eine vorbereitete SQL\-Anweisung erstellt und mit einem einzigen String\-Parameterwert ausgeführt sowie die Ergebnisse aus dem Resultset gelesen.  
  
 [!CODE [JDBC#UsingSQLWithParams1](../CodeSnippet/SQLDrivers/jdbc#usingsqlwithparams1)]  
  
## Siehe auch  
 [Verwenden von Anweisungen mit SQL](../content/Using-Statements-with-SQL.md)  
  
  