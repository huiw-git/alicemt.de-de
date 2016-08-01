---
title: "createClob-Methode (SQLServerConnection)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 58b0865a-1cde-4046-9761-51e471294023
caps.latest.revision: 16
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
# createClob-Methode (SQLServerConnection)
  Erstellt ein Clob\-Objekt ohne Daten.  
  
## Syntax  
  
```  
  
public java.sql.Clob createClob()  
```  
  
## Rückgabewert  
 Ein Clob\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese createClob\-Methode wird von der createClob\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
 Dank dieser Methode wird [SQLServerClob-Konstruktor &#40;SQLServerConnection, java.lang.String&#41;](../content/SQLServerClob-Constructor--SQLServerConnection--java.lang.String-.md) nicht mehr benötigt.  
  
## Siehe auch  
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  