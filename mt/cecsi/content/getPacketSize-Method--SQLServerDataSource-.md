---
title: "getPacketSize-Methode (SQLServerDataSource)"
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
  - SQLServerDataSource.getPacketSize
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: b2e9f01a-2e51-47e5-90bf-43c62d1be74d
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
# getPacketSize-Methode (SQLServerDataSource)
    
## getPacketSize\-Methode \(SQLServerDataSource\)  
 Gibt die aktuelle Netzwerkpaketgröße \(in Bytes\) für die Kommunikation mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] zurück.  
  
## Syntax  
  
```  
  
public int getPacketSize()  
```  
  
## Rückgabewert  
 Ein Wert vom Typ **int** mit der aktuellen Netzwerkpaketgröße.  
  
## Hinweise  
 Ist die packetSize\-Eigenschaft nicht festgelegt, wird von der getPacketSize\-Methode der Standardwert \(8000\) zurückgegeben.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  