---
title: "setFailoverPartner-Methode (SQLServerDataSource)"
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
  - SQLServerDataSource.setFailoverPartner
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 5310b7c2-9d10-474f-ad3a-218fe5da694b
caps.latest.revision: 17
caps.handback.revision: 17
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
# setFailoverPartner-Methode (SQLServerDataSource)
    
## setFailoverPartner\-Methode \(SQLServerDataSource\)  
 Legt den Namen des Failoverservers fest, der in einer Datenbankspiegelungskonfiguration verwendet wird.  
  
## Syntax  
  
```  
  
public void setFailoverPartner(java.lang.String serverName)  
```  
  
#### Parameter  
 *serverName*  
  
 Ein **String** mit dem Namen des Failoverservers.  
  
## Hinweise  
 Der von dieser Methode festgelegte Wert wird im Falle eines Fehlers beim erstmaligen Herstellen einer Verbindung mit dem Prinzipalserver verwendet. Sobald die Verbindung hergestellt wurde, wird dieser Wert ignoriert. In Verbindung mit dieser Methode muss auch die [setDatabaseName](../content/setDatabaseName-Method--SQLServerDataSource-.md)\-Methode verwendet werden, da andernfalls eine Ausnahme ausgelöst wird.  
  
 Bei festgelegtem Failoverservernamen wird das Angeben der Portnummer des Failoverservers vom Treiber nicht unterstützt. Das Aufrufen der [setServerName](../content/setServerName-Method--SQLServerDataSource-.md)\-Methode und der [setInstanceName](../content/setInstanceName-Method--SQLServerDataSource-.md)\-Methode mit der [setFailoverPartner](../content/setFailoverPartner-Method--SQLServerDataSource-.md)\-Methode wird jedoch unterstützt.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  