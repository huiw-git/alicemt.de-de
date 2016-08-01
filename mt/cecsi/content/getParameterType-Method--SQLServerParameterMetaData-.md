---
title: "getParameterType-Methode (SQLServerParameterMetaData)"
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
  - SQLServerParameterMetaData.getParameterType
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 638aca05-63e4-4d73-a9c8-e0442f775720
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
# getParameterType-Methode (SQLServerParameterMetaData)
    
## getParameterType\-Methode \(SQLServerParameterMetaData\)  
 Ruft den SQL\-Typ des angegebenen Parameters ab.  
  
## Syntax  
  
```  
  
public int getParameterType(int param)  
```  
  
#### Parameter  
 *param*  
  
 Ein Wert vom Typ **int** zum Angeben des Parameterindexes.  
  
## Rückgabewert  
 Ein Objekt vom Typ **int** , das den im java.sql.Types\-Element definierten JDBC\-Typcode angibt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getParameterType\-Methode wird von der getParameterType\-Methode in der java.sql.ParameterMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerParameterMetaData-Methoden](../content/SQLServerParameterMetaData-Methods.md)   
 [SQLServerParameterMetaData-Elemente](../content/SQLServerParameterMetaData-Members.md)   
 [SQLServerParameterMetaData-Klasse](../content/SQLServerParameterMetaData-Class.md)  
  
  