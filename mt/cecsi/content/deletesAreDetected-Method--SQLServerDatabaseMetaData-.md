---
title: "deletesAreDetected-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.deletesAreDetected
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 73f3d994-bbd7-43d2-8b64-50057e278983
caps.latest.revision: 16
caps.handback.revision: 15
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
# deletesAreDetected-Methode (SQLServerDatabaseMetaData)
  Ruft ab, ob das Löschen einer sichtbaren Zeile durch Aufrufen der [rowDeleted](../content/rowDeleted-Method--SQLServerResultSet-.md)\-Methode der [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Klasse ermittelt werden kann.  
  
## Syntax  
  
```  
  
public boolean deletesAreDetected(int type)  
```  
  
#### Parameter  
 *type*  
  
 Ein Wert vom Typ **int** zum Angeben des Resultsettyps, bei dem es sich gemäß Definition in "java.sql.ResultSet" oder SQLServerResultSet um einen der folgenden Werte handeln kann:  
  
## java.sql.ResultSet\-Typen  
 TYPE\_FORWARD\_ONLY  
  
 TYPE\_SCROLL\_SENSITIVE  
  
 TYPE\_SCROLL\_INSENSITIVE  
  
## SQLServerResultSet\-Typen  
 TYPE\_SS\_SCROLL\_STATIC  
  
 TYPE\_SS\_SCROLL\_KEYSET  
  
 TYPE\_SS\_DIRECT\_FORWARD\_ONLY  
  
 TYPE\_SS\_SERVER\_CURSOR\_FORWARD\_ONLY  
  
 TYPE\_SS\_SCROLL\_DYNAMIC  
  
## Rückgabewert  
 **true**, wenn die gelöschte Zeile durch eine Lücke ersetzt wird. **false**, wenn die gelöschte Zeile entfernt wird.  
  
 Bei Verwendung von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank wird von dieser Methode für TYPE\_SS\_SCROLL\_KEYSET\-Cursor der Wert **true** und für alle anderen Resultsettypen der Wert **false** zurückgegeben.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese deletesAreDetected\-Methode wird von der deletesAreDetected\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
> [!NOTE]  
>  Gelöschte Zeilen werden von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] zwar für alle aktualisierbaren Cursortypen erkannt, die Erkennung für Vorwärtscursor und dynamische Cursor ist jedoch kurzlebig.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  