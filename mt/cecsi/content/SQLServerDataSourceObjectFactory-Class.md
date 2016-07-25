---
title: "SQLServerDataSourceObjectFactory-Klasse"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b616632b-5987-470d-b36c-b22fa9213145
caps.latest.revision: 12
caps.handback.revision: 11
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
# SQLServerDataSourceObjectFactory-Klasse
  Stellt ein Objektfactory zum Materialisieren von Datenquellen aus der JNDI \(Java Naming and Directory Interface\) dar.  
  
 **Paket:** com.microsoft.sqlserver.jdbc  
  
 **Erweitert:** java.lang.Object  
  
 **Implementiert:** javax.naming.spi.ObjectFactory  
  
## Syntax  
  
```  
  
public class SQLServerDataSourceObjectFactory  
```  
  
## Hinweise  
 Diese Methode wird von allen Datenquellenklassen geerbt. Diese Klasse, von der ein [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-Objekt implementiert wird, wird von ObjectFactory als Teil der Unterstützung der Referenceable\-Schnittstelle verfügbar gemacht. Von Java\-Anwendungsservern wird getReference für Datenquellenklassen aufgerufen, wodurch ein Reference\-Objekt erstellt wird, von dem der Klassenname intern als Klassenfactory verwendet wird.  
  
 Wenn das Reference\-Objekt vom Java\-Anwendungsserver dereferenziert werden muss, wird eine Instanz des SQLServerDataSourceObjectFactory\-Objekts erstellt und die [getObjectInstance](../content/getObjectInstance-Method--SQLServerDataSourceObjectFactory-.md)\-Methode aufgerufen, um die Datenquellinstanz abzurufen. Dabei wird das Reference\-Objekt übergeben.  
  
## Siehe auch  
 [SQLServerDataSourceObjectFactory-Elemente](../content/SQLServerDataSourceObjectFactory-Members.md)   
 [API-Referenz für den JDBC-Treiber](../content/JDBC-Driver-API-Reference.md)  
  
  