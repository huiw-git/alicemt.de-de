---
title: "setURL-Methode (SQLServerDataSource)"
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
  - SQLServerDataSource.setURL
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: bea70100-ac98-4625-8748-ef7cc0b111ea
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
# setURL-Methode (SQLServerDataSource)
    
## setURL\-Methode \(SQLServerDataSource\)  
 Legt die URL fest, die zum Herstellen einer Verbindung mit der Datenquelle verwendet wird.  
  
## Syntax  
  
```  
  
public void setURL(java.lang.String url)  
```  
  
#### Parameter  
 *url*  
  
 Ein **String** mit der URL.  
  
## Hinweise  
 Aus Sicherheitsgründen sollte das Kennwort nicht in der URL für die setURL\-Methode enthalten sein. Der Grund hierfür ist, dass Java\-Anwendungsserver von Drittanbietern oft den für die URL\-Eigenschaft festgelegten Wert auf der Benutzeroberfläche für die Datenquellenkonfiguration anzeigen. Verwenden Sie stattdessen die [setPassword](../content/setPassword-Method--SQLServerDataSource-.md)\-Methode, um den Wert für das Kennwort festzulegen. Java\-Anwendungsserver zeigen kein in der Datenquelle festgelegtes Kennwort auf der Konfigurationsbenutzeroberfläche an.  
  
> [!NOTE]  
>  Wird die setURL\-Methode nicht vor dem Aufruf der [getURL](../content/getURL-Method--SQLServerDataSource-.md)\-Methode aufgerufen, wird von getURL der Standardwert \(jdbc:sqlserver:\/\/\) zurückgegeben.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  