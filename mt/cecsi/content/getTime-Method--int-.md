---
title: "getTime-Methode (int)"
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
  - SQLServerCallableStatement.getTime (int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 6c13dea2-511f-48dc-b3db-2d3b72ccc9de
caps.latest.revision: 12
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
# getTime-Methode (int)
    
## getTime\-Methode \(int\)  
 Ruft den Wert des angegebenen Parameters unter Berücksichtigung des Parameterindexes als java.sql.Time\-Objekt in der Programmiersprache Java ab.  
  
## Syntax  
  
```  
  
public java.sql.Time getTime(int index)  
```  
  
#### Parameter  
 *index*  
  
 Ein Wert vom Typ **int** zum Angeben des Parameterindexes.  
  
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
  
  