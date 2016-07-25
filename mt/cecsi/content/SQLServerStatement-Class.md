---
title: "SQLServerStatement-Klasse"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ec24963c-8b51-4838-91e9-1fbfa2347451
caps.latest.revision: 14
caps.handback.revision: 14
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
# SQLServerStatement-Klasse
  Stellt die grundlegende Implementierung der JDBC\-Anweisungsfunktion dar.  
  
 **Paket:** com.microsoft.sqlserver.jdbc  
  
 **Implementiert:** [ISQLServerStatement](../content/ISQLServerStatement-Interface.md)  
  
## Syntax  
  
```  
  
public class SQLServerStatement  
```  
  
## Hinweise  
 Von der SQLServerStatement\-Klasse wird außerdem eine Reihe von Basisklassenimplementierungsmethoden für die JDBC\-vorbereitete Anweisung und aufrufbare Anweisungen bereitgestellt. Standardmäßig werden von der SQLServerStatement\-Klasse SQL\-Anweisungen ausgeführt und anschließend Updatezählungen und Resultsets an die Benutzeranwendung zurückgegeben.  
  
 Diese Klasse unterstützt das Entpacken in die Klasse SQLServerStatement, die Schnittstelle ISQLServerStatement und die Schnittstelle  java.sql.Statement. Weitere Informationen finden Sie unter [Wrapper und Schnittstellen](../content/Wrappers-and-Interfaces.md).  
  
## Siehe auch  
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [API-Referenz für den JDBC-Treiber](../content/JDBC-Driver-API-Reference.md)  
  
  