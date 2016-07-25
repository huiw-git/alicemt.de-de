---
title: "setXopenStates-Methode (SQLServerDataSource)"
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
  - SQLServerDataSource.setXopenStates
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 9723591f-e987-426f-b70a-07f5c70dc094
caps.latest.revision: 12
caps.handback.revision: 12
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
# setXopenStates-Methode (SQLServerDataSource)
  Legt einen Wert vom Typ **Boolean** fest, mit dem angegeben wird, ob das Konvertieren von SQL\-Status in XOPEN\-kompatible Status aktiviert ist.  
  
## Syntax  
  
```  
  
public void setXopenStates(boolean xopenStates)  
```  
  
#### Parameter  
 *xopenStates*  
  
 **true**, wenn das Konvertieren von SQL\-Status zu XOPEN\-kompatiblen Status aktiviert ist. Andernfalls wird **false** verwendet.  
  
## Hinweise  
 Ist die xopenStates\-Eigenschaft auf **true** festgelegt, werden SQL\-Status von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] in XOPEN\-kompatible Status konvertiert. Durch den Standardwert **false** werden vom JDBC\-Treiber SQL 99\-Statuscodes zurückgegeben. Ist die xopenStates\-Eigenschaft nicht festgelegt, wird von der [getXopenStates](../content/getXopenStates-Method--SQLServerDataSource-.md)\-Methode der Standardwert **false** zurückgegeben.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  