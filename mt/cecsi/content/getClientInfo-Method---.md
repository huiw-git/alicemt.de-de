---
title: "getClientInfo-Methode ()"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b06a5ced-b760-4c78-b17e-854ce95a1a5c
caps.latest.revision: 16
caps.handback.revision: 16
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
# getClientInfo-Methode ()
  Ruft eine Liste mit dem Namen und dem aktuellen Wert der einzelnen Clientinformationseigenschaften ab, die vom JDBC\-Treiber unterstützt werden.  
  
## Syntax  
  
```  
  
public java.util.Properties getClientInfo()  
```  
  
## Rückgabewert  
 Ein Properties\-Objekt mit dem Namen und dem aktuellen Wert der einzelnen Clientinformationseigenschaften, die vom JDBC\-Treiber unterstützt werden.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getClientInfo\-Methode wird von der getClientInfo\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
 Von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] werden keine Eigenschaften für Clientinformationen unterstützt. Daher wird von dieser Methode ein leeres Properties\-Objekt zurückgegeben.  
  
 Entsprechend kann die [getClientInfoProperties](../content/getClientInfoProperties-Method--SQLServerDatabaseMetaData-.md)\-Methode der [SQLServerDatabaseMetaData](../content/SQLServerDatabaseMetaData-Class.md)\-Klasse von Anwendungen zum Abrufen einer Liste mit vom Treiber unterstützten Eigenschaften für Clientinformationen verwendet werden. Die [getClientInfoProperties](../content/getClientInfoProperties-Method--SQLServerDatabaseMetaData-.md)\-Methode gibt ein leeres Resultset zurück.  
  
## Siehe auch  
 [getClientInfo-Methode &#40;SQLServerConnection&#41;](../content/getClientInfo-Method--SQLServerConnection-.md)   
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  