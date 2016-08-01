---
title: "getHoldability-Methode (ISQLServerConnection)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLServerConnection.getHoldability
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: b1644791-c36a-4837-86c4-9299537ee1c2
caps.latest.revision: 11
caps.handback.revision: 10
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
# getHoldability-Methode (ISQLServerConnection)
    
## getHoldability\-Methode \(ISQLServerConnection\)  
 Ruft die aktuelle Haltbarkeit von [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekten ab, die unter Verwendung dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekts erstellt werden.  
  
## Syntax  
  
```  
  
public int getHoldability()  
```  
  
## Rückgabewert  
 Ein Wert vom Typ **int** mit einer der folgenden Haltbarkeitsstufen:  
  
 HOLD\_CURSORS\_OVER\_COMMIT  
  
 CLOSE\_CURSORS\_AT\_COMMIT  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getHoldability\-Methode wird von der getHoldability\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  