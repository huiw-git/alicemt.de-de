---
title: "SQLServerParameterMetaData-Klasse"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 546290e0-9411-4a2b-aa36-61251e70e9cf
caps.latest.revision: 10
caps.handback.revision: 9
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
# SQLServerParameterMetaData-Klasse
  Stellt die Metadaten für die Parameter vorbereiteter Anweisungen dar.  
  
 **Paket:** com.microsoft.sqlserver.jdbc  
  
 **Erweitert:** java.lang.Object  
  
 **Implementiert:** java.sql.ParameterMetaData  
  
## Syntax  
  
```  
  
public class SQLServerParameterMetaData  
```  
  
## Hinweise  
 Zum Abrufen der Metadaten von Parametern werden vorbereitete Anweisungen mit SET FMT ONLY ausgeführt. Von aufrufbaren Anweisungen wird "sp\_sproc\_columns" aufgerufen, um Namen und Metadaten für die Prozedurparameter abzurufen.  
  
## Siehe auch  
 [SQLServerParameterMetaData-Elemente](../content/SQLServerParameterMetaData-Members.md)   
 [API-Referenz für den JDBC-Treiber](../content/JDBC-Driver-API-Reference.md)  
  
  