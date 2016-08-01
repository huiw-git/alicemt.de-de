---
title: "Verwenden von Anweisungen mit SQL"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fe28f48a-e1bc-48ff-a5e7-c24cd6e5ecc7
caps.latest.revision: 11
caps.handback.revision: 11
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
# Verwenden von Anweisungen mit SQL
  Wenn Sie Daten in einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank mit [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] und Inline\-SQL\-Anweisungen verarbeiten, können Sie verschiedenen Klassen verwenden. Die verwendete Klasse hängt vom Typ der SQL\-Anweisung ab, die ausgeführt werden soll.  
  
 Wenn die SQL\-Anweisung keine IN\-Parameter enthält, verwenden Sie die [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Klasse. Wenn IN\-Parameter vorhanden sind, verwenden Sie die [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\-Klasse.  
  
> [!NOTE]  
>  Wenn Sie SQL\-Anweisungen verwenden müssen, die IN\- und OUT\-Parameter enthalten, müssen Sie diese als gespeicherte Prozeduren implementieren und mit der [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Klasse aufrufen. Weitere Informationen zum Verwenden gespeicherter Prozeduren finden Sie unter [Verwenden von Anweisungen mit gespeicherten Prozeduren](../content/Using-Statements-with-Stored-Procedures.md).  
  
 Die folgenden Abschnitte enthalten Beschreibungen der verschiedenen Szenarios für die Arbeit mit Daten in einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank mit SQL\-Anweisungen.  
  
## In diesem Abschnitt  
  
|Thema|Beschreibung|  
|-----------|------------------|  
|[Verwenden von SQL-Anweisungen ohne Parameter](../content/Using-an-SQL-Statement-with-No-Parameters.md)|Beschreibt die Verwendung von SQL\-Anweisungen, die keine Parameter enthalten.|  
|[Verwenden von SQL-Anweisungen mit Parametern](../content/Using-an-SQL-Statement-with-Parameters.md)|Beschreibt die Verwendung von SQL\-Anweisungen, die Parameter enthalten.|  
|[Ändern von Datenbankobjekten mit SQL-Anweisungen](../content/Using-an-SQL-Statement-to-Modify-Database-Objects.md)|Beschreibt die Verwendung von SQL\-Anweisungen, um Datenbankobjekte zu ändern.|  
|[Ändern von Daten mit SQL-Anweisungen](../content/Using-an-SQL-Statement-to-Modify-Data.md)|Beschreibt die Verwendung von SQL\-Anweisungen, um Daten in einer Datenbank zu ändern.|  
  
## Siehe auch  
 [Verwenden von Anweisungen mit dem JDBC-Treiber](../content/Using-Statements-with-the-JDBC-Driver.md)  
  
  