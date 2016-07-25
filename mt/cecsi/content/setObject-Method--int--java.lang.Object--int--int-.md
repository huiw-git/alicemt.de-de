---
title: "setObject-Methode (int, java.lang.Object, int, int)"
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
  - SQLServerPreparedStatement.setObject (int, java.lang.Object, int, int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: d190ee20-d669-4c6f-a081-d5cfec2f72ca
caps.latest.revision: 18
caps.handback.revision: 17
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
# setObject-Methode (int, java.lang.Object, int, int)
    
## setObject\-Methode \(int, java.lang.Object, int, int\)  
 Legt den Wert des angegebenen Parameters unter Verwendung des angegebenen Objekts, des Zieltyps und der Dezimalstellen fest.  
  
## Syntax  
  
```  
  
public final void setObject(int n,  
                            java.lang.Object obj,  
                            int targetSqlType,  
                            int scale)  
```  
  
#### Parameter  
 *n*  
  
 Ein Wert vom Typ **int** zum Angeben der Parameternummer.  
  
 *obj*  
  
 Ein Objekt.  
  
 *targetSqlType*  
  
 Ein **int** \-Objekt, das den im java.sql.Types\-Element definierten Zieltyp angibt.  
  
 *scale*  
  
 Ein Element vom Typ **int** , das die Anzahl von Stellen rechts des Dezimalzeichens anzeigt. Dieser Parameter wird für alle Typen verwendet, die nicht "NUMERIC" oder "DECIMAL" sind.  
  
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
  
  