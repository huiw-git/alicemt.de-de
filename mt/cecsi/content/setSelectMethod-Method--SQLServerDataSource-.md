---
title: "setSelectMethod-Methode (SQLServerDataSource)"
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
  - SQLServerDataSource.setSelectMethod
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 7934276d-5ac9-4cbc-a2a0-2c65c93733ac
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
# setSelectMethod-Methode (SQLServerDataSource)
    
## setSelectMethod\-Methode \(SQLServerDataSource\)  
 Legt den Standardcursortyp fest, der für alle Resultsets verwendet wird, die mithilfe dieses [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Objekts erstellt werden.  
  
## Syntax  
  
```  
  
public void setSelectMethod(java.lang.String selectMethod)  
```  
  
#### Parameter  
 *selectMethod*  
  
 Ein Wert vom Typ **String** mit dem Standardcursortyp.  
  
## Hinweise  
 "selectMethod" ist der Standardcursortyp, der für ein Resultset verwendet wird. Diese Eigenschaft ist nützlich für die Verarbeitung großer Resultsets ohne dass das gesamte Resultset im clientseitigen Speicher abgelegt wird. Wenn Sie die Eigenschaft auf "cursor" festlegen, können Sie einen serverseitigen Cursor erstellen, der jeweils kleinere Datenauschnitte abrufen kann. Wenn die selectMethod\-Eigenschaft nicht festgelegt ist, gibt [getSelectMethod](../content/getSelectMethod-Method--SQLServerDataSource-.md) den Standardwert "direct" zurück.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  