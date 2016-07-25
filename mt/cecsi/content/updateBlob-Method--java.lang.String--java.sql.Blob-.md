---
title: "updateBlob-Methode (java.lang.String, java.sql.Blob)"
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
  - SQLServerResultSet.updateBlob (java.lang.String, java.sql.Blob)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: fdd47885-c7ec-4599-a645-ad0e082586f4
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
# updateBlob-Methode (java.lang.String, java.sql.Blob)
    
## updateBlob\-Methode \(java.lang.String, java.sql.Blob\)  
 Aktualisiert die angegebene Spalte mit einem java.sql.Blob\-Wert.  
  
## Syntax  
  
```  
  
public void updateBlob(java.lang.String columnName,  
                       java.sql.Blob x)  
```  
  
#### Parameter  
 *columnName*  
  
 Ein **String** mit dem Spaltennamen.  
  
 *x*  
  
 Ein Blob\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese updateBlob\-Methode wird von der updateBlob\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
## Siehe auch  
 [updateBlob-Methode &#40;ISQLServerResultSet&#41;](../content/updateBlob-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  