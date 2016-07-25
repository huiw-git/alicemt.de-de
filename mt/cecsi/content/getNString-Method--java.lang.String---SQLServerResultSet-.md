---
title: "getNString-Methode (java.lang.String) (SQLServerResultSet)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 546d77e2-723a-42ac-ba3f-fabf2395d376
caps.latest.revision: 15
caps.handback.revision: 14
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
# getNString-Methode (java.lang.String) (SQLServerResultSet)
  Ruft den Wert der angegebenen Spalte in der aktuellen Zeile des [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als java.lang.String\-Objekt ab.  
  
## Syntax  
  
```  
  
public java.lang.String getNString(java.lang.String columnLabel)  
```  
  
#### Parameter  
 *columnLabel*  
  
 Ein String mit der Spaltenbezeichnung.  
  
## Rückgabewert  
 Ein String\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getNString\-Methode wird von der getNString\-Methode in der java.sql.SQLServerResultSet\-Schnittstelle angegeben.  
  
 Mit dieser Methode kann der Wert einer Spalte vom Typ **nvarchar**, **nchar**, **nvarchar\(max\)**, **ntext** oder **xml** in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts abgerufen werden. Beim Versuch, mit dieser Methode Werte anderer Datentypen abzurufen, wird eine Ausnahme ausgelöst.  
  
## Siehe auch  
 [getNString-Methode &#40;SQLServerResultSet&#41;](../content/getNString-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)  
  
  