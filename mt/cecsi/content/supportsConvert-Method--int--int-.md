---
title: "supportsConvert-Methode (int, int)"
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
  - SQLServerDatabaseMetaData.supportsConvert (int, int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 54741cfd-32ac-46c5-8b09-fd60fd8833d7
caps.latest.revision: 6
caps.handback.revision: 6
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
# supportsConvert-Methode (int, int)
    
## supportsConvert\-Methode \(int, int\)  
 Ruft ab, ob von dieser Datenbank die CONVERT\-Funktion für zwei angegebene SQL\-Typen unterstützt wird.  
  
## Syntax  
  
```  
  
public boolean supportsConvert(int fromType,  
                               int toType)  
```  
  
#### Parameter  
 *fromType*  
  
 Der JDBC\-Ausgangstyp der Konvertierung.  
  
 *toType*  
  
 Der JDBC\-Zieltyp der Konvertierung.  
  
## Rückgabewert  
 **true**, sofern unterstützt. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese supportsConvert\-Methode wird von der supportsConvert\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
## Siehe auch  
 [supportsConvert-Methode &#40;SQLServerDatabaseMetaData&#41;](../content/supportsConvert-Method--SQLServerDatabaseMetaData-.md)   
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  