---
title: "Arbeiten mit Resultsets"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4fc4b1c6-3075-4ad7-9244-865d9ede7ae6
caps.latest.revision: 10
caps.handback.revision: 10
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
# Arbeiten mit Resultsets
  Bei der Verarbeitung von Daten in einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank besteht eine Methode zum Bearbeiten der Daten darin, ein Resultset zu verwenden.[!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] unterstützt über das [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt die Verwendung von Resultsets. Mithilfe des SQLServerResultSet\-Objekts können Sie die von einer SQL\-Anweisung oder gespeicherten Prozedur zurückgegebenen Daten abrufen, die Daten bei Bedarf aktualisieren und dann wieder in der Datenbank speichern.  
  
 Das SQLServerResultSet\-Objekt enthält darüber hinaus Methoden, um in den Datenzeilen zu navigieren, die enthaltenen Daten abzurufen oder festzulegen und die Sensitivität gegenüber Änderungen in der zugrunde liegenden Datenbank einzurichten.  
  
> [!NOTE]  
>  Weitere Informationen zur Verwaltung von Resultsets, einschließlich deren Sensitivität gegenüber Änderungen, finden Sie unter [Verwalten von Resultsets mit dem JDBC-Treiber](../content/Managing-Result-Sets-with-the-JDBC-Driver.md).  
  
 Die Themen in diesem Abschnitt beschreiben verschiedene Möglichkeiten, wie Sie mithilfe von Resultsets die in einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank enthaltenen Daten bearbeiten können.  
  
## In diesem Abschnitt  
  
|Thema|Beschreibung|  
|-----------|------------------|  
|[Abrufen von Resultsetdaten - Beispiel](../content/Retrieving-Result-Set-Data-Sample.md)|Beschreibt die Verwendung eines Resultsets, um Daten aus einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank abzurufen und anzuzeigen.|  
|[Ändern von Resultsetdaten - Beispiel](../content/Modifying-Result-Set-Data-Sample.md)|Beschreibt die Verwendung eines Resultsets, um Daten in eine [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank einzufügen, daraus abzurufen bzw. darin zu ändern.|  
|[Zwischenspeichern von Resultsetdaten - Beispiel](../content/Caching-Result-Set-Data-Sample.md)|Beschreibt die Verwendung eines Resultsets, um umfangreiche Daten aus einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank abzurufen, und wie die Zwischenspeicherung dieser Daten im Client gesteuert wird.|  
  
## Siehe auch  
 [Beispiele für JDBC-Treiberanwendungen](../content/Sample-JDBC-Driver-Applications.md)  
  
  