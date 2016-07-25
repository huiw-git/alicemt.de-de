---
title: "SQLServerBlob-Konstruktor (SQLServerConnection, byte)"
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
  - SQLServerConnection, byte[].SQLServerBlob
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 9fe573e3-30db-4828-abab-e9346493e931
caps.latest.revision: 14
caps.handback.revision: 14
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
# SQLServerBlob-Konstruktor (SQLServerConnection, byte)
    
## SQLServerBlob\-Konstruktor \(SQLServerConnection, byte\[\]\)  
 Initialisiert eine neue Instanz der [SQLServerBlob](../content/SQLServerBlob-Class.md)\-Klasse, wenn ein [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt und ein Array vom Typ **byte** angegeben werden.  
  
> [!NOTE]  
>  Diese Methode ist seit Version 2.0 von JDBC Driver veraltet. Verwenden Sie stattdessen die [createBlob](../content/createBlob-Method--SQLServerConnection-.md)\-Methode der [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Klasse.  
  
## Syntax  
  
```  
  
public SQLServerBlob(SQLServerConnection connection,  
                     byte[] data)  
```  
  
#### Parameter  
 *connection*  
  
 Ein SQLServerConnection\-Objekt.  
  
 *data*  
  
 Ein **byte** \-Array.  
  
## Siehe auch  
 [SQLServerBlob-Konstruktoren](../content/SQLServerBlob-Constructors.md)   
 [SQLServerBlob-Elemente](../content/SQLServerBlob-Members.md)   
 [SQLServerBlob-Klasse](../content/SQLServerBlob-Class.md)  
  
  