---
title: "updateNClob-Methode (java.lang.String, java.io.Reader, long)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ad5c8d9b-f8c8-4ddf-85c8-23420bba54ee
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
# updateNClob-Methode (java.lang.String, java.io.Reader, long)
  Aktualisiert die angegebene Spalte unter Verwendung des angegebenen **Reader**\-Objekts, dessen Länge der angegebenen Zeichenanzahl entspricht.  
  
## Syntax  
  
```  
  
public void updateNClob(java.lang.String columnLabel,  
                        java.io.Reader reader,  
                        long length)  
```  
  
#### Parameter  
 *columnLabel*  
  
 Ein **String** zum Angeben der Spaltenbezeichnung.  
  
 *reader*  
  
 Ein Reader\-Objekt.  
  
 *length*  
  
 Die Anzahl von Zeichen in den Parameterdaten.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese updateNClob\-Methode wird von der updateNClob\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Diese Methode wird nur für Spalten vom Typ **nvarchar\(max\)**, **ntext** und **xml** unterstützt. Bei Verwendung dieser Methode für andere Datentypen wird eine Ausnahme ausgelöst.  
  
## Siehe auch  
 [updateNClob-Methode &#40;ISQLServerResultSet&#41;](../content/updateNClob-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  