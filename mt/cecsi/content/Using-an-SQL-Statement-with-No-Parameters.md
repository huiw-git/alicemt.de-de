---
title: "Verwenden von SQL-Anweisungen ohne Parameter"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4b0728bd-059b-4b71-895c-999335bc7427
caps.latest.revision: 10
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
# Verwenden von SQL-Anweisungen ohne Parameter
    
## Verwenden von SQL\-Anweisungen ohne Parameter  
 Wenn Sie Daten in einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank mit einer SQL\-Anweisung ohne Parameter verarbeiten möchten, können Sie mit der [executeQuery](../content/executeQuery-Method--SQLServerStatement-.md)\-Methode der [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Klasse ein [SQLServerResultSet](../content/SQLServerResultSet-Class.md) zurückgeben, das die angeforderten Daten enthält. Sie müssen dazu zuerst mit der [createStatement](../content/createStatement-Method--SQLServerConnection-.md)\-Methode der [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Klasse ein SQLServerStatement\-Objekt erstellen.  
  
 Im folgenden Beispiel werden eine offene Verbindung zur [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)][!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank an die Funktion übergeben, eine SQL\-Anweisung erstellt und ausgeführt sowie die Ergebnisse aus dem Resultset gelesen.  
  
 [!CODE [JDBC#UsingSQLWithNoParams1](../CodeSnippet/SQLDrivers/jdbc#usingsqlwithnoparams1)]  
  
 Weitere Informationen zum Verwenden von Resultsets finden Sie unter [Verwalten von Resultsets mit dem JDBC-Treiber](../content/Managing-Result-Sets-with-the-JDBC-Driver.md).  
  
## Siehe auch  
 [Verwenden von Anweisungen mit SQL](../content/Using-Statements-with-SQL.md)  
  
  