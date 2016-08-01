---
title: "getAsciiStream-Methode (SQLServerClob)"
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
  - SQLServerClob.getAsciiStream
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 134abe5e-5add-4d27-b333-b4b0f4d94c31
caps.latest.revision: 9
caps.handback.revision: 8
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
# getAsciiStream-Methode (SQLServerClob)
    
## getAsciiStream\-Methode \(SQLServerClob\)  
 Materialisiert das CLOB als ASCII\-Datenstrom.  
  
## Syntax  
  
```  
  
public java.io.InputStream getAsciiStream()  
```  
  
## Rückgabewert  
 Ein Eingabedatenstrom mit den CLOB\-Daten.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getAsciiStream\-Methode wird von der getAsciiStream\-Methode in der java.sql.Clob\-Schnittstelle angegeben.  
  
 Gibt immer einen Bytestrom zurück und geht davon aus, dass die Daten im CLOB das ASCII\-Format aufweisen, da nicht bekannt ist, ob es sich um Unicode oder eine andere Multibyte\-Codeseite handelt.  
  
## Siehe auch  
 [SQLServerClob-Methoden](../content/SQLServerClob-Methods.md)   
 [SQLServerClob-Elemente](../content/SQLServerClob-Members.md)   
 [SQLServerClob-Klasse](../content/SQLServerClob-Class.md)  
  
  