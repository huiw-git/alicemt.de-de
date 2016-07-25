---
title: "SQLServerException-Klasse"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: af5ef257-7cf6-4db3-b1ee-07d22d82bef1
caps.latest.revision: 9
caps.handback.revision: 8
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
# SQLServerException-Klasse
  Stell die fehlerhafte oder unvollständige Ausführung einer SQL\-Anweisung dar.  
  
 **Paket:** com.microsoft.sqlserver.jdbc  
  
 **Erweitert:** java.sql.SQLException  
  
 **Implementiert:** java.io.Serializable  
  
## Syntax  
  
```  
  
public final class SQLServerException  
```  
  
## Hinweise  
 Die SQLServerException\-Klasse behandelt sowohl SQL 92\- als auch XOPEN\-Statuscodes. Diese verwenden eine vom Benutzer angegebene Verbindungseigenschaft und sind daher wechselbar. Ausnahmen werden in die angegebenen offenen Protokolldateien geschrieben.  
  
## Siehe auch  
 [SQLServerException-Elemente](../content/SQLServerException-Members.md)   
 [API-Referenz für den JDBC-Treiber](../content/JDBC-Driver-API-Reference.md)  
  
  