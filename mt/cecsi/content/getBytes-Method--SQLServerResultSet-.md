---
title: "getBytes-Methode (SQLServerResultSet)"
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
  - SQLServerResultSet.getBytes
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: d16a0aea-6144-4fcb-bcbc-5d7daa36d327
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
# getBytes-Methode (SQLServerResultSet)
  Ruft den Wert der angegebenen Spalte in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Array vom Typ **byte** in der Programmiersprache Java ab.  
  
## Überladungsliste  
  
|Name|Beschreibung|  
|----------|------------------|  
|[getBytes \(int\)](../content/getBytes-Method--int---SQLServerResultSet-.md)|Ruft den Wert des angegebenen Spaltenindexes in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Array vom Typ **byte** in der Programmiersprache Java ab.|  
|[getBytes \(java.lang.String\)](../content/getBytes-Method--java.lang.String---SQLServerResultSet-.md)|Ruft den Wert des angegebenen Spaltennamens in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Array vom Typ **byte** in der Programmiersprache Java ab.|  
  
## Hinweise  
 In einer früheren Version von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] konnten Sie mithilfe von "SQLServerResultSet.getBytes" Werte zwischen Bytearrays und dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentyp **date**, **time**, **datetime2** oder **datetimeoffset** konvertieren. Nun wird durch Verwendung der Methode mit diesen Datentypen eine Ausnahme ausgelöst, die angibt, dass die Konvertierung nicht unterstützt wird.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  