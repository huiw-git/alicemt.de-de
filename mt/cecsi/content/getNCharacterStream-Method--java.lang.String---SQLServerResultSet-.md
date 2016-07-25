---
title: "getNCharacterStream-Methode (java.lang.String) (SQLServerResultSet)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a117f3a3-9c25-41e1-9adb-a40e90620dd6
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
# getNCharacterStream-Methode (java.lang.String) (SQLServerResultSet)
  Ruft den Wert der angegebenen Spalte in der aktuellen Zeile des [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Reader\-Objekt ab.  
  
## Syntax  
  
```  
  
public java.io.Reader getNCharacterStream(java.lang.String columnLabel)  
```  
  
#### Parameter  
 *columnLabel*  
  
 Ein String mit der Spaltenbezeichnung.  
  
## Rückgabewert  
 Ein Reader\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getNCharacterStream\-Methode wird von der getNCharacterStream\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Mit dieser Methode kann der Wert einer Spalte vom Typ **nvarchar**, **nchar**, **nvarchar\(max\)**, **ntext** oder **xml** in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts abgerufen werden. Beim Versuch, mit dieser Methode Werte anderer Datentypen abzurufen, wird eine Ausnahme ausgelöst.  
  
## Siehe auch  
 [getNCharacterStream-Methode &#40;ISQLServerResultSet&#41;](../content/getNCharacterStream-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)  
  
  