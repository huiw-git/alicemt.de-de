---
title: "toString-Methode (DateTimeOffset)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e77b9be3-1a02-4769-8acf-ac71d48d6a76
caps.latest.revision: 8
caps.handback.revision: 7
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
# toString-Methode (DateTimeOffset)
    
## toString\-Methode \(DateTimeOffset\)  
 Gibt eine Zeichenfolgendarstellung des **DateTimeOffset**\-Objekts zurück.  
  
## Syntax  
  
```  
  
public String toString()  
```  
  
## Rückgabewert  
 Eine Zeichenfolgendarstellung des **DateTimeOffset**\-Objekts.  
  
## Hinweise  
 Die Zeichenfolge hat das Format *YYYY*\-*MM*\-*DD**hh*:*mm*:*ss*\[.*fffffff*\] \[\+|\-\]*hh*:*mm*.  
  
 Die Sekundenbruchteile der zurückgegebenen Zeichenfolge werden bis zur angegebenen Genauigkeit mit Nullen aufgefüllt. So wird beispielsweise ein **datetimeoffset\(6\)** mit einem Wert von "2010\-03\-10 12:34:56.78 \-08:00" von DateTimeOffset.toString als "2010\-03\-10 12:34:56.780000 \-08:00" formatiert.  
  
## Siehe auch  
 [DateTimeOffset-Klasse](../content/DateTimeOffset-Class.md)   
 [DateTimeOffset-Elemente](../content/DateTimeOffset-Members.md)  
  
  