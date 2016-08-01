---
title: "getParameterClassName-Methode (SQLServerParameterMetaData)"
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
  - SQLServerParameterMetaData.getParameterClassName
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 545634d8-f06b-429a-9293-0087d758f359
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
# getParameterClassName-Methode (SQLServerParameterMetaData)
    
## getParameterClassName\-Methode \(SQLServerParameterMetaData\)  
 Ruft den vollqualifizierten Namen der Java\-Klasse ab, deren Instanzen an die [setObject](../content/setObject-Method--SQLServerPreparedStatement-.md)\-Methode der [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\-Klasse übergeben werden sollen.  
  
## Syntax  
  
```  
  
public java.lang.String getParameterClassName(int param)  
```  
  
#### Parameter  
 *param*  
  
 Ein Wert vom Typ **int** zum Angeben des Parameterindexes.  
  
## Rückgabewert  
 Ein **String** mit dem vollqualifizierten Namen der Klasse.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getParameterClassName\-Methode wird von der getParameterClassName\-Methode in der java.sql.ParameterMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerParameterMetaData-Methoden](../content/SQLServerParameterMetaData-Methods.md)   
 [SQLServerParameterMetaData-Elemente](../content/SQLServerParameterMetaData-Members.md)   
 [SQLServerParameterMetaData-Klasse](../content/SQLServerParameterMetaData-Class.md)  
  
  