---
title: "getDateTimeOffset(int) (SQLServerResultSet)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 60abf83d-6f97-4e47-b9d3-5072bd09d869
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
# getDateTimeOffset(int) (SQLServerResultSet)
  Diese Methode wurde in [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 hinzugefügt.  
  
 Ruft den Wert der angegebenen Spalte unter Berücksichtigung des Parameterindexes als [DateTimeOffset-Klasse](../content/DateTimeOffset-Class.md)\-Objekt in der Programmiersprache Java ab.  
  
## Syntax  
  
```  
  
public microsoft.sql.DateTimeOffset getDateTimeOffset(int columnIndex)  
```  
  
#### Parameter  
 *columnIndex*  
  
 Die Ordnungszahl der Spalte.  
  
## Rückgabewert  
 Ein [DateTimeOffset-Klasse](../content/DateTimeOffset-Class.md)\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Sie können einen [DateTimeOffset-Klasse](../content/DateTimeOffset-Class.md)\-Wert mit [SQLServerResultSet.updateDateTimeOffset](../content/updateDateTimeOffset--SQLServerResultSet-.md) aktualisieren.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  