---
title: "ISQLServerResultSet-Schnittstelle"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 002496f7-8ec0-4267-b4e6-ba095e2ef306
caps.latest.revision: 8
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
# ISQLServerResultSet-Schnittstelle
  Stellt ein JDBC\-Resultset dar. Die Schnittstelle wurde in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 hinzugefügt.  
  
 **Paket:** com.microsoft.sqlserver.jdbc  
  
 **Erweitert:** java.sql.ResultSet  
  
## Syntax  
  
```  
  
public interface ISQLServerResultSet  
```  
  
## Hinweise  
 Diese Schnittstelle wird durch [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md) implementiert.  
  
 Diese Schnittstelle legt die [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-spezifischen Methoden dar:  
  
|Methode|Weitere Informationen finden Sie unter|  
|-------------|--------------------------------------------|  
|public microsoft.sql.DateTimeOffset getDateTimeOffset\(int\)|[getDateTimeOffset](../content/getDateTimeOffset-int---SQLServerResultSet-.md)|  
|public microsoft.sql.DateTimeOffset getDateTimeOffset\(String\)|[getDateTimeOffset](../content/getDateTimeOffset-java.lang.string---SQLServerResultSet-.md)|  
|public void updateDateTimeOffset\(int, microsoft.sql.DateTimeOffset\)|[updateDateTimeOffset](../content/updateDateTimeOffset-int--microsoft.sql.DateTimeOffset---SQLServerResultSet-.md)|  
|public void updateDateTimeOffset\(String, microsoft.sql.DateTimeOffset\)|[updateDateTimeOffset](../content/updateDateTimeOffset-string--microsoft.sql.DateTimeOffset---SQLServerResultSet-.md)|  
  
 Diese Schnittstelle legt die folgenden [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-spezifischen Felder dar:  
  
|Feld|Weitere Informationen finden Sie unter|  
|----------|--------------------------------------------|  
|public static final int CONCUR\_SS\_OPTIMISTIC\_CC|[CONCUR\_SS\_OPTIMISTIC\_CC](../content/CONCUR_SS_OPTIMISTIC_CC-Field--SQLServerResultSet-.md)|  
|public static final int CONCUR\_SS\_OPTIMISTIC\_CCVAL|[CONCUR\_SS\_OPTIMISTIC\_CCVAL](../content/CONCUR_SS_OPTIMISTIC_CCVAL-Field--SQLServerResultSet-.md)|  
|public static final int CONCUR\_SS\_SCROLL\_LOCKS|[CONCUR\_SS\_SCROLL\_LOCKS](../content/CONCUR_SS_SCROLL_LOCKS-Field--SQLServerResultSet-.md)|  
|public static final int TYPE\_SS\_DIRECT\_FORWARD\_ONLY|[TYPE\_SS\_DIRECT\_FORWARD\_ONLY](../content/TYPE_SS_DIRECT_FORWARD_ONLY-Field--SQLServerResultSet-.md)|  
|public static final int TYPE\_SS\_SCROLL\_DYNAMIC|[TYPE\_SS\_SCROLL\_DYNAMIC](../content/TYPE_SS_SCROLL_DYNAMIC-Field--SQLServerResultSet-.md)|  
|public static final int TYPE\_SS\_SCROLL\_KEYSET|[TYPE\_SS\_SCROLL\_KEYSET](../content/TYPE_SS_SCROLL_KEYSET-Field--SQLServerResultSet-.md)|  
|public static final int TYPE\_SS\_SCROLL\_STATIC|[TYPE\_SS\_SCROLL\_STATIC](../content/TYPE_SS_SCROLL_STATIC-Field--SQLServerResultSet-.md)|  
|public static final int TYPE\_SS\_SERVER\_CURSOR\_FORWARD\_ONLY|[TYPE\_SS\_SERVER\_CURSOR\_FORWARD\_ONLY](../content/TYPE_SS_SERVER_CURSOR_FORWARD_ONLY-Field--SQLServerResultSet-.md)|  
  
## Siehe auch  
 [API-Referenz für den JDBC-Treiber](../content/JDBC-Driver-API-Reference.md)  
  
  