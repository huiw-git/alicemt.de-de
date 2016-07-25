---
title: "setLoginTimeout-Methode (SQLServerDataSource)"
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
  - SQLServerDataSource.setLoginTimeout
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: b63d1cf4-dc1b-4e35-9a56-50436642eaaf
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
# setLoginTimeout-Methode (SQLServerDataSource)
    
## setLoginTimeout\-Methode \(SQLServerDataSource\)  
 Legt die Anzahl von Sekunden fest, die vom [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Objekt bei der Verbindungsherstellung gewartet wird.  
  
## Syntax  
  
```  
  
public void setLoginTimeout(int loginTimeout)  
```  
  
#### Parameter  
 *loginTimeout*  
  
 Ein Wert vom Typ **int** zum Darstellen der Wartedauer in Sekunden. Mit dem Wert "0" wird angegeben, dass es sich bei dem Timeout um das Standardsystemtimeout \(standardmäßig 15 Sekunden\) handelt.  
  
## Hinweise  
 Diese setLoginTimeout\-Methode wird von der setLoginTimeout\-Methode in der javax.sql.DataSource\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  