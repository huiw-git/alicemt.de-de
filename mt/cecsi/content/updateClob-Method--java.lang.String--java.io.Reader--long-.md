---
title: "updateClob-Methode (java.lang.String, java.io.Reader, long)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6b8f759a-ce5d-41b2-b6cc-24a3ab299f1f
caps.latest.revision: 14
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
# updateClob-Methode (java.lang.String, java.io.Reader, long)
  Aktualisiert die angegebene Spalte unter Verwendung des angegebenen Reader\-Objekts, dessen Länge der angegebenen Zeichenanzahl entspricht.  
  
## Syntax  
  
```  
  
public void updateClob(java.lang.String columnLabel,  
                        java.io.Reader reader,  
                        long length)  
```  
  
#### Parameter  
 *columnLabel*  
  
 Ein **String** mit der Spaltenbezeichnung.  
  
 *reader*  
  
 Ein Reader\-Objekt.  
  
 *length*  
  
 Die Anzahl von Zeichen in den Parameterdaten.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese updateClob\-Methode wird von der updateClob\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
## Siehe auch  
 [updateClob-Methode &#40;ISQLServerResultSet&#41;](../content/updateClob-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  