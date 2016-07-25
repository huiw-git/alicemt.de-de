---
title: "updateRow-Methode (ISQLServerResultSet)"
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
  - MSQLServerResultSet.updateRow
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: cfced0ca-a281-40dc-8d2f-370d5f0bf12b
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
# updateRow-Methode (ISQLServerResultSet)
    
## updateRow\-Methode \(ISQLServerResultSet\)  
 Aktualisiert die zugrunde liegende Datenbank mit dem neuen Inhalt der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts.  
  
## Syntax  
  
```  
  
public void updateRow()  
```  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese updateRow\-Methode wird von der updateRow\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Diese Methode kann nicht aufgerufen werden, wenn sich der Cursor in der Einfügezeile befindet.  
  
 Wird diese Methode aufgerufen, obwohl keine Spaltenwerte geändert wurden, wird eine Ausnahme ausgelöst.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  