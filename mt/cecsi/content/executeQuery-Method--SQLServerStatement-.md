---
title: "executeQuery-Methode (SQLServerStatement)"
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
  - SQLServerStatement.executeQuery
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 599cf463-e19f-4baa-bacb-513cad7c6cd8
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
# executeQuery-Methode (SQLServerStatement)
  Führt die angegebene SQL\-Anweisung aus und gibt ein einzelnes [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt zurück.  
  
## Syntax  
  
```  
  
public java.sql.ResultSet executeQuery(java.lang.String sql)  
```  
  
#### Parameter  
 *sql*  
  
 Ein **String** mit einer SQL\-Anweisung.  
  
## Rückgabewert  
 Ein SQLServerResultSet\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese executeQuery\-Methode wird von der executeQuery\-Methode in der java.sql.Statement\-Schnittstelle angegeben.  
  
 [SQLServerException](../content/SQLServerException-Class.md) wird ausgelöst, wenn die angegebene SQL\-Anweisung etwas anderes als ein einzelnes [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt produziert.  
  
 Wenn beim Ausführen einer gespeicherten Prozedur eine Updatezählung größer als 1 erhalten oder mehrere Resultsets generiert werden, führen Sie die gespeicherte Prozedur mit der [execute](../content/execute-Method--SQLServerStatement-.md)\-Methode aus.  
  
## Siehe auch  
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  