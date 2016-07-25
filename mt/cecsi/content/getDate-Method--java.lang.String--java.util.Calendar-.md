---
title: "getDate-Methode (java.lang.String, java.util.Calendar)"
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
  - SQLServerCallableStatement.getDate (java.util.Calendar)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 6d0deaf2-6f12-4a6e-b537-a51fa3478059
caps.latest.revision: 10
caps.handback.revision: 9
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
# getDate-Methode (java.lang.String, java.util.Calendar)
    
## getDate\-Methode \(java.lang.String, java.util.Calendar\)  
 Ruft den Wert des angegebenen Parameters unter Berücksichtigung des Parameternamens und Calendar\-Objekts als java.sql.Date\-Objekt in der Programmiersprache Java ab.  
  
## Syntax  
  
```  
  
public java.sql.Date getDate(java.lang.String sCol,  
                             java.util.Calendar cal)  
```  
  
#### Parameter  
 *sCol*  
  
 Ein **String** mit dem Parameternamen.  
  
 *cal*  
  
 Ein Calendar\-Objekt.  
  
## Rückgabewert  
 Ein Date\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getDate\-Methode wird von der getDate\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
 Von dieser Methode wird ein gültiger Datumsteil eines datetime\- oder smalldatetime\-Datentyps von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] zurückgegeben. Der Zeitteil ist dabei auf die Java\-Zeitbasis \(00:00, Mitternacht\) festgelegt.  
  
## Siehe auch  
 [getDate-Methode &#40;SQLServerCallableStatement&#41;](../content/getDate-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  