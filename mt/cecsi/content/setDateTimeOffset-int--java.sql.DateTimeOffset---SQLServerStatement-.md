---
title: "setDateTimeOffset(int, java.sql.DateTimeOffset) (SQLServerStatement)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e8b6e380-6b53-489b-be73-73fcb5258269
caps.latest.revision: 10
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
# setDateTimeOffset(int, java.sql.DateTimeOffset) (SQLServerStatement)
    
## setDateTimeOffset\(int, java.sql.DateTimeOffset\) \(SQLServerStatement\)  
 Legt den angegebenen Parameter auf den angegebenen DateTimeOffset\-Wert fest.  
  
## Syntax  
  
```  
  
public void setDateTimeOffset(int parameterIndex, DateTimeOffset dateTime)  
```  
  
#### Parameter  
 *parameterIndex*  
  
 Der Index der festzulegenden Spalte.  
  
 *dateTimeOffset*  
  
 Ein DateTimeOffset\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Das DateTimeOffset\-Format lautet "YYYY\-MM\-DD HH\-MM\-SS\[.nnnnnnn\] \[\+\]\[\-\] HH:MM". Verwenden Sie die folgende Tabelle als Referenz.  
  
|SQL\-Typ|Einfügung|  
|--------------|---------------|  
|datetime|Kann nur Folgendes einfügen: "YYYY\-MM\-DD hh:mm:ss\[.nnn\]"|  
|smalldatetime|Kann nur Folgendes einfügen: "YYYY\-MM\-DD hh:mm:ss"|  
|Time|Kann nur Folgendes einfügen: "hh:mm:ss\[.nnnnnnn\]"|  
|Date|Kann nur Folgendes einfügen: "YYYY\-MM\-DD"|  
|DateTime2|Kann nur Folgendes einfügen: "YYYY\-MM\-DD hh:mm:ss\[.nnnnnnn\]"|  
  
## Siehe auch  
 [getDateTimeOffset &#40;SQLServerResultSet&#41;](../content/getDateTimeOffset--SQLServerResultSet-.md)   
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  