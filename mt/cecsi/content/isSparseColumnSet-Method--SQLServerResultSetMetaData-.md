---
title: "isSparseColumnSet-Methode (SQLServerResultSetMetaData)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ac363670-78ae-49f1-aeda-4fba3329a258
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
# isSparseColumnSet-Methode (SQLServerResultSetMetaData)
  Gibt an, ob eine Spalte in einem Resultset ein Satz von Spalten mit geringer Dichte ist.  
  
## Syntax  
  
```scr  
public boolean isSparseColumnSet(int column)  
```  
  
#### Parameter  
 *column*  
  
 Der Index der Spalte \(mit der Basis eins\).  
  
## Rückgabewert  
 **true**, wenn eine Spalte in einem Resultset ein Satz von Spalten mit geringer Dichte ist, andernfalls **false**.  
  
## Hinweise  
 Diese Methode ruft keine Informationen aus der Datenbank ab.  
  
## Siehe auch  
 [SQLServerResultSetMetaData-Methoden](../content/SQLServerResultSetMetaData-Methods.md)   
 [SQLServerResultSetMetaData-Elemente](../content/SQLServerResultSetMetaData-Members.md)   
 [SQLServerResultSetMetaData-Klasse](../content/SQLServerResultSetMetaData-Class.md)  
  
  