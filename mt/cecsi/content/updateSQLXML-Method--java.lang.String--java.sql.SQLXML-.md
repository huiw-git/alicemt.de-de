---
title: "updateSQLXML-Methode (java.lang.String, java.sql.SQLXML)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 60021881-ef83-499b-9977-e20ff23c1312
caps.latest.revision: 8
caps.handback.revision: 8
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
# updateSQLXML-Methode (java.lang.String, java.sql.SQLXML)
  Aktualisiert die angegebene Spalte mit einem java.sql.SQLXML\-Wert.  
  
## Syntax  
  
```  
  
public void updateSQLXML(java.lang.String columnLabel,  
                         java.sql.SQLXML xmlObject)  
```  
  
#### Parameter  
 *columnLabel*  
  
 Ein **String** zum Angeben der Spaltenbezeichnung.  
  
 *xmlObject*  
  
 Ein SQLXML\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese updateSQLXML\-Methode wird von der updateSQLXML\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
## Siehe auch  
 [updateSQLXML-Methode &#40;ISQLServerResultSet&#41;](../content/updateSQLXML-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  