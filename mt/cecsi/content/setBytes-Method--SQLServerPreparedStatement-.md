---
title: "setBytes-Methode (ISQLServerPreparedStatement)"
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
  - SQLServerPreparedStatement.setBytes
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 52e99ef9-b786-4a14-bfc5-4162e46aafbb
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
# setBytes-Methode (ISQLServerPreparedStatement)
    
## setBytes\-Methode \(ISQLServerPreparedStatement\)  
 Legt den angegebenen Parameter auf das angegebene Bytearray fest.  
  
## Syntax  
  
```  
  
public final void setBytes(int n,  
                           byte[] x)  
```  
  
#### Parameter  
 *n*  
  
 Ein Wert vom Typ **int** zum Angeben der Parameternummer.  
  
 *x*  
  
 Ein Array von Bytes.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Die setBytes\-Methode wird von der setBytes\-Methode in der java.sql.PreparedStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)   
 [SQLServerPreparedStatement-Klasse](../content/SQLServerPreparedStatement-Class.md)  
  
  