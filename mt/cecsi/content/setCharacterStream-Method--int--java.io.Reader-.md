---
title: "setCharacterStream-Methode (int, java.io.Reader)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b8d4e1f7-14fc-4590-af98-1eda30d2ca6d
caps.latest.revision: 20
caps.handback.revision: 20
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
# setCharacterStream-Methode (int, java.io.Reader)
    
## setCharacterStream\-Methode \(int, java.io.Reader\)  
 Legt den angegebenen Parameter auf das angegebene java.io.Reader\-Objekt fest.  
  
> [!NOTE]  
>  Diese Funktion wird mit Version 2.0 von [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver eingeführt.  
  
## Syntax  
  
```  
  
public final void setCharacterStream(int parameterIndex,  
                              java.io.Reader reader)  
```  
  
#### Parameter  
 *parameterIndex*  
  
 Ein Wert vom Typ **int** zum Angeben der Parameternummer.  
  
 *reader*  
  
 Das java.io.Reader\-Objekt, das die Unicode\-Daten enthält.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setCharacterStream\-Methode wird von der setCharacterStream\-Methode in der java.sql.PreparedStatement\-Schnittstelle angegeben.  
  
## Siehe auch  
 [setCharacterStream-Methode &#40;ISQLServerPreparedStatement&#41;](../content/setCharacterStream-Method--SQLServerPreparedStatement-.md)   
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)  
  
  