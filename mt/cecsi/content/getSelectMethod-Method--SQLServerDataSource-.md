---
title: "getSelectMethod-Methode (SQLServerDataSource)"
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
  - SQLServerDataSource.getSelectMethod
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: b6255d2e-0028-474a-afa8-553ef092243e
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
# getSelectMethod-Methode (SQLServerDataSource)
    
## getSelectMethod\-Methode \(SQLServerDataSource\)  
 Gibt den Standardcursortyp zurück, der für alle Resultsets verwendet wird, die mithilfe dieses [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Objekts erstellt werden.  
  
## Syntax  
  
```  
  
public java.lang.String getSelectMethod()  
```  
  
## Rückgabewert  
 Ein Wert vom Typ **String** mit dem Standardcursortyp.  
  
## Hinweise  
 Die selectMethod\-Eigenschaft gibt den Standardcursortyp an, der für ein Resultset verwendet wird. Diese Eigenschaft ist nützlich für die Verarbeitung großer Resultsets ohne dass das gesamte Resultset im clientseitigen Speicher abgelegt wird. Wenn Sie die Eigenschaft auf "cursor" festlegen, können Sie einen serverseitigen Cursor erstellen, der jeweils kleinere Datenauschnitte abrufen kann. Wenn die selectMethod\-Eigenschaft nicht festgelegt ist, gibt getSelectMethod den Standardwert "direct" zurück.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  