---
title: "rowDeleted-Methode (ISQLServerResultSet)"
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
  - SQLServerResultSet.rowDeleted
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 9c6db315-e614-4604-b020-41af6a214cc1
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
# rowDeleted-Methode (ISQLServerResultSet)
    
## rowDeleted\-Methode \(ISQLServerResultSet\)  
 Ruft ab, ob eine Zeile gelöscht wurde.  
  
## Syntax  
  
```  
  
public boolean rowDeleted()  
```  
  
## Rückgabewert  
 **true**, wenn eine Zeile gelöscht wurde und Löschungen ermittelt wurden. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese rowDeleted\-Methode wird von der rowDeleted\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Eine gelöschte Zeile hinterlässt in einem Resultset ggf. eine sichtbare Lücke. Diese Methode kann verwendet werden, um Löcher in einem Resultset zu ermitteln. Der zurückgegebene Wert ist davon abhängig, ob vom [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt Löschungen ermittelt werden können.  
  
> [!NOTE]  
>  Gelöschte Zeilen werden von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] zwar für alle aktualisierbaren Cursortypen erkannt, die Erkennung für Vorwärtscursor und dynamische Cursor ist jedoch kurzlebig.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  