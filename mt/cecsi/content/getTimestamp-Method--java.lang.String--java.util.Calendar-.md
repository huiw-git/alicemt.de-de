---
title: "getTimestamp-Methode (java.lang.String, java.util.Calendar)"
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
  - SQLServerCallableStatement.getTimestamp (java.lang.String,java.util.Calendar)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 770668d9-2e52-4ff0-be2f-ebf78fd41644
caps.latest.revision: 10
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
# getTimestamp-Methode (java.lang.String, java.util.Calendar)
    
## getTimestamp\-Methode \(java.lang.String, java.util.Calendar\)  
 Ruft den Wert des angegebenen Parameters als java.sql.Timestamp\-Objekt in der Programmiersprache Java ab \(unter Berücksichtigung des vorhandenen Parameternamens\), indem ein Calendar\-Objekt verwendet wird.  
  
## Syntax  
  
```  
  
public java.sql.Timestamp getTimestamp(java.lang.String name,  
                                       java.util.Calendar cal)  
```  
  
#### Parameter  
 *name*  
  
 Ein **String** mit dem Parameternamen.  
  
 *cal*  
  
 Ein Calendar\-Objekt.  
  
## Rückgabewert  
 Ein Timestamp\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getTimestamp\-Methode wird von der getTimestamp\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
 Von dieser Methode werden nur Werte aus [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]**datetime**\- und **smalldatetime** \-Spalten zurückgegeben.  
  
## Siehe auch  
 [getTimestamp-Methode &#40;SQLServerCallableStatement&#41;](../content/getTimestamp-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  