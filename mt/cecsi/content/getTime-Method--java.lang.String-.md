---
title: "getTime-Methode (java.lang.String)"
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
  - SQLServerCallableStatement.getTime (java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: ca0a3b29-30d1-4d20-bc8d-d3d9ed19ff50
caps.latest.revision: 11
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
# getTime-Methode (java.lang.String)
    
## getTime\-Methode \(java.lang.String\)  
 Ruft den Wert des angegebenen Parameters unter Berücksichtigung des Parameternamens als java.sql.Time\-Objekt in der Programmiersprache Java ab.  
  
## Syntax  
  
```  
  
public java.sql.Time getTime(java.lang.String sCol)  
```  
  
#### Parameter  
 *sCol*  
  
 Ein **String** mit dem Parameternamen.  
  
## Rückgabewert  
 Ein Time\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getTime\-Methode wird von der getTime\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
 Aus dem Diagramm mit dem Titel "Konvertierungen für Abrufmethoden" in [Grundlegendes zu Datentypkonvertierungen](../content/Understanding-Data-Type-Conversions.md) ist ersichtlich, welche [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentypen mit dieser Methode abgerufen werden können.  
  
## Siehe auch  
 [getTime-Methode &#40;SQLServerCallableStatement&#41;](../content/getTime-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  