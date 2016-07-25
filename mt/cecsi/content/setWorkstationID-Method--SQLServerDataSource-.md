---
title: "setWorkstationID-Methode (SQLServerDataSource)"
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
  - SQLServerDataSource.setWorkstationID
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: c1093615-90bf-4918-9f05-8abd765ffb03
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
# setWorkstationID-Methode (SQLServerDataSource)
    
## setWorkstationID\-Methode \(SQLServerDataSource\)  
 Legt den Namen des Clientcomputers fest, der zum Herstellen einer Verbindung mit der Datenquelle verwendet wird.  
  
## Syntax  
  
```  
  
public void setWorkstationID(java.lang.String workstationID)  
```  
  
#### Parameter  
 *workstationID*  
  
 Ein **String** mit dem Computernamen des Clients.  
  
## Hinweise  
 Die workstationID ist der Name des Clientcomputers oder der Workstation. Ist die workstationID\-Eigenschaft nicht festgelegt, wird von der InetAddress.getLocalHost\(\).getHostName\(\)\-Methode der Standardwert erstellt. Wenn von getHostName ein leerer Wert zurückgegeben wird, wird die getHostAddress\(\).toString\(\)\-Methode aufgerufen.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  