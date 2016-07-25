---
title: "updateNClob-Methode (java.lang.String, java.sql.NClob)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a025d124-3634-49fa-8bb5-e9b98f2d5de3
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
# updateNClob-Methode (java.lang.String, java.sql.NClob)
  Aktualisiert die angegebene Spalte mit einem **NClob**\-Wert.  
  
## Syntax  
  
```  
  
public void updateNClob(java.lang.String columnLabel,  
                        java.sql.NClob x)  
```  
  
#### Parameter  
 *columnLabel*  
  
 Ein **String** zum Angeben der Spaltenbezeichnung.  
  
 *x*  
  
 Ein NClob\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese updateNClob\-Methode wird von der updateNClob\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Diese Methode wird nur für Spalten vom Typ **nvarchar\(max\)**, **ntext** und **xml** unterstützt. Bei Verwendung dieser Methode für andere Datentypen wird eine Ausnahme ausgelöst.  
  
## Siehe auch  
 [updateNClob-Methode &#40;ISQLServerResultSet&#41;](../content/updateNClob-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  