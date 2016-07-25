---
title: "getSearchStringEscape-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.getSearchStringEscape
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: ea0f95d0-0238-4dc8-9f26-7ff9b65f30c3
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
# getSearchStringEscape-Methode (SQLServerDatabaseMetaData)
    
## getSearchStringEscape\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft den **String** ab, mit dem sich Platzhalterzeichen mit Escapezeichen versehen lassen.  
  
## Syntax  
  
```  
  
public java.lang.String getSearchStringEscape()  
```  
  
## Rückgabewert  
 Ein **String** , der die Zeichenfolge zum Versehen der Platzhalterzeichenfolge mit Escapezeichen enthält.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getSearchStringEscape\-Methode wird von der getSearchStringEscape\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
 Diese Methode wird nur für Suchen nach Metadatenmustern verwendet. Sie gibt "\\" zurück. Mit einem **String** \-Suchmuster können Platzhalter \("%" und "\_"\) mit Escapezeichen versehen und durch Voranstellen eines umgekehrten Schrägstrichs als Literale bereitgestellt werden. Hierdurch wird "\\%" in "\[%\]" und "\\\_" in "\[\_\]" konvertiert.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  