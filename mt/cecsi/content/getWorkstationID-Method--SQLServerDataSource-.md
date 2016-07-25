---
title: "getWorkstationID-Methode (SQLServerDataSource)"
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
  - SQLServerDataSource.getWorkstationID
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: f6a701de-a8fa-4668-9310-99a8c6e32c88
caps.latest.revision: 10
caps.handback.revision: 9
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
# getWorkstationID-Methode (SQLServerDataSource)
    
## getWorkstationID\-Methode \(SQLServerDataSource\)  
 Gibt den Namen des Clientcomputers zurück, der zum Herstellen einer Verbindung mit der Datenquelle verwendet wird.  
  
## Syntax  
  
```  
  
public java.lang.String getWorkstationID()  
```  
  
## Rückgabewert  
 Ein **String** mit dem Computernamen des Clients.  
  
## Hinweise  
 Die workstationID ist der Name des Clientcomputers oder der Workstation. Ist die workstationID\-Eigenschaft nicht festgelegt, wird von der InetAddress.getLocalHost\(\).getHostName\(\)\-Methode der Standardwert erstellt. Wenn von getHostName ein leerer Wert zurückgegeben wird, wird die getHostAddress\(\).toString\(\)\-Methode aufgerufen.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  