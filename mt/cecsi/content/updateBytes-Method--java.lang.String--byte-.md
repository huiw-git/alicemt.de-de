---
title: "updateBytes-Methode (java.lang.String, byte)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLServerResultSet.updateBytes (java.lang.String, byte[])
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 4fb9de2b-61bc-4c96-89a5-c07cd7ee201a
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
# updateBytes-Methode (java.lang.String, byte)
  Aktualisiert die angegebene Spalte mit einem Array von **byte**\-Werten unter Berücksichtigung des Spaltennamens.  
  
## Syntax  
  
```  
  
public void updateBytes(java.lang.String columnName,  
                        byte[] x)  
```  
  
#### Parameter  
 *columnName*  
  
 Ein **String** mit dem Spaltennamen.  
  
 *x*  
  
 Ein Array von Werten vom Typ **byte**.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese updateBytes\-Methode wird von der updateBytes\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 In einer früheren Version von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] konnten Sie mithilfe von "SQLServerResultSet.updateBytes" Werte zwischen Bytearrays und dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentyp **date**, **time**, **datetime2** oder **datetimeoffset** konvertieren. Nun wird durch Verwendung der Methode mit diesen Datentypen eine Ausnahme ausgelöst, die angibt, dass die Konvertierung nicht unterstützt wird.  
  
## Siehe auch  
 [updateBytes-Methode &#40;SQLServerResultSet&#41;](../content/updateBytes-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  