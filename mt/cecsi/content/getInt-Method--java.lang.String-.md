---
title: "getInt-Methode (java.lang.String)"
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
  - SQLServerCallableStatement.getInt (java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 1705812f-1f04-4e84-b6c8-d164dded47b3
caps.latest.revision: 10
caps.handback.revision: 10
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
# getInt-Methode (java.lang.String)
    
## getInt\-Methode \(java.lang.String\)  
 Ruft den Wert des angegebenen Parameters unter Berücksichtigung des Parameternamens als ein **int** \-Objekt in der Programmiersprache Java ab.  
  
## Syntax  
  
```  
  
public int getInt(java.lang.String sCol)  
```  
  
#### Parameter  
 *sCol*  
  
 Ein **String** mit dem Parameternamen.  
  
## Rückgabewert  
 Ein **int** \-Wert.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getInt\-Methode wird von der getInt\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
 Die Methode wird nur für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentypen unterstützt, die einen Ganzzahlwert wie "int", "smallint", "tinyint" und "bit" sicher zurückgeben. Bei Verwendung dieser Methode für andere Datentypen wird eine Ausnahme ausgelöst.  
  
## Siehe auch  
 [getInt-Methode &#40;SQLServerCallableStatement&#41;](../content/getInt-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  