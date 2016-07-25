---
title: "executeUpdate-Methode ()"
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
  - SQLServerPreparedStatement.executeUpdate ()
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: ca534c6b-ef4d-4ae8-8cc3-514728623cff
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
# executeUpdate-Methode ()
    
## executeUpdate\-Methode \(\)  
 Führt die SQL\-Anweisung in diesem [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\-Objekt aus. Hierbei muss es sich um eine SQL\-Anweisung vom Typ "INSERT", "UPDATE", "MERGE", "DELETE" oder um eine SQL\-Anweisung handeln, von der nichts zurückgegeben wird \(beispielsweise eine DDL\-Anweisung\).  
  
## Syntax  
  
```  
  
public int executeUpdate()  
```  
  
## Rückgabewert  
 Ein Wert vom Typ **int** zum Angeben der Anzahl der betroffenen Zeilen \("0" bei Verwendung einer DDL\-Anweisung\).  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Die executeUpdate\-Methode wird von der executeUpdate\-Methode in der java.sql.PreparedStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [executeUpdate-Methode &#40;ISQLServerPreparedStatement&#41;](../content/executeUpdate-Method--SQLServerPreparedStatement-.md)   
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)   
 [SQLServerPreparedStatement-Klasse](../content/SQLServerPreparedStatement-Class.md)  
  
  