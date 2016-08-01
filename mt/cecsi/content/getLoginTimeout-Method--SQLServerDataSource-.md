---
title: "getLoginTimeout-Methode (SQLServerDataSource)"
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
  - SQLServerDataSource.getLoginTimeout
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 316f067c-9e08-456a-af19-b80b0bbd4a5c
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
# getLoginTimeout-Methode (SQLServerDataSource)
    
## getLoginTimeout\-Methode \(SQLServerDataSource\)  
 Gibt die Anzahl von Sekunden zurück, die vom [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Objekt bei der Verbindungsherstellung gewartet wird.  
  
## Syntax  
  
```  
  
public int getLoginTimeout()  
```  
  
## Rückgabewert  
 Ein Wert vom Typ **int** zum Darstellen der Wartedauer in Sekunden.  
  
## Hinweise  
 Wird von der Anwendung kein expliziter Timeoutwert angegeben, werden von dieser Methode standardmäßig 15 Sekunden zurückgegeben.  
  
 Diese getLoginTimeout\-Methode wird von der getLoginTimeout\-Methode in der javax.sql.DataSource\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  