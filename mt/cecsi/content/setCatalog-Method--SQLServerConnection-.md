---
title: "setCatalog-Methode (SQLServerConnection)"
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
  - SQLServerConnection.setCatalog
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 553c0603-c07d-436a-86eb-3ba6b51bd696
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
# setCatalog-Methode (SQLServerConnection)
  Legt den angegebenen Katalognamen fest, um einen Teilbereich der Datenbank dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekts auszuwählen, in dem gearbeitet werden soll.  
  
## Syntax  
  
```  
  
public void setCatalog(java.lang.String catalog)  
```  
  
#### Parameter  
 *catalog*  
  
 Ein **String** mit dem Katalognamen.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setCatalog\-Methode wird von der setCatalog\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
 Das *catalog*\-Argument wird von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] automatisch mit Escapezeichen versehen. Bei Verwendung dieser Methode wird die catalog\-Eigenschaft für das Connection\-Objekt festgelegt. Diese wird auf keine andere Weise implizit festgelegt.  
  
## Siehe auch  
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  