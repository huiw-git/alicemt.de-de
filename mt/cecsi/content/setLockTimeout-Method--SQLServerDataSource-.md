---
title: "setLockTimeout-Methode (SQLServerDataSource)"
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
  - SQLServerDataSource.setLockTimeout
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 10dca5aa-1851-4326-9ae9-7a8430d12d11
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
# setLockTimeout-Methode (SQLServerDataSource)
    
## setLockTimeout\-Methode \(SQLServerDataSource\)  
 Legt einen Wert vom Typ **int** fest, mit dem angegeben wird, wie lange von der Datenbank bis zum Melden eines Sperrtimeouts gewartet wird \(in Millisekunden\).  
  
## Syntax  
  
```  
  
public void setLockTimeout(int lockTimeout)  
```  
  
#### Parameter  
 *lockTimeout*  
  
 Ein Wert vom Typ **int** , der die Wartedauer in Millisekunden enthält.  
  
## Hinweise  
 Das Sperrtimeout ist die Anzahl von Millisekunden bis zur Meldung eines Sperrtimeouts durch die Datenbank. Der Standardwert "\-1" bedeutet, dass unbegrenzt gewartet wird. Wird dieser Wert angegeben, wird er als Standardwert für alle Anweisungen der Verbindung verwendet.  
  
> [!NOTE]  
>  Bei dem Wert "0" wird nicht gewartet. Ist die lockTimeout\-Eigenschaft nicht festgelegt, wird von der [getLockTimeout](../content/getLockTimeout-Method--SQLServerDataSource-.md)\-Methode der Standardwert "\-1" zurückgegeben.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  