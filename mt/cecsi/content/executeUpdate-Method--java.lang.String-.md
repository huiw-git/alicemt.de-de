---
title: "executeUpdate-Methode (java.lang.String)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLServerPreparedStatement.executeUpdate (java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 91ecb1cd-001d-4ac9-9ae8-5db05c3c2959
caps.latest.revision: 11
caps.handback.revision: 11
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
# executeUpdate-Methode (java.lang.String)
    
## executeUpdate\-Methode \(java.lang.String\)  
 Führt die angegebene SQL\-Anweisung aus. Hierbei kann es sich um eine Anweisung vom Typ "INSERT", "UPDATE", "MERGE" oder "DELETE" oder um eine SQL\-Anweisung handeln, von der nichts zurückgegeben wird \(beispielsweise eine SQL\-DDL\-Anweisung\).  
  
## Syntax  
  
```  
  
public final int executeUpdate(java.lang.String sql)  
```  
  
#### Parameter  
 *sql*  
  
 Ein **String** mit der SQL\-Anweisung.  
  
## Rückgabewert  
 Ein Wert vom Typ **int** zum Angeben der Anzahl der betroffenen Zeilen \("0" bei Verwendung einer DDL\-Anweisung\).  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Die executeUpdate\-Methode wird von der executeUpdate\-Methode in der java.sql.PreparedStatement\-Schnittstelle angegeben.  
  
 Durch den Aufruf dieser Methode wird eine Ausnahme ausgelöst, da die SQL\-Anweisung für das SQLServerPreparedStatement\-Objekt bei der Erstellung des Objekts angegeben wird.  
  
## Siehe auch  
 [executeUpdate-Methode &#40;ISQLServerPreparedStatement&#41;](../content/executeUpdate-Method--SQLServerPreparedStatement-.md)   
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)   
 [SQLServerPreparedStatement-Klasse](../content/SQLServerPreparedStatement-Class.md)  
  
  