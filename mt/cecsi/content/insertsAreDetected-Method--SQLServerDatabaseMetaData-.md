---
title: "insertsAreDetected-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.insertsAreDetected
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: f296cc42-9d26-48c3-a360-bcf51c31f7fb
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
# insertsAreDetected-Methode (SQLServerDatabaseMetaData)
    
## insertsAreDetected\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft ab, ob das Einfügen einer sichtbaren Zeile durch Aufrufen der [rowInserted](../content/rowInserted-Method--SQLServerResultSet-.md)\-Methode der [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Klasse ermittelt werden kann.  
  
## Syntax  
  
```  
  
public boolean insertsAreDetected(int type)  
```  
  
#### Parameter  
 *type*  
  
 Eine Ganzzahl zum Angeben des Resultsettyps, bei dem es sich gemäß Definition in "java.sql.ResultSet" oder "SQLServerResultSet" um einen der folgenden Werte handeln kann:  
  
### java.sql.ResultSet\-Typen  
 TYPE\_FORWARD\_ONLY  
  
 TYPE\_SCROLL\_SENSITIVE  
  
 TYPE\_SCROLL\_INSENSITIVE  
  
### SQLServerResultSet\-Typen  
 TYPE\_SS\_SCROLL\_STATIC  
  
 TYPE\_SS\_SCROLL\_KEYSET  
  
 TYPE\_SS\_DIRECT\_FORWARD\_ONLY  
  
 TYPE\_SS\_SERVER\_CURSOR\_FORWARD\_ONLY  
  
 TYPE\_SS\_SCROLL\_DYNAMIC  
  
## Rückgabewert  
 **true**, wenn die Zeileneinfügung ermittelt werden kann. Andernfalls wird **false** verwendet.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese insertsAreDetected\-Methode wird von der insertsAreDetected\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
> [!NOTE]  
>  Von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] werden für Cursortypen keine eingefügten Zeilen ermittelt.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  