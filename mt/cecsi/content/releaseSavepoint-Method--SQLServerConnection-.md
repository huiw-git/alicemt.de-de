---
title: "releaseSavepoint-Methode (SQLServerConnection)"
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
  - SQLServerConnection.releaseSavepoint
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: b6b625ea-c7ce-4a32-a9e0-6d2b4321bfd8
caps.latest.revision: 13
caps.handback.revision: 13
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
# releaseSavepoint-Methode (SQLServerConnection)
  Entfernt das angegebene [SQLServerSavepoint](../content/SQLServerSavepoint-Class.md)\-Objekt aus der aktuellen Transaktion.  
  
> [!NOTE]  
>  Diese Methode wird von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] derzeit nicht unterstützt.  
  
## Syntax  
  
```  
  
public void releaseSavepoint(java.sql.Savepoint savepoint)  
```  
  
#### Parameter  
 *savepoint*  
  
 Das zu entfernende SavePoint\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese releaseSavepoint\-Methode wird von der releaseSavepoint\-Methode in der java.sql.Connection\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [SQLServerConnection-Klasse](../content/SQLServerConnection-Class.md)  
  
  