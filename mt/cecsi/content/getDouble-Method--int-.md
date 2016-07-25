---
title: "getDouble-Methode (int)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLServerCallableStatement.getDouble (int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: c0ed63bb-5ebe-4155-9f91-8fbfeac9c3b2
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
# getDouble-Methode (int)
    
## getDouble\-Methode \(int\)  
 Ruft den Wert des angegebenen Parameters unter Berücksichtigung des Parameterindexes als **double** \-Objekt in der Programmiersprache Java ab.  
  
## Syntax  
  
```  
  
public double getDouble(int index)  
```  
  
#### Parameter  
 *index*  
  
 Ein Wert vom Typ **int** zum Angeben des Parameterindexes.  
  
## Rückgabewert  
 Ein Wert vom Typ **double** .  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getDouble\-Methode wird von der getDouble\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
 Von dieser Methode werden alle zahlenbasierten Datentypen mit der Java\-Genauigkeit vom Typ **double** zurückgegeben.  
  
## Siehe auch  
 [getDouble-Methode &#40;SQLServerCallableStatement&#41;](../content/getDouble-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  