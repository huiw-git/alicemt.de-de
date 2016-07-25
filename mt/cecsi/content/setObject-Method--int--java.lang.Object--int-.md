---
title: "setObject-Methode (int, java.lang.Object, int)"
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
  - SQLServerPreparedStatement.setObject (int, java.lang.Object, int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 78bfb6cc-8ca4-4879-9e2b-04164e746314
caps.latest.revision: 19
caps.handback.revision: 18
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
# setObject-Methode (int, java.lang.Object, int)
    
## setObject\-Methode \(int, java.lang.Object, int\)  
 Legt den Wert des angegebenen Parameters unter Verwendung des angegebenen Objekts und des Zieltyps fest.  
  
## Syntax  
  
```  
  
public final void setObject(int n,  
                            java.lang.Object obj,  
                            int targetSqlType)  
```  
  
#### Parameter  
 *n*  
  
 Ein Wert vom Typ **int** zum Angeben der Parameternummer.  
  
 *obj*  
  
 Ein Objekt.  
  
 *targetSqlType*  
  
 Ein **int** \-Objekt, das den im java.sql.Types\-Element definierten Zieltyp angibt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Die setObject\-Methode wird von der setObject\-Methode in der java.sql.PreparedStatement\-Schnittstelle angegeben.  
  
 Ab [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 wird das Verhalten der Methode durch die **sendTimeAsDatetime**\-Verbindungseigenschaft \([Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md)\) und [SQLServerDataSource.setSendTimeAsDatetime](../content/setSendTimeAsDatetime-Method--SQLServerDataSource-.md) geändert.  
  
 Weitere Informationen finden Sie unter [Konfigurieren der Art und Weise, wie java.sql.Time-Werte an den Server gesendet werden](../content/Configuring-How-java.sql.Time-Values-are-Sent-to-the-Server.md).  
  
## Siehe auch  
 [setObject-Methode &#40;ISQLServerPreparedStatement&#41;](../content/setObject-Method--SQLServerPreparedStatement-.md)   
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)   
 [SQLServerPreparedStatement-Klasse](../content/SQLServerPreparedStatement-Class.md)  
  
  