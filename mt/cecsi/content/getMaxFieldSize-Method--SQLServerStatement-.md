---
title: "getMaxFieldSize-Methode (ISQLServerStatement)"
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
  - SQLServerStatement.getMaxFieldSize
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: ed7bbcb8-660b-4e9b-8241-e216c42826f9
caps.latest.revision: 8
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
# getMaxFieldSize-Methode (ISQLServerStatement)
    
## getMaxFieldSize\-Methode \(ISQLServerStatement\)  
 Ruft die maximale Anzahl von Bytes ab, die für Zeichen\- und Binärspaltenwerte in einem [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt zurückgegeben werden können, das von diesem [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt erstellt wird.  
  
## Syntax  
  
```  
  
public final int getMaxFieldSize()  
```  
  
## Rückgabewert  
 Ein Element vom Typ **int** , das die maximale Anzahl von Bytes anzeigt, die eine Spalte enthalten kann. Oder es wird "0" angezeigt, wenn keine Grenze vorhanden ist.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getMaxFieldSize\-Methode wird von der getMaxFieldSize\-Methode in der java.sql.Statement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [ISQLServerStatement-Methoden](../content/SQLServerStatement-Methods.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  