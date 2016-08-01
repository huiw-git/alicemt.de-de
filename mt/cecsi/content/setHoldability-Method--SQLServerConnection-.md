---
title: "setHoldability-Methode (ISQLServerConnection)"
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
  - SQLServerConnection.setHoldability
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 552eebd0-4c38-43f0-961f-35244f99109b
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
# setHoldability-Methode (ISQLServerConnection)
    
## setHoldability\-Methode \(ISQLServerConnection\)  
 Ändert die Haltbarkeit von [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekten, die unter Verwendung dieses [SQLServerSavepoint](../content/SQLServerSavepoint-Class.md)\-Objekts erstellt werden, zur angegebenen Haltbarkeit.  
  
## Syntax  
  
```  
  
public void setHoldability(int nNewHold)  
```  
  
#### Parameter  
 *nNewHold*  
  
 Ein Wert vom Typ **int** mit einer der folgenden Haltbarkeitsstufen:  
  
 HOLD\_CURSORS\_OVER\_COMMIT  
  
 CLOSE\_CURSORS\_AT\_COMMIT  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setHoldability\-Methode wird von der setHoldability\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  