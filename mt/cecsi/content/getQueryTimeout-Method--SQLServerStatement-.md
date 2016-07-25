---
title: "getQueryTimeout-Methode (SQLServerStatement)"
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
  - SQLServerStatement.getQueryTimeout
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 8dff954f-b458-4fa6-abe6-be62ff75e2b9
caps.latest.revision: 11
caps.handback.revision: 11
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
# getQueryTimeout-Methode (SQLServerStatement)
  Ruft die Anzahl von Sekunden ab, die von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] auf die Ausführung dieses [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekts gewartet wird.  
  
## Syntax  
  
```  
  
public final int getQueryTimeout()  
```  
  
## Rückgabewert  
 Ein Wert vom Typ **int**, der die Wartezeit des JDBC\-Treibers in Sekunden angibt, oder "0", wenn kein Limit vorhanden ist.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getQueryTimeout\-Methode wird von der getQueryTimeout\-Methode in der java.sql.Statement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  