---
title: "&#196;ndern von Datenbankobjekten mit SQL-Anweisungen"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f49ea499-df3c-4e85-9fc7-450fb99622a6
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
# &#196;ndern von Datenbankobjekten mit SQL-Anweisungen
    
## Ändern von Datenbankobjekten mit SQL\-Anweisungen  
 Mit der [executeUpdate](../content/executeUpdate-Method--SQLServerStatement-.md)\-Methode der [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Klasse können Sie [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbankobjekte über eine SQL\-Anweisung ändern. Die executeUpdate\-Methode übergibt die SQL\-Anweisung zur Verarbeitung an die Datenbank und gibt anschließend den Wert 0 zurück, weil keine Zeilen betroffen sind.  
  
 Sie müssen dazu zuerst mit der [createStatement](../content/createStatement-Method--SQLServerConnection-.md)\-Methode der [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Klasse ein SQLServerStatement\-Objekt erstellen.  
  
> [!NOTE]  
>  SQL\-Anweisungen, die Objekte in einer Datenbank ändern, werden DDL\-Anweisungen \(Data Definition Language\) genannt. Dazu gehören Anweisungen wie CREATE TABLE, DROP TABLE, CREATE INDEX und DROP INDEX. Weitere Informationen zu den von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] unterstützten DDL\-Anweisungen finden Sie in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation.  
  
 Im folgenden Beispiel werden eine offene Verbindung zur [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)][!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank an die Funktion übergeben, eine SQL\-Anweisung erstellt, die die einfache Testtabelle in der Datenbank erstellt, die Anweisung anschließend ausgeführt und der Rückgabewert angezeigt.  
  
 [!CODE [JDBC#UsingSQLToModifyDBObjects1](../CodeSnippet/SQLDrivers/jdbc#usingsqltomodifydbobjects1)]  
  
## Siehe auch  
 [Verwenden von Anweisungen mit SQL](../content/Using-Statements-with-SQL.md)  
  
  