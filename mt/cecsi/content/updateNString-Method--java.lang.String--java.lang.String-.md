---
title: "updateNString-Methode (java.lang.String, java.lang.String)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6daca03f-c60f-4842-b9e3-11d136e78312
caps.latest.revision: 18
caps.handback.revision: 17
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
# updateNString-Methode (java.lang.String, java.lang.String)
  Aktualisiert die angegebene Spalte mit einem Wert vom Typ **String** unter Verwendung der angegebenen Spaltenbezeichnung.  
  
## Syntax  
  
```  
  
public void updateNString(java.lang.String columnLabel,  
                          java.lang.String nString)  
```  
  
#### Parameter  
 *columnLabel*  
  
 Ein **String** mit der Spaltenbezeichnung.  
  
 *nString*  
  
 Ein **String**\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese updateNString\-Methode wird von der updateNString\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Von dieser Methode wird ein Java\-**String** an ausgewählte Spalten vom Typ **nchar**, **nvarchar\(max\)**, **ntext** und **xml** übergeben. Bei Verwendung dieser Methode für andere Datentypspalten wird eine Ausnahme ausgelöst.  
  
## Siehe auch  
 [updateNString-Methode &#40;ISQLServerResultSet&#41;](../content/updateNString-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  