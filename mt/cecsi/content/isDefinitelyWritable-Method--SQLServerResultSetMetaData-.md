---
title: "isDefinitelyWritable-Methode (SQLServerResultSetMetaData)"
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
  - SQLServerResultSetMetaData.isDefinitelyWritable
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 7650e89a-dc8e-43ca-8eb2-f962f1a4b4ae
caps.latest.revision: 10
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
# isDefinitelyWritable-Methode (SQLServerResultSetMetaData)
  Gibt an, ob ein Schreibvorgang in der angegebenen Spalte definitiv erfolgreich sein wird.  
  
## Syntax  
  
```  
  
public boolean isDefinitelyWritable(int column)  
```  
  
#### Parameter  
 *column*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindex.  
  
## Rückgabewert  
 **true**, wenn der Schreibvorgang in der Spalte definitiv erfolgreich sein wird. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese isDefinitelyWritable\-Methode wird von der isDefinitelyWritable\-Methode in der java.sql.ResultSetMetaData\-Schnittstelle angegeben.  
  
> [!NOTE]  
>  Wird [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank verwendet, wird von dieser Methode immer "false" zurückgegeben.  
  
## Siehe auch  
 [SQLServerResultSetMetaData-Methoden](../content/SQLServerResultSetMetaData-Methods.md)   
 [SQLServerResultSetMetaData-Elemente](../content/SQLServerResultSetMetaData-Members.md)   
 [SQLServerResultSetMetaData-Klasse](../content/SQLServerResultSetMetaData-Class.md)  
  
  