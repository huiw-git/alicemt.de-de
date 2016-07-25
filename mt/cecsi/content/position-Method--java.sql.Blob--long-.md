---
title: "position-Methode (java.sql.Blob, long)"
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
  - SQLServerBlob.position (java.sql.Blob.long)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: ebd005e5-f6c5-4789-87f9-d2fdacd35060
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
# position-Methode (java.sql.Blob, long)
    
## position\-Methode \(java.sql.Blob, long\)  
 Gibt die Position eines angegebenen Musters im BLOB auf der Grundlage des angegebenen Musters und des Startindexes zurück.  
  
## Syntax  
  
```  
  
public long position(java.sql.Blob pattern,  
                     long start)  
```  
  
#### Parameter  
 *pattern*  
  
 Das zu suchende Muster.  
  
 *start*  
  
 Der Startindex, in dem gesucht werden soll.  
  
## Rückgabewert  
 Ein Wert vom Typ **long** der Position, an der das Muster gefunden wurde oder "\-1", wenn es nicht gefunden wurde.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese position\-Methode wird von der position\-Methode in der java.sql.Blob\-Schnittstelle angegeben.  
  
## Siehe auch  
 [position-Methode &#40;SQLServerBlob&#41;](../content/position-Method--SQLServerBlob-.md)   
 [SQLServerBlob-Methoden](../content/SQLServerBlob-Methods.md)   
 [SQLServerBlob-Elemente](../content/SQLServerBlob-Members.md)   
 [SQLServerBlob-Klasse](../content/SQLServerBlob-Class.md)  
  
  