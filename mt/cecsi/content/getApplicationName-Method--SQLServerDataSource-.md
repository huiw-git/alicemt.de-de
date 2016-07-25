---
title: "getApplicationName-Methode (SQLServerDataSource)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLServerDataSource.getApplicationName
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: f71e501c-ccd7-4a1e-b6ea-4d47a81c18c6
caps.latest.revision: 13
caps.handback.revision: 12
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
# getApplicationName-Methode (SQLServerDataSource)
  Gibt den Anwendungsnamen zurück.  
  
## Syntax  
  
```  
  
public java.lang.String getApplicationName()  
```  
  
## Rückgabewert  
 Ein **String**, der den Anwendungsnamen enthält, oder "[!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]", wenn kein Wert festgelegt ist.  
  
## Hinweise  
 Anhand des Anwendungsnamens wird die jeweilige Anwendung in den verschiedenen Profilerstellungs\- und Protokollierungstools von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] identifiziert. Ist der Anwendungsname nicht festgelegt, wird von der getApplicationName\-Methode die nicht lokalisierte Zeichenfolge "[!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]" zurückgegeben.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  