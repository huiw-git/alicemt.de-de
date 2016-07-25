---
title: "setDateTimeOffset-Methode (SQLServerPreparedStatement)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5014dba9-1755-4769-b070-6cbeecee864e
caps.latest.revision: 7
caps.handback.revision: 6
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
# setDateTimeOffset-Methode (SQLServerPreparedStatement)
  Diese Methode wurde in [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 hinzugefügt.  
  
 Legt den Wert der Spalte fest, die für den [DateTimeOffset-Klasse](../content/DateTimeOffset-Class.md)\-Wert angegeben wurde.  
  
## Syntax  
  
```  
  
public final void setDateTimeOffset(int n, microsoft.sql.DateTimeOffset x)  
```  
  
#### Parameter  
 *n*  
  
 Die nullbasierte Ordinalzahl einer Spalte.  
  
 *x*  
  
 Das [DateTimeOffset-Klasse](../content/DateTimeOffset-Class.md)\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Siehe auch  
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)   
 [SQLServerPreparedStatement-Klasse](../content/SQLServerPreparedStatement-Class.md)  
  
  