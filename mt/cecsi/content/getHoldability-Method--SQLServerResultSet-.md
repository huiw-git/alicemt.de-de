---
title: "getHoldability-Methode (SQLServerResultSet)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4508d90f-c3c4-4eac-8001-fb0b93b66734
caps.latest.revision: 16
caps.handback.revision: 15
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
# getHoldability-Methode (SQLServerResultSet)
  Ruft die Haltbarkeit dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts ab.  
  
## Syntax  
  
```  
  
public int getHoldability()  
```  
  
## Rückgabewert  
 Ein Wert vom Typ **int** mit einer der folgenden Holdabilitystufen:  
  
 HOLD\_CURSORS\_OVER\_COMMIT  
  
 CLOSE\_CURSORS\_AT\_COMMIT  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getHoldability\-Methode wird von der getHoldability\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Zum Festlegen der Holdability für Resultsets kann von Anwendungen die [setHoldability](../content/setHoldability-Method--SQLServerConnection-.md)\-Methode der [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Klasse verwendet werden. Nach dem Aufrufen der [setHoldability](../content/setHoldability-Method--SQLServerConnection-.md)\-Methode, dem Erstellen des Anweisungsobjekts und dessen Resultsetobjekts und dem Ausführen der Anweisung muss die Haltbarkeit von der Anwendung möglicherweise erneut geändert werden.  
  
 Wenn Servercursor mit SQL Server 2005 oder höher verbunden sind, wirkt sich das Festlegen der Haltbarkeit nur auf die Haltbarkeit neuer Resultsets aus, die erst noch für diese Verbindung erstellt werden. Bei SQL Server 2000 wirkt sich das Festlegen der Haltbarkeit jedoch sowohl auf die Haltbarkeit vorhandener als auch neuer, noch für die Verbindung zu erstellender Resultsets aus.  
  
 Wird die Holdability zurückgesetzt und die getHoldability\-Methode für ein zuvor erstelltes Resultsetobjekt aufgerufen, unterscheidet sich der von dieser Methode zurückgegebene Wert möglicherweise vom Holdabilitywert, der von den folgenden Methoden zurückgegeben wird: Statement.getResultSetHoldability, Connection.getHoldability oder DatabaseMetaData.getResultSetHoldability.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  