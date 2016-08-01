---
title: "getClientInfo-Methode (java.lang.String)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e8e632c4-d6cc-4c5e-b6ad-873579343b19
caps.latest.revision: 15
caps.handback.revision: 15
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
# getClientInfo-Methode (java.lang.String)
  Ruft den Wert einer angegebenen Eigenschaft für Clientinformationen ab.  
  
## Syntax  
  
```  
  
public java.lang.String getClientInfo (java.lang.String name)  
```  
  
#### Parameter  
 *name*  
  
 Ein String mit dem Namen der abzurufenden Eigenschaft für Clientinformationen.  
  
## Rückgabewert  
 Ein String mit dem Wert der Eigenschaft für Clientinformationen.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getClientInfo\-Methode wird von der getClientInfo\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
 Von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] werden keine Eigenschaften für Clientinformationen unterstützt. Daher gibt diese Methode einen **null**\-Wert zurück.  
  
 Entsprechend kann die [getClientInfoProperties](../content/getClientInfoProperties-Method--SQLServerDatabaseMetaData-.md)\-Methode der [SQLServerDatabaseMetaData](../content/SQLServerDatabaseMetaData-Class.md)\-Klasse von Anwendungen zum Abrufen einer Liste mit vom Treiber unterstützten Eigenschaften für Clientinformationen verwendet werden. Die [getClientInfoProperties](../content/getClientInfoProperties-Method--SQLServerDatabaseMetaData-.md)\-Methode gibt ein leeres Resultset zurück.  
  
## Siehe auch  
 [getClientInfo-Methode &#40;SQLServerConnection&#41;](../content/getClientInfo-Method--SQLServerConnection-.md)   
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  