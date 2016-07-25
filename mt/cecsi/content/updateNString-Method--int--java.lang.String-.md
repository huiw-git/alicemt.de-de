---
title: "updateNString-Methode (int, java.lang.String)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1bb909f1-4a96-4be1-adea-36c8d9703112
caps.latest.revision: 17
caps.handback.revision: 16
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
# updateNString-Methode (int, java.lang.String)
  Aktualisiert die angegebene Spalte mit einem **String**\-Wert unter Verwendung des angegebenen Spaltenindex.  
  
## Syntax  
  
```  
  
public void updateNString(int columnIndex,  
                        java.lang.String nString)  
```  
  
#### Parameter  
 *columnIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindex.  
  
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
  
  