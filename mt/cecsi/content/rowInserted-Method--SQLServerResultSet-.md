---
title: "rowInserted-Methode (ISQLServerResultSet)"
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
  - SQLServerResultSet.rowInserted
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: e7c10372-0be8-4baa-87f7-ed6b66003357
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
# rowInserted-Methode (ISQLServerResultSet)
    
## rowInserted\-Methode \(ISQLServerResultSet\)  
 Ruft ab, ob in der aktuellen Zeile eine Einfügung vorgenommen wurde.  
  
## Syntax  
  
```  
  
public boolean rowInserted()  
```  
  
## Rückgabewert  
 **true**, wenn in der Zeile eine Einfügung vorgenommen wurde und Einfügungen erkannt wurden. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese rowUpdated\-Methode wird von der rowUpdated\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Der zurückgegebene Wert ist davon abhängig, ob vom [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt sichtbare Einfügungen ermittelt werden können.  
  
> [!NOTE]  
>  Von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] werden für Cursortypen keine eingefügten Zeilen ermittelt.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  