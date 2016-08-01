---
title: "getMoreResults-Methode (int)"
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
  - SQLServerStatement.getMoreResults (int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 6419e5a8-8b3a-4d5b-8226-95865c52c723
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
# getMoreResults-Methode (int)
    
## getMoreResults\-Methode \(int\)  
 Wechselt zum nächsten Schritt des [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekts und behandelt alle derzeit geöffneten Resultsetobjekte gemäß den Anweisungen, die durch den angegebenen Modus vorgegeben werden.  
  
## Syntax  
  
```  
  
public final boolean getMoreResults(int mode)  
```  
  
#### Parameter  
 *mode*  
  
 Ein Wert vom Typ **int** zur Angabe der Behandlung von derzeit geöffneten Resultsetobjekten. Dabei muss es sich um eine der folgenden Konstanten handeln:  
  
 CLOSE\_CURRENT\_RESULT  
  
 KEEP\_CURRENT\_RESULT \(vom JDBC\-Treiber nicht unterstützt\)  
  
 CLOSE\_ALL\_RESULTS  
  
## Rückgabewert  
 **true**, wenn es sich beim zurückgegebenen Ergebnis um ein Resultset handelt. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getMoreResults\-Methode wird von der getMoreResults\-Methode in der java.sql.Statement\-Schnittstelle angegeben.  
  
 Falls die getMoreResults\-Methode aufgerufen wird, bevor die Ergebnisse abgerufen werden, entspricht das Verhalten dem *mode*\-Argument, und das nächste Ergebnis wird aufgerufen.  
  
> [!NOTE]  
>  Die Verwendung der Konstante KEEP\_CURRENT\_RESULT wird vom JDBC\-Treiber nicht unterstützt. Bei ihrer Verwendung wird eine Ausnahme ausgelöst.  
  
## Siehe auch  
 [getMoreResults-Methode &#40;ISQLServerStatement&#41;](../content/getMoreResults-Method--SQLServerStatement-.md)   
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  