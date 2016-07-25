---
title: "getParameterTypeName-Methode (SQLServerParameterMetaData)"
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
  - SQLServerParameterMetaData.getParameterTypeName
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: ebe7ff0f-3cc0-408e-9503-4ca754c9c37f
caps.latest.revision: 8
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
# getParameterTypeName-Methode (SQLServerParameterMetaData)
    
## getParameterTypeName\-Methode \(SQLServerParameterMetaData\)  
 Ruft den datenbankspezifischen Typnamen des angegebenen Parameters ab.  
  
## Syntax  
  
```  
  
public java.lang.String getParameterTypeName(int param)  
```  
  
#### Parameter  
 *param*  
  
 Ein Wert vom Typ **int** zum Angeben des Parameterindexes.  
  
## Rückgabewert  
 Ein **String** mit dem Typnamen.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getParameterTypeName\-Methode wird von der getParameterTypeName\-Methode in der java.sql.ParameterMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerParameterMetaData-Methoden](../content/SQLServerParameterMetaData-Methods.md)   
 [SQLServerParameterMetaData-Elemente](../content/SQLServerParameterMetaData-Members.md)   
 [SQLServerParameterMetaData-Klasse](../content/SQLServerParameterMetaData-Class.md)  
  
  