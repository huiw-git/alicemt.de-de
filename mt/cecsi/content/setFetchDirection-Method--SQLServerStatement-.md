---
title: "setFetchDirection-Methode (SQLServerStatement)"
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
  - SQLServerStatement.setFetchDirection
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 18176517-2fb3-4266-924d-0f01253083d2
caps.latest.revision: 13
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
# setFetchDirection-Methode (SQLServerStatement)
  Gibt für [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] die Richtung an, in der die Resultsetzeilen verarbeitet werden sollen.  
  
> [!NOTE]  
>  Die Angabe dieser Methode wird vom JDBC\-Treiber derzeit ignoriert.  
  
## Syntax  
  
```  
  
public final void setFetchDirection(int nDir)  
```  
  
#### Parameter  
 *nDir*  
  
 Ein Wert vom Typ **int** zum Angeben der Zeilenverarbeitungsrichtung. Mögliche Werte:  
  
 FETCH\_FORWARD  
  
 FETCH\_REVERSE  
  
 FETCH\_UNKNOWN  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setFetchDirection\-Methode wird von der setFetchDirection\-Methode in der java.sql.Statement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  