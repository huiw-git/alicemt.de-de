---
title: "isNullable-Methode (SQLServerParameterMetaData)"
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
  - SQLServerParameterMetaData.sNullable
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: d7e07cff-6fc4-4c9c-8e8f-838c77734bc5
caps.latest.revision: 7
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
# isNullable-Methode (SQLServerParameterMetaData)
    
## isNullable\-Methode \(SQLServerParameterMetaData\)  
 Ruft ab, ob im angegebenen Parameter NULL\-Werte zulässig sind.  
  
## Syntax  
  
```  
  
public int isNullable(int param)  
```  
  
#### Parameter  
 *param*  
  
 Ein Wert vom Typ **int** zum Angeben des Parameterindexes.  
  
## Rückgabewert  
 Ein Wert vom Typ **int** zum Angeben der NULL\-Zulässigkeit des angegebenen Parameters. Mögliche Werte:  
  
 ParameterMetaData.parameterNoNulls  
  
 ParameterMetaData.parameterNullable  
  
 ParameterMetaData.parameterNullabilityUnknown  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese isNullable\-Methode wird von der isNullable\-Methode in der java.sql.ParameterMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerParameterMetaData-Methoden](../content/SQLServerParameterMetaData-Methods.md)   
 [SQLServerParameterMetaData-Elemente](../content/SQLServerParameterMetaData-Members.md)   
 [SQLServerParameterMetaData-Klasse](../content/SQLServerParameterMetaData-Class.md)  
  
  