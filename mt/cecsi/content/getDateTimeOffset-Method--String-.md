---
title: "getDateTimeOffset-Methode (Zeichenfolge)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fedb1d75-0c3d-4eb3-ae65-da0e153265cc
caps.latest.revision: 14
caps.handback.revision: 14
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
# getDateTimeOffset-Methode (Zeichenfolge)
  Diese Methode wurde in [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 hinzugefügt.  
  
 Ruft den Wert des angegebenen Parameters unter Berücksichtigung des Parameterindexes als [DateTimeOffset-Klasse](../content/DateTimeOffset-Class.md)\-Objekt in der Programmiersprache Java ab.  
  
## Syntax  
  
```  
  
public microsoft.sql.DateTimeOffset getDateTimeOffset(String sCol)  
```  
  
#### Parameter  
 *sCol*  
  
 Der Name eines Parameters.  
  
## Rückgabewert  
 Ein [DateTimeOffset-Klasse](../content/DateTimeOffset-Class.md)\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Sie können einen [DateTimeOffset-Klasse](../content/DateTimeOffset-Class.md)\-Parameterwert mit [SQLServerCallableStatement.setDateTimeOffset](../content/setDateTimeOffset-Method--SQLServerCallableStatement-.md) festlegen.  
  
## Siehe auch  
 [getDateTimeOffset-Methode &#40;SQLServerCallableStatement&#41;](../content/getDateTimeOffset-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  