---
title: "getFailoverPartner-Methode (SQLServerDataSource)"
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
  - SQLServerDataSource.getFailoverPartner
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 885f927f-9c48-42e0-a7fb-fd936d2b8130
caps.latest.revision: 12
caps.handback.revision: 12
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
# getFailoverPartner-Methode (SQLServerDataSource)
    
## getFailoverPartner\-Methode \(SQLServerDataSource\)  
 Gibt den Namen des Failoverservers zurück, der in einer Datenbankspiegelungskonfiguration verwendet wird.  
  
## Syntax  
  
```  
  
public string getFailoverPartner()  
```  
  
## Rückgabewert  
 Ein **String** , der den Namen des Failoverpartners oder NULL enthält, sofern kein Name festgelegt ist.  
  
## Hinweise  
 Der von dieser Methode zurückgegebene Wert gibt den Failoverpartnernamen wieder, der mithilfe der [setFailoverPartner](../content/setFailoverPartner-Method--SQLServerDataSource-.md)\-Methode festgelegt wurde.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  