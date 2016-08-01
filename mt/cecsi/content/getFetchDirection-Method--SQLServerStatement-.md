---
title: "getFetchDirection-Methode (SQLServerStatement)"
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
  - SQLServerStatement.getFetchDirection
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: ceb4ae68-decc-46d3-83f1-0bbd23aaf58c
caps.latest.revision: 12
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
# getFetchDirection-Methode (SQLServerStatement)
  Ruft die Richtung zum Abrufen von Zeilen aus Datenbanktabellen ab, die standardmäßig für Resultsets verwendet wird, die auf der Grundlage dieses [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekts generiert werden.  
  
> [!NOTE]  
>  Diese Methode wird von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] derzeit nicht implementiert. Aus diesem Grund wird immer "FETCH\_UNKNOWN" zurückgegeben.  
  
## Syntax  
  
```  
  
public final int getFetchDirection()  
```  
  
## Rückgabewert  
 Ein Wert vom Typ **int** zum Angeben der Abrufrichtung, die von der [setFetchDirection](../content/setFetchDirection-Method--SQLServerStatement-.md)\-Methode angegeben wird.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getFetchDirection\-Methode wird von der getFetchDirection\-Methode in der java.sql.Statement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  