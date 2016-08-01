---
title: "getBlob-Methode (java.lang.String)"
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
  - SQLServerCallableStatement.getBlob (java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 3fe74b50-9ccd-4973-a93a-6da2c20a4154
caps.latest.revision: 9
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
# getBlob-Methode (java.lang.String)
    
## getBlob\-Methode \(java.lang.String\)  
 Ruft den Wert des angegebenen JDBC\-BLOB\-Parameters unter Berücksichtigung des Parameternamens und unter Verwendung des angegebenen Blob\-Objekts als Objekt in der Programmiersprache Java ab.  
  
## Syntax  
  
```  
  
public java.sql.Blob getBlob(java.lang.String sCol)  
```  
  
#### Parameter  
 *sCol*  
  
 Ein **String** mit dem Parameternamen.  
  
## Rückgabewert  
 Ein Blob\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getBlob\-Methode wird von der getBlob\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [getBlob-Methode &#40;SQLServerCallableStatement&#41;](../content/getBlob-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  