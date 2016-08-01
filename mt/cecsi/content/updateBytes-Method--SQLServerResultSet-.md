---
title: "updateBytes-Methode (SQLServerResultSet)"
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
  - SQLServerResultSet.updateBytes
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 3050c836-fbb3-4475-99e5-05637a48a932
caps.latest.revision: 12
caps.handback.revision: 11
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
# updateBytes-Methode (SQLServerResultSet)
  Aktualisiert die angegebene Spalte mit einem Array von **byte**\-Werten.  
  
## Überladungsliste  
  
|Name|Beschreibung|  
|----------|------------------|  
|[updateBytes \(int, byte&#91;&#93;\)](../content/updateBytes-Method--int--byte-.md)|Aktualisiert die angegebene Spalte mit einem Array von **byte**\-Werten unter Berücksichtigung des Spaltenindexes.|  
|[updateBytes \(java.lang.String, byte&#91;&#93;\)](../content/updateBytes-Method--java.lang.String--byte-.md)|Aktualisiert die angegebene Spalte mit einem Array von **byte**\-Werten unter Berücksichtigung des Spaltennamens.|  
  
## Hinweise  
 In einer früheren Version von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] konnten Sie mithilfe von "SQLServerResultSet.updateBytes" Werte zwischen Bytearrays und dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentyp **date**, **time**, **datetime2** oder **datetimeoffset** konvertieren. Nun wird durch Verwendung der Methode mit diesen Datentypen eine Ausnahme ausgelöst, die angibt, dass die Konvertierung nicht unterstützt wird.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  