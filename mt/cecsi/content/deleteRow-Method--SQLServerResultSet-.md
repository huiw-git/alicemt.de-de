---
title: "deleteRow-Methode (ISQLServerResultSet)"
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
  - SQLServerResultSet.deleteRow
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: aa04a644-c7c2-4738-8b6e-7fea566d2c16
caps.latest.revision: 9
caps.handback.revision: 9
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
# deleteRow-Methode (ISQLServerResultSet)
    
## deleteRow\-Methode \(ISQLServerResultSet\)  
 Löscht die aktuelle Zeile aus diesem[SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt sowie aus der zugrunde liegenden Datenbank.  
  
## Syntax  
  
```  
  
public void deleteRow()  
```  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese deleteRow\-Methode wird von der deleteRow\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Diese Methode kann nicht aufgerufen werden, wenn sich der Cursor in der Einfügezeile befindet.  
  
 Bei der Verwendung von Keysetcursorn wird von dieser Methode eine Lücke im Resultset hinterlassen. Ob diese Lücke vorhanden ist, können Sie mit der [rowDeleted](../content/rowDeleted-Method--SQLServerResultSet-.md)\-Methode überprüfen. Die Zeilennummern der Zeilen im Resultset ändern sich nicht.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  