---
title: "getLastUpdateCount-Methode (SQLServerDataSource)"
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
  - SQLServerDataSource.getLastUpdateCount
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 4c4fbb24-0b02-42da-928c-a903bb591cc7
caps.latest.revision: 17
caps.handback.revision: 17
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
# getLastUpdateCount-Methode (SQLServerDataSource)
  Gibt einen Wert vom Typ **Boolean** zurück, mit dem angegeben wird, ob die lastUpdateCount\-Eigenschaft aktiviert ist.  
  
## Syntax  
  
```  
  
public boolean getLastUpdateCount()  
```  
  
## Rückgabewert  
 **true**, wenn "lastUpdateCount" aktiviert ist. Andernfalls wird **false** verwendet.  
  
## Hinweise  
 Ist die lastUpdateCount\-Eigenschaft auf **true** festgelegt, wird von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] nur die letzte Updatezählung aus einer an den Server übergebenen SQL\-Anweisung zurückgegeben. Ist die lastUpdateCount\-Eigenschaft auf **false** festgelegt, werden vom Treiber alle Updatezählungen zurückgegeben – einschließlich jener, die von möglicherweise ausgelösten Triggern zurückgegeben wurden. Ist die lastUpdateCount\-Eigenschaft nicht festgelegt, wird von der getLastUpdateCount\-Methode der Standardwert **true** zurückgegeben.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  