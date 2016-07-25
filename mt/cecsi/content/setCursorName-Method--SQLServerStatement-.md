---
title: "setCursorName-Methode (SQLServerStatement)"
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
  - SQLServerStatement.setCursorName
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 3f3ec4f2-103a-4e16-9206-c5bd8639f946
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
# setCursorName-Methode (SQLServerStatement)
  Legt den SQL\-Cursornamen auf die angegebene Zeichenfolge fest, die dann für nachfolgende Ausführungsmethoden verwendet wird.  
  
> [!NOTE]  
>  Diese Methode wird von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] derzeit nicht unterstützt. Das Aufrufen der Methode hat keinerlei Wirkung.  
  
## Syntax  
  
```  
  
public final void setCursorName(java.lang.String name)  
```  
  
#### Parameter  
 *name*  
  
 Ein **String** mit dem Cursornamen.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setCursorName\-Methode wird von der setCursorName\-Methode in der java.sql.Statement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  