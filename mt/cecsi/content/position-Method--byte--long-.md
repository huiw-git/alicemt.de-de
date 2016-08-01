---
title: "position-Methode (byte, long)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLServerBlob.position (byte[], long)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 787412c2-4342-49c8-9ca2-7a9ddcd3277c
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
# position-Methode (byte, long)
    
## position\-Methode \(byte\[\], long\)  
 Gibt die Position eines angegebenen Musters im BLOB auf der Grundlage des angegebenen  **byte** array\-Musters und des Startindexes zurück.  
  
## Syntax  
  
```  
  
public long position(byte[] bPattern,  
                     long start)  
```  
  
#### Parameter  
 *bPattern*  
  
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
  
  