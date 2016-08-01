---
title: "absolute-Methode (ISQLServerResultSet)"
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
  - SQLServerResultSet.absolute
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 638e8148-8ca0-4e1f-9ec2-04a11bc9809b
caps.latest.revision: 8
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
# absolute-Methode (ISQLServerResultSet)
    
## absolute\-Methode \(ISQLServerResultSet\)  
 Versetzt den Cursor in die vorhandene Zeile in diesem [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt.  
  
## Syntax  
  
```  
  
public boolean absolute(int row)  
```  
  
#### Parameter  
 *row*  
  
 Ein Wert vom Typ **int** zum Angeben der Zeilenzahl, an die verschoben werden soll. Kann positiv, negativ oder "0" sein.  
  
## Rückgabewert  
 **true**, wenn der Cursor an die angegebene Position verschoben wird. **false**, wenn er vor die erste oder hinter die letzte Zeile verschoben wird.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese absolute\-Methode wird von der absolute\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  