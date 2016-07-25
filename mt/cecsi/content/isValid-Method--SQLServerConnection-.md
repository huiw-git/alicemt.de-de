---
title: "isValid-Methode (SQLServerConnection)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3b0a8bbf-9369-4456-9ab8-1434ccacdd7e
caps.latest.revision: 15
caps.handback.revision: 15
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
# isValid-Methode (SQLServerConnection)
  Gibt an, ob dieses [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt noch geöffnet und gültig ist.  
  
## Syntax  
  
```  
  
public boolean isValid(int timeout)  
```  
  
#### Parameter  
 *timeout*  
  
 Ein Wert vom Typ **int** zum Angeben der Anzahl von Sekunden, die auf die Überprüfung der Verbindung gewartet wird.  
  
## Rückgabewert  
 **true**, wenn die Verbindung gültig ist. **false**, wenn die Verbindung nicht gültig ist oder die Gültigkeit der Verbindung nicht vor Ablauf des Timeouts ermittelt werden kann.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese isValid\-Methode wird von der isValid\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  