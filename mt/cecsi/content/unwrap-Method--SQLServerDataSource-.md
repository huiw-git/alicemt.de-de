---
title: "unwrap-Methode (SQLServerDataSource)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: eb8abe29-f3ec-4752-a590-1d5dc3e48f08
caps.latest.revision: 19
caps.handback.revision: 18
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
# unwrap-Methode (SQLServerDataSource)
  Gibt ein Objekt zurück, das die angegebene Schnittstelle implementiert, um den Zugriff auf die [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-spezifischen Methoden zu ermöglichen.  
  
## Syntax  
  
```  
  
public <T> T unwrap(Class<T> iface)  
```  
  
#### Parameter  
 *iface*  
  
 Eine Klasse vom Typ "T" zum Definieren einer Schnittstelle.  
  
## Rückgabewert  
 Ein Objekt, von dem die angegebene Schnittstelle implementiert wird.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Die [unwrap](../content/unwrap-Method--SQLServerDataSource-.md)\-Methode wird von der java.sql.Wrapper\-Schnittstelle definiert, die in den JDBC 4.0\-Spezifikationen eingeführt wird.  
  
 Von den Anwendungen muss u. U. auf [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-spezifische JDBC\-API\-Erweiterungen zugegriffen werden. Die unwrap\-Methode unterstützt das Entpacken in öffentliche, von diesem Objekt erweiterte Klassen, wenn von den Klassen Herstellererweiterungen verfügbar gemacht werden.  
  
 Beim Aufrufen dieser Methode wird das Objekt in die [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Klasse entpackt.  
  
 Weitere Informationen finden Sie unter [Wrapper und Schnittstellen](../content/Wrappers-and-Interfaces.md).  
  
## Siehe auch  
 [isWrapperFor-Methode &#40;SQLServerDataSource&#41;](../content/isWrapperFor-Method--SQLServerDataSource-.md)   
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  