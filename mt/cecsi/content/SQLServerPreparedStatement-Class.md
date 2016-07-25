---
title: "SQLServerPreparedStatement-Klasse"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a8481c06-fbba-432b-8c69-4f4619c20ad4
caps.latest.revision: 15
caps.handback.revision: 14
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
# SQLServerPreparedStatement-Klasse
  Stellt die grundlegende Implementierung der JDBC\-Funktion für vorbereitete Anweisungen dar.  
  
 **Paket:** com.microsoft.sqlserver.jdbc  
  
 **Erweitert:** SQLServerStatement  
  
 **Implementiert:** [ISQLServerPreparedStatement](../content/ISQLServerPreparedStatement-Interface.md)  
  
## Syntax  
  
```  
  
public class SQLServerPreparedStatement  
```  
  
## Hinweise  
 SQLServerPreparedStatement stellt Methoden bereit, mit denen Sie Parameter in Form beliebiger systemeigener Java\-Typen und vieler Java\-Objekttypen angegeben können.SQLServerPreparedStatement bereitet anhand der gespeicherten Prozedur [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]**sp\_prepare** Anweisungen vor und verwendet das zurückgegebene Anweisungshandle erneut für jede darauffolgende Ausführung einer Anweisung, wobei normalerweise verschiedene vom Benutzer bereitgestellte Parameter verwendet werden.  
  
 SQLServerPreparedStatement unterstützt Batchverarbeitung, wobei eine Reihe von vorbereiteten Anweisungen in einem einzelnen Datenbank\-Roundtrip ausgeführt wird, um die Laufzeitleistung zu verbessern.  
  
 Diese Klasse unterstützt das Entpacken in die Klasse SQLServerPreparedStatement, die Schnittstelle ISQLServerPreparedStatement, die Schnittstelle  java.sql.PreparedStatement sowie die Klassen und Schnittstellen, die von  SQLServerStatement für das Entpacken unterstützt werden. Weitere Informationen finden Sie unter [Wrapper und Schnittstellen](../content/Wrappers-and-Interfaces.md).  
  
## Siehe auch  
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)   
 [API-Referenz für den JDBC-Treiber](../content/JDBC-Driver-API-Reference.md)  
  
  