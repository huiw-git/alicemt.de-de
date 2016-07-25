---
title: "setClientInfo-Methode (java.lang.String, java.lang.String)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8d050831-8305-48a8-bd22-207932111040
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
# setClientInfo-Methode (java.lang.String, java.lang.String)
  Legt den Wert der angegebenen Eigenschaft für Clientinformationen fest.  
  
## Syntax  
  
```  
  
public void setClientInfo (java.lang.String name,  
                           java.lang.String value)  
```  
  
#### Parameter  
 *name*  
  
 Ein String mit dem Namen der festzulegenden Eigenschaft für Clientinformationen.  
  
 *value*  
  
 Ein String mit dem Wert, auf den die Eigenschaft für Clientinformationen festgelegt werden soll.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setClientInfo\-Methode wird von der setClientInfo\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
 Von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] werden keine Eigenschaften für Clientinformationen unterstützt. In der JDBC Driver\-Version 2.0 wird von dieser Methode eine Warnung für eine Eigenschaft generiert. Zum Abrufen einer Warnung sollte von Anwendungen die [getWarnings](../content/getWarnings-Method--SQLServerConnection-.md)\-Methode der [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Klasse verwendet werden.  
  
## Siehe auch  
 [setClientInfo-Methode &#40;ISQLServerConnection&#41;](../content/setClientInfo-Method--SQLServerConnection-.md)   
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  