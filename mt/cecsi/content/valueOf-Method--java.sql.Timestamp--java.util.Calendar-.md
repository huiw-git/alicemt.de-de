---
title: "valueOf-Methode (java.sql.Timestamp, java.util.Calendar)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7320c383-0b06-446d-963b-7005e50324a2
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
# valueOf-Methode (java.sql.Timestamp, java.util.Calendar)
  Erstellt ein **DateTimeOffset**\-Objekt, das einen Zeitpunkt in einem bestimmten Offset von GMT darstellt, wenn ein java.sql.Timestamp\- und ein java.util.Calendar\-Wert das Offset angeben.  
  
## Syntax  
  
```  
  
public static DateTimeOffset valueOf(java.sql.Timestamp timestamp, java.util.Calendar calendar)  
```  
  
#### Parameter  
 *timestamp*  
  
 Ein java.sql.Timestamp\-Wert.  
  
 *calendar*  
  
 Der Offsetwert.  Die date\- und time\-Komponenten von *calendar* werden gemäß dem *timestamp*\-Wert festgelegt.  
  
## Rückgabewert  
 Gibt ein DateTimeOffset\-Objekt zurück, das den vom  java.sql.Timestamp\-Objekt gegebenen Zeitpunkt in der gegebenen Zeitzone des java.util.Calendar\-Objekts darstellt.  
  
## Hinweise  
 Mit dieser Methode wird auch das java.util.Calendar\-Objekt auf den vom  java.sql.Timestamp\-Objekt gegebenen Zeitpunkt gesetzt.  
  
## Siehe auch  
 [DateTimeOffset-Klasse](../content/DateTimeOffset-Class.md)   
 [DateTimeOffset-Elemente](../content/DateTimeOffset-Members.md)  
  
  