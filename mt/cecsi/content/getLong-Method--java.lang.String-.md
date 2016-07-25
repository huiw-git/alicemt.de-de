---
title: "getLong-Methode (java.lang.String)"
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
  - SQLServerCallableStatement.getLong (java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 92e30537-5fd9-4b67-8b0f-486c6e840e03
caps.latest.revision: 11
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
# getLong-Methode (java.lang.String)
    
## getLong\-Methode \(java.lang.String\)  
 Ruft den Wert des angegebenen Parameters unter Berücksichtigung des Parameternamens als ein Objekt vom Typ **long** in der Programmiersprache Java ab.  
  
## Syntax  
  
```  
  
public long getLong(java.lang.String sCol)  
```  
  
#### Parameter  
 *sCol*  
  
 Ein **String** mit dem Parameternamen.  
  
## Rückgabewert  
 Ein Wert vom Typ **long** .  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getLong\-Methode wird von der getLong\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
 Die Methode wird nur unter [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentypen unterstützt, die einen Ganzzahlwert wie **bigint**, **int**, **smallint**, **tinyint** und **bit** sicher zurückgeben. Bei Verwendung dieser Methode für andere Datentypen wird eine Ausnahme ausgelöst.  
  
## Siehe auch  
 [getLong-Methode &#40;SQLServerCallableStatement&#41;](../content/getLong-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  