---
title: "setDateTimeOffset-Methode (SQLServerCallableStatement)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9383e14d-c83e-43c5-980c-50a3e0bedc31
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
# setDateTimeOffset-Methode (SQLServerCallableStatement)
  Diese Methode wurde in [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 hinzugefügt.  
  
 Legt den Wert der Spalte fest, die für den [DateTimeOffset-Klasse](../content/DateTimeOffset-Class.md)\-Wert angegeben wurde.  
  
## Syntax  
  
```  
  
public void setDateTimeOffset(String sCol, microsoft.sql.DateTimeOffset t)  
```  
  
#### Parameter  
 *sCol*  
  
 Der Name einer Spalte.  
  
 *t*  
  
 Das [DateTimeOffset-Klasse](../content/DateTimeOffset-Class.md)\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Sie können einen [DateTimeOffset-Klasse](../content/DateTimeOffset-Class.md)\-Wert mit [SQLServerCallableStatement.getDateTimeOffset](../content/getDateTimeOffset-Method--SQLServerCallableStatement-.md) abrufen.  
  
 [setDateTimeOffset](../content/setDateTimeOffset-Method--SQLServerPreparedStatement-.md) nimmt die Ordinalposition der Spalte.  
  
## Siehe auch  
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  