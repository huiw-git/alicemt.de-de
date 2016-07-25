---
title: "setPortNumber-Methode (SQLServerDataSource)"
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
  - SQLServerDataSource.setPortNumber
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 59c5fa23-bc1a-4142-af17-70e275f0b833
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
# setPortNumber-Methode (SQLServerDataSource)
    
## setPortNumber\-Methode \(SQLServerDataSource\)  
 Legt die Portnummer zur Kommunikation mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] fest.  
  
## Syntax  
  
```  
  
public void setPortNumber(int portNumber)  
```  
  
#### Parameter  
 *portNumber*  
  
 Ein Wert vom Typ **int** , der die Portnummer enthält.  
  
## Hinweise  
 Die Portnummer ist die TCP\/IP\-Portnummer, die beim Öffnen einer Socketverbindung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verwendet wird. Ist die portNumber\-Eigenschaft nicht festgelegt, wird von der [getPortNumber](../content/getPortNumber-Method--SQLServerDataSource-.md)\-Methode der Standardwert "1433" zurückgegeben.  
  
> [!NOTE]  
>  Von der setPortNumber\-Methode wird für den eingegebenen Portwert keine Bereichsprüfung durchgeführt. Sie können eine nicht gültige Portnummer weitergeben, z. B. 99999, ohne dabei einen Fehler auszulösen.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  