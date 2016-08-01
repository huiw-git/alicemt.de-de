---
title: "executeUpdate-Methode (SQLServerStatement)"
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
  - SQLServerStatement.executeUpdate
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 10ae662a-ce3c-4b24-875c-5c2df319d93b
caps.latest.revision: 16
caps.handback.revision: 15
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
# executeUpdate-Methode (SQLServerStatement)
  Führt die angegebene SQL\-Anweisung aus. Hierbei kann es sich um eine Anweisung vom Typ "INSERT", "UPDATE" oder "DELETE" oder um eine SQL\-Anweisung handeln, von der nichts zurückgegeben wird \(beispielsweise eine SQL\-DDL\-Anweisung\). Ab [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 wird von executeUpdate die korrekte Anzahl Zeilen zurückgegeben, die in einem MERGE\-Vorgang aktualisiert wurde.  
  
## Überladungsliste  
  
|Name|Beschreibung|  
|----------|------------------|  
|[executeUpdate \(java.lang.String\)](../content/executeUpdate-Method--java.lang.String---SQLServerStatement-.md)|Führt die angegebene SQL\-Anweisung aus. Hierbei kann es sich um eine Anweisung vom Typ "INSERT", "UPDATE", "DELETE" oder "MERGE" oder um eine SQL\-Anweisung handeln, von der nichts zurückgegeben wird \(beispielsweise eine SQL\-DDL\-Anweisung\).|  
|[executeUpdate \(java.lang.String, int\)](../content/executeUpdate-Method--java.lang.String--int-.md)|Führt die angegebene SQL\-Anweisung aus und signalisiert [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] mit dem angegebenen Flag, ob die automatisch generierten Schlüssel, die von diesem [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt erstellt werden, zum Abrufen verfügbar gemacht werden sollen.|  
|[executeUpdate \(java.lang.String, int&#91;&#93;\)](../content/executeUpdate-Method--java.lang.String--int[]-.md)|Führt die angegebene SQL\-Anweisung aus und signalisiert dem JDBC\-Treiber, dass die automatisch generierten Schlüssel, die in dem angegebenen Array angegeben sind, zum Abrufen verfügbar gemacht werden sollen.|  
|[executeUpdate \(java.lang.String, java.lang.String&#91;&#93;\)](../content/executeUpdate-Method--java.lang.String--java.lang.String-.md)|Führt die angegebene SQL\-Anweisung aus und signalisiert dem JDBC\-Treiber, dass die automatisch generierten Schlüssel, die in dem angegebenen Array angegeben sind, zum Abrufen verfügbar gemacht werden sollen.|  
  
## Siehe auch  
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  