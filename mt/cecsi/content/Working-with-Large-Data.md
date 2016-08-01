---
title: "Arbeiten mit umfangreichen Daten"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5b93569f-eceb-4f05-b49c-067564cd3c85
caps.latest.revision: 24
caps.handback.revision: 23
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
# Arbeiten mit umfangreichen Daten
  Der JDBC\-Treiber bietet Unterstützung für die adaptive Pufferung, mit der Sie beliebige Daten mit umfangreichen Werten ohne den Aufwand von Servercursorn abrufen können. Mithilfe der adaptiven Pufferung ruft [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] Ergebnisse der Anweisungsausführung erst dann von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ab, wenn sie in der Anwendung benötigt werden, statt alle Ergebnisse auf einmal abzurufen. Der Treiber verwirft außerdem die Ergebnisse, sobald die Anwendung nicht mehr auf sie zugreifen kann.  
  
 In Version 1.2 von [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] JDBC Driver war der Pufferungsmodus standardmäßig auf "**full**" festgelegt. Wenn die responseBuffering\-Verbindungseigenschaft in der Anwendung in den Verbindungseigenschaften oder mit der [setResponseBuffering](../content/setResponseBuffering-Method--SQLServerStatement-.md)\-Methode des [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekts nicht auf "**adaptive**" festgelegt ist, unterstützte der Treiber das Lesen des gesamten Resultsets auf einmal vom Server. Um das Verhalten der adaptiven Pufferung zu verwenden, musste die responseBuffering\-Verbindungseigenschaft in der Anwendung explizit auf "**adaptive**" festgelegt werden.  
  
 Der **adaptive**\-Wert ist der Standardpufferungsmodus, und der JDBC\-Treiber puffert nach Bedarf so wenig Daten wie möglich. Weitere Informationen zum Verwenden der adaptiven Pufferung finden Sie unter [Verwenden der adaptiven Pufferung](../content/Using-Adaptive-Buffering.md).  
  
 Die Themen in diesem Abschnitt beschreiben verschiedene Möglichkeiten, wie Sie Daten mit umfangreichen Werten aus einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank abrufen können.  
  
## In diesem Abschnitt  
  
|Thema|Beschreibung|  
|-----------|------------------|  
|[Beispiel zum Lesen umfangreicher Daten](../content/Reading-Large-Data-Sample.md)|Beschreibt die Verwendung einer SQL\-Anweisung zum Abrufen von Daten mit umfangreichen Werten.|  
|[Beispiel zum Lesen umfangreicher Daten mit gespeicherten Prozeduren](../content/Reading-Large-Data-with-Stored-Procedures-Sample.md)|Beschreibt das Abrufen eines umfangreichen CallableStatement OUT\-Parameterwerts.|  
|[Beispiel zum Aktualisieren umfangreicher Daten](../content/Updating-Large-Data-Sample.md)|Beschreibt das Aktualisieren von Daten mit umfangreichen Werten in einer Datenbank.|  
  
## Siehe auch  
 [Beispiele für JDBC-Treiberanwendungen](../content/Sample-JDBC-Driver-Applications.md)  
  
  