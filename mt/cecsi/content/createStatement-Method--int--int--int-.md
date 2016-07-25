---
title: "createStatement-Methode (int, int, int)"
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
  - SQLServerConnection.createStatement (int, int, int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 2e4fa385-8f61-4394-8f75-3e839930a57d
caps.latest.revision: 9
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
# createStatement-Methode (int, int, int)
    
## createStatement\-Methode \(int, int, int\)  
 Erstellt ein [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt, mit dem [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekte mit dem angegebenen Typ sowie der Parallelität und Haltbarkeit generiert werden.  
  
## Syntax  
  
```  
  
public java.sql.Statement createStatement(int nType,  
                                          int nConcur,  
                                          int nHold)  
```  
  
#### Parameter  
 *resultSetType*  
  
 Der Wert vom Typ **int** , der den Resultsettyp darstellt.  
  
 *nConcur*  
  
 Der Wert vom Typ **int** , der den Resultset\-Parallelitätstyp darstellt.  
  
 *nHold*  
  
 Der Wert vom Typ **int** , der die Haltbarkeit darstellt.  
  
## Rückgabewert  
 Das Statement\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese createStatement\-Methode wird von der createStatement\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
## Siehe auch  
 [createStatement-Methode &#40;ISQLServerConnection&#41;](../content/createStatement-Method--SQLServerConnection-.md)   
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  