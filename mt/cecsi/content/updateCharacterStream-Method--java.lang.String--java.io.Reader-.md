---
title: "updateCharacterStream-Methode (java.lang.String, java.io.Reader)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a8ec22a9-4bbd-4759-9f21-957304ef3a5e
caps.latest.revision: 17
caps.handback.revision: 16
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
# updateCharacterStream-Methode (java.lang.String, java.io.Reader)
  Aktualisiert die angegebene Spalte mit einem Zeichendatenstromwert.  
  
## Syntax  
  
```  
  
public void updateCharacterStream(java.lang.String columnLabel,  
                                  java.io.Reader reader)  
```  
  
#### Parameter  
 *columnLabel*  
  
 Ein **String** mit der Spaltenbezeichnung.  
  
 *reader*  
  
 Ein Reader\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese updateCharacterStream\-Methode wird von der updateCharacterStream\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Von dieser Methode werden Unicode\-Zeichen aus einem Reader\-Objekt an ausgewählte Text\- und Binärspalten übergeben. Hierzu zählen alle Textspalten sowie Spalten vom Typ **binary**, **varbinary**, **varbinary\(max\)**, **image** und **xml**, aber keine **udt**\-Spalten.  
  
 Die Verwendung dieser Methode für die Datentypen **image**, **text** und **ntext** von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] kann sich negativ auf die Leistung auswirken.  
  
## Siehe auch  
 [updateCharacterStream-Methode &#40;ISQLServerResultSet&#41;](../content/updateCharacterStream-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  