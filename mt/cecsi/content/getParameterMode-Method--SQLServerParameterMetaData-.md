---
title: "getParameterMode-Methode (SQLServerParameterMetaData)"
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
  - SQLServerParameterMetaData.getParameterMode
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: d93c9b70-18c2-44bb-a6de-70a7e940d806
caps.latest.revision: 8
caps.handback.revision: 8
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
# getParameterMode-Methode (SQLServerParameterMetaData)
    
## getParameterMode\-Methode \(SQLServerParameterMetaData\)  
 Ruft den Modus des angegebenen Parameters ab.  
  
## Syntax  
  
```  
  
public int getParameterMode(int param)  
```  
  
#### Parameter  
 *param*  
  
 Ein Wert vom Typ **int** zum Angeben des Parameterindexes.  
  
## Rückgabewert  
 Ein Wert vom Typ **int** zum Angeben des Modus des angegebenen Parameters. Mögliche Werte:  
  
 ParameterMetaData.parameterModeIn  
  
 ParameterMetaData.parameterModeInOut  
  
 ParameterMetaData.parameterModeOut  
  
 ParameterMetaData.parameterModeUnknown  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getParameterMode\-Methode wird von der getParameterMode\-Methode in der java.sql.ParameterMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerParameterMetaData-Methoden](../content/SQLServerParameterMetaData-Methods.md)   
 [SQLServerParameterMetaData-Elemente](../content/SQLServerParameterMetaData-Members.md)   
 [SQLServerParameterMetaData-Klasse](../content/SQLServerParameterMetaData-Class.md)  
  
  