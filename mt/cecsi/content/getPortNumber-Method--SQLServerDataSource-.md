---
title: "getPortNumber-Methode (SQLServerDataSource)"
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
  - SQLServerDataSource.getPortNumber
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: e5dc38d0-4340-4ad7-a56e-1d2a0f0fd846
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
# getPortNumber-Methode (SQLServerDataSource)
    
## getPortNumber\-Methode \(SQLServerDataSource\)  
 Gibt die aktuelle Portnummer für die Kommunikation mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] zurück.  
  
## Syntax  
  
```  
  
public int getPortNumber()  
```  
  
## Rückgabewert  
 Ein Wert vom Typ **int** mit der aktuellen Portnummer.  
  
## Hinweise  
 Die Portnummer ist die TCP\/IP\-Portnummer, die beim Öffnen einer Socketverbindung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verwendet wird. Ist die portNumber\-Eigenschaft nicht festgelegt, wird von der getPortNumber\-Methode der Standardwert \(1433\) zurückgegeben.  
  
> [!NOTE]  
>  Von der [setPortNumber](../content/setPortNumber-Method--SQLServerDataSource-.md)\-Methode wird für den eingegebenen Portwert keine Bereichsprüfung durchgeführt. Sie können ungültige Portnummern weitergeben, z. B. 99999, ohne dabei einen Fehler auszulösen.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  