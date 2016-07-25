---
title: "unwrap-Methode (SQLServerStatement)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ce680176-ef04-4e44-bb6c-ec50bd06e7e6
caps.latest.revision: 22
caps.handback.revision: 21
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
# unwrap-Methode (SQLServerStatement)
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
 Die [unwrap](../content/unwrap-Method--SQLServerStatement-.md)\-Methode wird von der java.sql.Wrapper\-Schnittstelle definiert, die in den JDBC 4.0\-Spezifikationen eingeführt wird.  
  
 Von den Anwendungen muss u. U. auf [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-spezifische JDBC\-API\-Erweiterungen zugegriffen werden. Die unwrap\-Methode unterstützt das Entpacken in öffentliche, von diesem Objekt erweiterte Klassen, wenn von den Klassen Herstellererweiterungen verfügbar gemacht werden.  
  
 Beim Aufrufen dieser Methode wird das Objekt in die [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Klasse entpackt.  
  
 Beispielcode finden Sie unter [Beispiel zum Aktualisieren umfangreicher Daten](../content/Updating-Large-Data-Sample.md) oder unter [unwrap-Methode &#40;SQLServerCallableStatement&#41;](../content/unwrap-Method--SQLServerCallableStatement-.md).  
  
 Weitere Informationen finden Sie unter [Wrapper und Schnittstellen](../content/Wrappers-and-Interfaces.md).  
  
## Siehe auch  
 [isWrapperFor-Methode &#40;SQLServerStatement&#41;](../content/isWrapperFor-Method--SQLServerStatement-.md)   
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  