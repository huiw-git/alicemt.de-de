---
title: "getShort-Methode (java.lang.String)"
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
  - SQLServerCallableStatement.getShort (java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: cd39ed03-b3e8-443d-9c7a-e8cf2581e581
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
# getShort-Methode (java.lang.String)
    
## getShort\-Methode \(java.lang.String\)  
 Ruft den Wert des angegebenen Parameters unter Berücksichtigung des Parameternamens als ein **short** \-Objekt in der Programmiersprache Java ab.  
  
## Syntax  
  
```  
  
public short getShort(java.lang.String sCol)  
```  
  
#### Parameter  
 *sCol*  
  
 Ein **String** mit dem Parameternamen.  
  
## Rückgabewert  
 Ein Wert vom Typ **short** .  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getShort\-Methode wird von der getShort\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
 Die Methode wird nur unter [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentypen unterstützt, die einen Ganzzahlwert wie "smallint", "tinyint" und "bit" sicher zurückgeben. Bei Verwendung dieser Methode für andere Datentypen wird eine Ausnahme ausgelöst.  
  
## Siehe auch  
 [getShort-Methode &#40;SQLServerCallableStatement&#41;](../content/getShort-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  