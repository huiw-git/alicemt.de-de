---
title: "rowUpdated-Methode (ISQLServerResultSet)"
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
  - SQLServerResultSet.rowUpdated
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 29303550-294e-4d43-b892-312b42e21271
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
# rowUpdated-Methode (ISQLServerResultSet)
    
## rowUpdated\-Methode \(ISQLServerResultSet\)  
 Ruft ab, ob die aktuelle Zeile aktualisiert wurde.  
  
## Syntax  
  
```  
  
public boolean rowUpdated()  
```  
  
## Rückgabewert  
 **true**, wenn die Zeile sichtbar vom Besitzer oder einem anderen Benutzer aktualisiert wurde und Updates ermittelt werden. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese rowUpdated\-Methode wird von der rowUpdated\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Der zurückgegebene Wert ist davon abhängig, ob vom Resultset Updates ermittelt werden.  
  
> [!NOTE]  
>  Von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] werden für Cursortypen keine aktualisierten Zeilen ermittelt.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  