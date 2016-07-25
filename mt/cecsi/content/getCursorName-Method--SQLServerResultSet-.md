---
title: "getCursorName-Methode (SQLServerResultSet)"
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
  - SQLServerResultSet.getCursorName
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: e5b3af67-423a-4551-a4c6-a4bc076bd504
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
# getCursorName-Methode (SQLServerResultSet)
  Ruft den Namen des von diesem [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt verwendeten SQL\-Cursors ab.  
  
> [!NOTE]  
>  Diese Methode wird von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] derzeit nicht unterstützt. Bei Aufruf wird eine Ausnahme ausgelöst.  
  
## Syntax  
  
```  
  
public java.lang.String getCursorName()  
```  
  
## Rückgabewert  
 Ein **String** mit dem Cursornamen.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getCursorName\-Methode wird von der getCursorName\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  