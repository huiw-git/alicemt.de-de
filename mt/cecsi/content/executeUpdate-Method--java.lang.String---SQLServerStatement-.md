---
title: "executeUpdate-Methode (java.lang.String) (SQLServerStatement)"
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
  - SQLServerStatement.executeUpdate (java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 85e7c3a2-f2da-49bf-9d90-5fd246fd60e1
caps.latest.revision: 13
caps.handback.revision: 13
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
# executeUpdate-Methode (java.lang.String) (SQLServerStatement)
  Führt die angegebene SQL\-Anweisung aus. Hierbei kann es sich um eine Anweisung vom Typ "INSERT", "UPDATE" oder "DELETE" oder um eine SQL\-Anweisung handeln, von der nichts zurückgegeben wird \(beispielsweise eine SQL\-DDL\-Anweisung\). Ab [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 wird von executeUpdate die korrekte Anzahl Zeilen zurückgegeben, die in einem MERGE\-Vorgang aktualisiert wurde.  
  
## Syntax  
  
```  
  
public int executeUpdate(java.lang.String sql)  
```  
  
#### Parameter  
 *sql*  
  
 Ein **String** mit der SQL\-Anweisung.  
  
## Rückgabewert  
 Ein Wert vom Typ **int** zum Angeben der Anzahl der betroffenen Zeilen \("0" bei Verwendung einer DDL\-Anweisung\).  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese executeUpdate\-Methode wird von der executeUpdate\-Methode in der java.sql.Statement\-Schnittstelle angegeben.  
  
 Wenn beim Ausführen einer gespeicherten Prozedur eine Updatezählung größer als 1 erhalten oder mehrere Resultsets generiert werden, führen Sie die gespeicherte Prozedur mit der [execute](../content/execute-Method--SQLServerStatement-.md)\-Methode aus.  
  
## Siehe auch  
 [executeUpdate-Methode &#40;SQLServerStatement&#41;](../content/executeUpdate-Method--SQLServerStatement-.md)   
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  