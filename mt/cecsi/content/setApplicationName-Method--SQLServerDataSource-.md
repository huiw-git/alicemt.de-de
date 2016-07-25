---
title: "setApplicationName-Methode (SQLServerDataSource)"
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
  - SQLServerDataSource.setApplicationName
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 24d6e48d-53c4-4da2-a6de-1cdff463c9cd
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
# setApplicationName-Methode (SQLServerDataSource)
  Legt den Anwendungsnamen fest.  
  
## Syntax  
  
```  
  
public void setApplicationName(java.lang.String applicationName)  
```  
  
#### Parameter  
 *applicationName*  
  
 Ein **String** mit dem Namen der Anwendung.  
  
## Hinweise  
 Anhand des Anwendungsnamens wird die jeweilige Anwendung in den verschiedenen Profilerstellungs\- und Protokollierungstools von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] identifiziert. Ist der Anwendungsname nicht festgelegt, wird von der getApplicationName\-Methode die nicht lokalisierte Zeichenfolge "[!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]" zurückgegeben.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  