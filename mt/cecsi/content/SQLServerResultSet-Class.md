---
title: "SQLServerResultSet-Klasse"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: eaffcff1-286c-459f-83da-3150778480c9
caps.latest.revision: 17
caps.handback.revision: 16
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
# SQLServerResultSet-Klasse
  Stellt ein JDBC\-Resultset dar.  
  
 **Paket:** com.microsoft.sqlserver.jdbc  
  
 **Implementiert:** [ISQLServerResultSet](../content/ISQLServerResultSet-Interface.md)  
  
## Syntax  
  
```  
  
public final class SQLServerResultSet  
```  
  
## Hinweise  
 Zwei Arten von Resultsets stehen zur Verfügung: clientseitige und serverseitige Resultsets.  
  
 Clientseitige Resultsets werden verwendet, wenn die Ergebnisse in den Clientprozessspeicher passen. Diese Ergebnisse bieten die höchste Geschwindigkeit und werden von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] vollständig aus der Datenbank gelesen. Bei diesen Resultsets entstehen für die Datenbank keine zusätzlichen Lasten, da keine serverseitigen Cursor erstellt werden müssen. Allerdings können diese Resultsettypen nicht aktualisiert werden.  
  
 Serverseitige Resultsets können verwendet werden, wenn die Ergebnisse nicht in den Clientprozessspeicher passen oder wenn das Resultset aktualisierbar sein muss. Bei dieser Art von Resultset wird vom JDBC\-Treiber ein serverseitiger Cursor erstellt, und die Zeilen des Resultsets werden transparent abgerufen, während der Benutzer einen Bildlauf ausführt.  
  
 Die SQLServerResultSet\-Klasse bietet eine Vielzahl von Methoden, mit denen sich das Resultset mit beliebigen systemeigenen Java\-Datentypen sowie mit vielen Java\-Objekttypen aktualisieren lässt.  
  
 Diese Klasse unterstützt das Entpacken in die Klasse SQLServerResultSet, die Schnittstelle  ISQLServerResultSet und die Schnittstelle  java.sql.ResultSet. Weitere Informationen finden Sie unter [Wrapper und Schnittstellen](../content/Wrappers-and-Interfaces.md).  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [API-Referenz für den JDBC-Treiber](../content/JDBC-Driver-API-Reference.md)  
  
  