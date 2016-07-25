---
title: "updateNClob-Methode (int, java.io.Reader, long)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2bdbb539-0cb9-4047-98e3-7d6906af68f8
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
# updateNClob-Methode (int, java.io.Reader, long)
  Aktualisiert die angegebene Spalte unter Verwendung des angegebenen Reader\-Objekts, dessen Länge der angegebenen Zeichenanzahl entspricht.  
  
## Syntax  
  
```  
  
public void updateNClob(int columnIndex,  
                        java.io.Reader reader,  
                        long length)  
```  
  
#### Parameter  
 *columnIndex*  
  
 Ein Wert vom Typ **int** zum Angeben des Spaltenindex.  
  
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
  
  