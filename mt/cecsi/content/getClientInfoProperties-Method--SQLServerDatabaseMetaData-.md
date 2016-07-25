---
title: "getClientInfoProperties-Methode (SQLServerDatabaseMetaData)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1568aef4-f4c4-40a0-a1ab-9c106905bd92
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
# getClientInfoProperties-Methode (SQLServerDatabaseMetaData)
  Ruft eine Liste mit den Eigenschaften für Clientinformationen ab, die vom Treiber unterstützt werden.  
  
## Syntax  
  
```  
  
public java.sql.ResultSet getClientInfoProperties()  
```  
  
## Rückgabewert  
 Ein ResultSet\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getClientInfoProperties\-Methode wird von der getClientInfoProperties\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
> [!NOTE]  
>  Von dieser Methode wird ein leeres Resultset zurückgegeben. Vom Treiber wird nur das Festlegen von **applicationName** unterstützt. **applicationName** wird erst zum Zeitpunkt der Verbindungsherstellung festgelegt. Das Aktualisieren der Clientanwendungsinformationen nach der Verbindungsherstellung wird von SQL Server nicht unterstützt.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  