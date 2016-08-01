---
title: "Abrufen der Treiberversion"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5e241d72-16da-4ada-ac67-e6308394108f
caps.latest.revision: 21
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
# Abrufen der Treiberversion
  Die installierte Version von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] kann wie folgt ermittelt werden:  
  
-   Rufen Sie die [SQLServerDatabaseMetaData](../content/SQLServerDatabaseMetaData-Class.md)\-Methoden [getDriverMajorVersion](../content/getDriverMajorVersion-Method--SQLServerDatabaseMetaData-.md), [getDriverMinorVersion](../content/getDriverMinorVersion-Method--SQLServerDatabaseMetaData-.md) oder [getDriverVersion](../content/getDriverVersion-Method--SQLServerDatabaseMetaData-.md) auf.  
  
-   Die Version wird in der Datei readme.txt für das Produkt angezeigt.  
  
 Außerdem kann der JDBC\-Treibername mit dem [getDriverName](../content/getDriverName-Method--SQLServerDatabaseMetaData-.md)\-Methodenaufruf für die SQLServerDatabaseMetaData\-Klasse zurückgegeben werden. Dabei wird beispielsweise "Microsoft JDBC Driver 4.0 für SQL Server" zurückgegeben.  
  
 Im Folgenden wird ein Beispiel für die Ausgabe von Aufrufen der Methoden in der SQLServerDatabaseMetaData\-Klasse bereitgestellt:  
  
 `getDriverName = Microsoft JDBC Driver 4.0 for SQL Server`  
  
 `getDriverMajorVersion = 4`  
  
 `getDriverMinorVersion = 0`  
  
 `getDriverVersion = 4.0.` *xxx.x*  
  
 Dabei ist "xxx.x" die abschließende Versionsnummer.  
  
## Siehe auch  
 [Diagnostizieren von Problemen mit dem JDBC-Treiber](../content/Diagnosing-Problems-with-the-JDBC-Driver.md)  
  
  