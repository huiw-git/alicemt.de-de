---
title: "getLockTimeout-Methode (SQLServerDataSource)"
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
  - SQLServerDataSource.getLockTimeout
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 676094e9-ec18-4524-9b21-1f9c5b16dd52
caps.latest.revision: 11
caps.handback.revision: 10
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
# getLockTimeout-Methode (SQLServerDataSource)
    
## getLockTimeout\-Methode \(SQLServerDataSource\)  
 Gibt einen Wert vom Typ **int** zurück, mit dem angegeben wird, wie lange von der Datenbank bis zum Melden eines Sperrtimeouts gewartet wird \(in Millisekunden\).  
  
## Syntax  
  
```  
  
public int getLockTimeout()  
```  
  
## Rückgabewert  
 Ein Wert vom Typ **int** mit der Anzahl von Millisekunden, die die Datenbank warten wird.  
  
## Hinweise  
 Das Sperrtimeout ist die Anzahl von Millisekunden bis zur Meldung eines Sperrtimeouts durch die Datenbank. Der Standardwert "\-1" bedeutet, dass unbegrenzt gewartet wird. Wird dieser Wert angegeben, wird er als Standardwert für alle Anweisungen der Verbindung verwendet.  
  
> [!NOTE]  
>  Bei dem Wert "0" wird nicht gewartet. Ist die lockTimeout\-Eigenschaft nicht festgelegt, wird von der getLockTimeout\-Methode der Standardwert "\-1" zurückgegeben.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  