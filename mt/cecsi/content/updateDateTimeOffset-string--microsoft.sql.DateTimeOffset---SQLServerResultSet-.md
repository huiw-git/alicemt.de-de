---
title: "updateDateTimeOffset(string, microsoft.sql.DateTimeOffset) (SQLServerResultSet)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 952947ce-7c6e-4364-b035-46cb7fe621b2
caps.latest.revision: 7
caps.handback.revision: 7
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
# updateDateTimeOffset(string, microsoft.sql.DateTimeOffset) (SQLServerResultSet)
  Diese Methode wurde in [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 hinzugefügt.  
  
 Aktualisiert bei einem vorhandenen Spaltennamen die für den [DateTimeOffset-Klasse](../content/DateTimeOffset-Class.md)\-Wert festgelegte Spalte.  
  
## Syntax  
  
```  
  
public void updateDateTimeOffset(String columnName, microsoft.sql.DateTimeOffset x)  
```  
  
#### Parameter  
 *columnName*  
  
 Der Name einer Spalte.  
  
 *x*  
  
 Ein [DateTimeOffset-Klasse](../content/DateTimeOffset-Class.md)\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Sie können einen [DateTimeOffset-Klasse](../content/DateTimeOffset-Class.md)\-Wert mit dem [SQLServerResultSet.getDateTimeOffset](../content/getDateTimeOffset--SQLServerResultSet-.md)\-Element abrufen.  
  
## Siehe auch  
 [updateDateTimeOffset &#40;SQLServerResultSet&#41;](../content/updateDateTimeOffset--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  