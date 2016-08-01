---
title: "getBytes-Methode (SQLServerCallableStatement)"
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
  - SQLServerCallableStatement.getBytes
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: b6e88cea-54b3-4d18-a9af-db54abf19f45
caps.latest.revision: 13
caps.handback.revision: 12
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
# getBytes-Methode (SQLServerCallableStatement)
  Ruft den Wert des angegebenen Parameters als Bytearray ab.  
  
## Überladungsliste  
  
|Name|Beschreibung|  
|----------|------------------|  
|[getBytes \(int\)](../content/getBytes-Method--int-.md)|Ruft den Wert des angegebenen Parameters unter Berücksichtigung des Parameterindexes als ein Array von Bytewerten ab.|  
|[getBytes \(java.lang.String\)](../content/getBytes-Method--java.lang.String-.md)|Ruft den Wert des angegebenen Parameters unter Berücksichtigung des Parameternamens als ein Array von Bytewerten ab.|  
  
## Hinweise  
 In einer früheren Version von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] konnten Sie mithilfe von "SQLServerCallableStatement.getBytes" Werte zwischen Bytearrays und dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentyp **date**, **time**, **datetime2** oder **datetimeoffset** konvertieren. Nun wird durch Verwendung der Methode mit diesen Datentypen eine Ausnahme ausgelöst, die angibt, dass die Konvertierung nicht unterstützt wird.  
  
## Siehe auch  
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  