---
title: "getXopenStates-Methode (SQLServerDataSource)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLServerDataSource.getXopenStates
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: de6fdf6b-8345-4490-b35e-7115b61e782e
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
# getXopenStates-Methode (SQLServerDataSource)
  Gibt einen Wert vom Typ **boolean** zurück, mit dem angegeben wird, ob das Konvertieren von SQL\-Status in XOPEN\-kompatible Status aktiviert ist.  
  
## Syntax  
  
```  
  
public boolean getXopenStates()  
```  
  
## Rückgabewert  
 **true**, wenn das Konvertieren von SQL\-Status zu XOPEN\-kompatiblen Status aktiviert ist. Andernfalls wird **false** verwendet.  
  
## Hinweise  
 Ist die xopenStates\-Eigenschaft auf **true** festgelegt, werden SQL\-Status von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] in XOPEN\-kompatible Status konvertiert. Durch den Standardwert **false** werden vom JDBC\-Treiber SQL 99\-Statuscodes zurückgegeben. Ist die xopenStates\-Eigenschaft nicht festgelegt, wird von der getXopenStates\-Methode der Standardwert **false** zurückgegeben.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  