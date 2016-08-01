---
title: "getSubString-Methode (SQLServerClob)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLServerClob.getSubString
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: bf915590-a883-4403-befa-5b5bb42f34d8
caps.latest.revision: 10
caps.handback.revision: 9
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
# getSubString-Methode (SQLServerClob)
    
## getSubString\-Methode \(SQLServerClob\)  
 Gibt eine Kopie der angegebenen Teilzeichenfolge im CLOB auf der Grundlage der angegebenen Startposition und der Anzahl der zu kopierenden Zeichen zurück.  
  
## Syntax  
  
```  
  
public java.lang.String getSubString(long pos,  
                                     int length)  
```  
  
#### Parameter  
 *pos*  
  
 Das erste Zeichen der zu extrahierenden Teilzeichenfolge. Das erste Zeichen befindet sich an Position 1.  
  
 *length*  
  
 Die Anzahl der aufeinanderfolgenden und zu kopierenden Zeichen.  
  
## Rückgabewert  
 Ein **String** , bei dem es sich um die angegebene Teilzeichenfolge im CLOB handelt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getSubString\-Methode wird von der getSubString\-Methode in der java.sql.Clob\-Schnittstelle angegeben.  
  
 Beim Versuch, null Zeichen aus einem leeren CLOB oder aus einem CLOB mit der Länge Null abzurufen, wird eine leere Zeichenfolge zurückgegeben. Beim Versuch, aus einem CLOB mit der Länge Null eine beliebige Zeichenlänge an einer beliebigen Position \(und nicht von Position 1\) abzurufen, wird eine Positionsausnahme ausgelöst.  
  
## Siehe auch  
 [SQLServerClob-Methoden](../content/SQLServerClob-Methods.md)   
 [SQLServerClob-Elemente](../content/SQLServerClob-Members.md)   
 [SQLServerClob-Klasse](../content/SQLServerClob-Class.md)  
  
  