---
title: "setClientInfo-Methode (java.util.Properties)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b2a8ec0b-40a2-44d1-90d9-a810d4132e56
caps.latest.revision: 19
caps.handback.revision: 19
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
# setClientInfo-Methode (java.util.Properties)
  Legt den Wert der Eigenschaften für Clientinformationen der Verbindung fest.  
  
## Syntax  
  
```  
  
public void setClientInfo (java.util.Properties properties)  
```  
  
#### Parameter  
 *properties*  
  
 Ein Properties\-Objekt mit der Liste der festzulegenden Eigenschaften für Clientinformationen.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setClientInfo\-Methode wird von der setClientInfo\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
 Von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] werden keine Eigenschaften für Clientinformationen unterstützt. Von dieser Methode werden Warnungen generiert, sofern vom *properties*\-Eingabeparameter nicht auf einen leeren Eigenschaftensatz verwiesen wird. Das heißt, dass von dieser Methode Warnungen für die Eigenschaften generiert werden, die von der Anwendung festgelegt werden sollen. Zum Abrufen der einzelnen Warnungen sollte von Anwendungen die [getWarnings](../content/getWarnings-Method--SQLServerConnection-.md)\-Methode der [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Klasse verwendet werden.  
  
## Siehe auch  
 [setClientInfo-Methode &#40;ISQLServerConnection&#41;](../content/setClientInfo-Method--SQLServerConnection-.md)   
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  