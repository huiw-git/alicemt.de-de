---
title: "setReadOnly-Methode (SQLServerConnection)"
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
  - SQLServerConnection.setReadOnly
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: bd11fd50-f092-43a0-a6bc-c63e70cff8da
caps.latest.revision: 14
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
# setReadOnly-Methode (SQLServerConnection)
  Versetzt dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt in den schreibgeschützten Modus, damit vom JDBC\-Treiber die Datenbankoptimierungen aktiviert werden.  
  
> [!NOTE]  
>  Diese Methode wird von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] nicht unterstützt.  
  
## Syntax  
  
```  
  
public void setReadOnly(boolean readOnly)  
```  
  
#### Parameter  
 *readOnly*  
  
 **true**, wenn die Verbindung schreibgeschützt sein soll. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setReadOnly\-Methode wird von der setReadOnly\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  