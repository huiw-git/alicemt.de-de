---
title: "getObjectInstance-Methode (SQLServerDataSourceObjectFactory)"
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
  - SQLServerDataSourceObjectFactory.getObjectInstance
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 0a1503e2-e991-4d70-a223-087fc63baf73
caps.latest.revision: 7
caps.handback.revision: 7
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
# getObjectInstance-Methode (SQLServerDataSourceObjectFactory)
    
## getObjectInstance\-Methode \(SQLServerDataSourceObjectFactory\)  
 Ruft eine Instanz des angegebenen Datenquellenobjekts ab.  
  
## Syntax  
  
```  
  
public java.lang.Object getObjectInstance(java.lang.Object ref,  
                                          javax.naming.Name name,  
                                          javax.naming.Context c,  
                                          java.util.Hashtable h)  
```  
  
#### Parameter  
 *ref*  
  
 Ein **Object** \-Wert.  
  
 *name*  
  
 Der Name des Objekts.  
  
 *c*  
  
 Der Kontext relativ zum angegebenen Namen.  
  
 *h*  
  
 Die Umgebung, die beim Erstellen des Objekts verwendet wird.  
  
## Rückgabewert  
 Ein **Object** \-Wert.  
  
## Ausnahmen  
 java.sql.SQLException  
  
## Hinweise  
 Die getObjectInstance\-Methode wird von der getObjectInstance\-Methode in der javax.naming.spi.ObjectFactory\-Schnittstelle angegeben.  
  
## Siehe auch  
 [SQLServerDataSourceObjectFactory-Elemente](../content/SQLServerDataSourceObjectFactory-Methods.md)   
 [SQLServerDataSourceObjectFactory-Elemente](../content/SQLServerDataSourceObjectFactory-Members.md)   
 [SQLServerDataSourceObjectFactory-Klasse](../content/SQLServerDataSourceObjectFactory-Class.md)  
  
  