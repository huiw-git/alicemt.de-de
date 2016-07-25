---
title: "insertRow-Methode (ISQLServerResultSet)"
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
  - SQLServerResultSet.insertRow
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 363d1008-1396-4fc0-8e27-c9ba2499e7f1
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
# insertRow-Methode (ISQLServerResultSet)
    
## insertRow\-Methode \(ISQLServerResultSet\)  
 Fügt den Inhalt der Einfügezeile diesem [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt und der Datenbank hinzu.  
  
## Syntax  
  
```  
  
public void insertRow()  
```  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese insertRow\-Methode wird von der insertRow\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Beim Aufruf dieser Methode muss sich der Cursor in der Einfügezeile befinden. Nach dem Aufruf dieser Methode verbleibt der Cursor in der Einfügezeile, und das Resultset im Einfügemodus.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  