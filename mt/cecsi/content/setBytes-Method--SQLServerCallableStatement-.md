---
title: "setBytes-Methode (SQLServerCallableStatement)"
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
  - SQLServerCallableStatement.setBytes
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: f264f1a6-ee35-4eaf-81d8-ecf99f03b35d
caps.latest.revision: 13
caps.handback.revision: 13
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
# setBytes-Methode (SQLServerCallableStatement)
  Legt den angegebenen Parameter auf das angegebene Array von **byte**\-Werten fest.  
  
## Syntax  
  
```  
  
public void setBytes(java.lang.String sCol,  
                     byte[] b)  
```  
  
#### Parameter  
 *sCol*  
  
 Ein **String** mit dem Parameternamen.  
  
 *b*  
  
 Ein Array von Werten vom Typ **byte**.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 In einer früheren Version des Treibers konnten Sie mithilfe von "SQLServerCallableStatement.setBytes" Werte zwischen Bytearrays und dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentyp **date**, **time**, **datetime2** oder  **datetimeoffset** konvertieren. Nun wird durch Verwendung der Methode mit diesen Datentypen eine Ausnahme ausgelöst, die angibt, dass die Konvertierung nicht unterstützt wird.  
  
 Diese setBytes\-Methode wird von der setBytes\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  