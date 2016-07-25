---
title: "acceptsURL-Methode (SQLServerDriver)"
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
  - SQLServerDriver.acceptsURL
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: fc744566-7191-4b15-9f76-b4b8087fb14a
caps.latest.revision: 7
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
# acceptsURL-Methode (SQLServerDriver)
    
## acceptsURL\-Methode \(SQLServerDriver\)  
 Überprüft, ob die angegebene URL gültig ist.  
  
## Syntax  
  
```  
  
public boolean acceptsURL(java.lang.String url)  
```  
  
#### Parameter  
 *url*  
  
 Ein **String** \-Wert mit der URL, die zum Herstellen einer Verbindung mit der Datenbank verwendet wird.  
  
## Rückgabewert  
 **true**, wenn die angegebene URL gültig ist. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese acceptsURL\-Methode wird von der acceptsURL\-Methode in der java.sql.Driver\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDriver-Methoden](../content/SQLServerDriver-Methods.md)   
 [SQLServerDriver-Elemente](../content/SQLServerDriver-Members.md)   
 [SQLServerDriver-Klasse](../content/SQLServerDriver-Class.md)  
  
  