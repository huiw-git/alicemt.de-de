---
title: "unwrap-Methode (SQLServerXADataSource)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d97c99b3-2224-4abb-8b32-40aff49fe759
caps.latest.revision: 11
caps.handback.revision: 10
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
# unwrap-Methode (SQLServerXADataSource)
  Gibt ein Objekt zurück, das die angegebene Schnittstelle implementiert, um den Zugriff auf die [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-spezifischen Methoden zu ermöglichen.  
  
## Syntax  
  
```  
  
public <T> T unwrap(Class<T> iface)  
```  
  
#### Parameter  
 *iface*  
  
 Eine Klasse vom Typ **T** zum Definieren einer Schnittstelle.  
  
## Rückgabewert  
 Ein Objekt, von dem die angegebene Schnittstelle implementiert wird.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Die [unwrap](../content/unwrap-Method--SQLServerXADataSource-.md)\-Methode wird von der java.sql.Wrapper\-Schnittstelle definiert, die in den JDBC 4.0\-Spezifikationen eingeführt wird.  
  
 Von den Anwendungen muss u. U. auf [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-spezifische JDBC\-API\-Erweiterungen zugegriffen werden. Die unwrap\-Methode unterstützt das Entpacken in öffentliche, von diesem Objekt erweiterte Klassen, wenn von den Klassen Herstellererweiterungen verfügbar gemacht werden.  
  
 Von der [SQLServerXADataSource](../content/SQLServerXADataSource-Class.md)\-Klasse wird die [SQLServerConnectionPoolDataSource](../content/SQLServerConnectionPoolDataSource-Class.md)\-Klasse erweitert, die von der [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Klasse aus erweitert wird. Beim Aufrufen dieser Methode wird das Objekt in die folgenden Klassen entpackt: [SQLServerDataSource](../content/SQLServerDataSource-Class.md), [SQLServerConnectionPoolDataSource](../content/SQLServerConnectionPoolDataSource-Class.md) und [SQLServerXADataSource](../content/SQLServerXADataSource-Class.md).  
  
 Weitere Informationen finden Sie unter [Wrapper und Schnittstellen](../content/Wrappers-and-Interfaces.md).  
  
## Siehe auch  
 [SQLServerXADataSource-Methoden](../content/SQLServerXADataSource-Methods.md)   
 [SQLServerXADataSource-Elemente](../content/SQLServerXADataSource-Members.md)   
 [SQLServerXADataSource-Klasse](../content/SQLServerXADataSource-Class.md)  
  
  