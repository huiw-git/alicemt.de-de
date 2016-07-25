---
title: "getBytes-Methode (java.lang.String)"
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
  - SQLServerCallableStatement.getBytes (java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 4d0dac7f-7f39-47a2-953e-80ab03688d82
caps.latest.revision: 12
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
# getBytes-Methode (java.lang.String)
  Ruft den Wert des angegebenen Parameters unter Berücksichtigung des Parameternamens als ein Array von Bytewerten ab.  
  
## Syntax  
  
```  
  
public byte[] getBytes(java.lang.String sCol)  
```  
  
#### Parameter  
 *sCol*  
  
 Ein **String** mit dem Parameternamen.  
  
## Rückgabewert  
 Ein Array von Werten vom Typ **byte**.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 In einer früheren Version von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] konnten Sie mithilfe von "SQLServerCallableStatement.getBytes" Werte zwischen Bytearrays und dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentyp **date**, **time**, **datetime2** oder **datetimeoffset** konvertieren. Nun wird durch Verwendung der Methode mit diesen Datentypen eine Ausnahme ausgelöst, die angibt, dass die Konvertierung nicht unterstützt wird.  
  
 Diese getBytes\-Methode wird von der getBytes\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [getBytes-Methode &#40;SQLServerCallableStatement&#41;](../content/getBytes-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  