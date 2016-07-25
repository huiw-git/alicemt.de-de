---
title: "setObject-Methode (java.lang.String, java.lang.Object, int)"
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
  - SQLServerCallableStatement.setObject (java.lang.String, java.lang.Object, int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: a9a0c802-7851-4826-b173-87b0c0acb3a0
caps.latest.revision: 20
caps.handback.revision: 19
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
# setObject-Methode (java.lang.String, java.lang.Object, int)
    
## setObject\-Methode \(java.lang.String, java.lang.Object, int\)  
 Legt den Wert des angegebenen Parameters unter Verwendung des angegebenen Objekts und des Zieltyps fest.  
  
## Syntax  
  
```  
  
public void setObject(java.lang.String sCol,  
                      java.lang.Object o,  
                      int n)  
```  
  
#### Parameter  
 *sCol*  
  
 Ein **String** mit dem Parameternamen.  
  
 *o*  
  
 Ein **Object** \-Wert.  
  
 *n*  
  
 Ein **int** \-Objekt, das den im java.sql.Types\-Element definierten Zieltyp angibt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setObject\-Methode wird von der setObject\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
 Ab [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 wird das Verhalten der Methode durch die **sendTimeAsDatetime**\-Verbindungseigenschaft \([Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md)\) und [SQLServerDataSource.setSendTimeAsDatetime](../content/setSendTimeAsDatetime-Method--SQLServerDataSource-.md) geändert.  
  
 Weitere Informationen finden Sie unter [Konfigurieren der Art und Weise, wie java.sql.Time-Werte an den Server gesendet werden](../content/Configuring-How-java.sql.Time-Values-are-Sent-to-the-Server.md).  
  
## Siehe auch  
 [setObject-Methode &#40;SQLServerCallableStatement&#41;](../content/setObject-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  