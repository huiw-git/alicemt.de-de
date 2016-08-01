---
title: "Verbinden und Abrufen von Daten"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ce43cc20-46a3-42ff-a3fb-75ad1ed10e08
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
# Verbinden und Abrufen von Daten
  Bei der Arbeit mit [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] gibt es zwei Hauptmethoden, um eine Verbindung mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank herzustellen. Eine Methode besteht darin, die Verbindungseigenschaften in der Verbindungs\-URL festzulegen und anschließend die getConnection\-Methode der DriverManager\-Klasse aufzurufen, um ein [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt zurückzugeben.  
  
> [!NOTE]  
>  Eine Liste der vom JDBC\-Treiber unterstützten Verbindungseigenschaften finden Sie unter [Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md).  
  
 Bei der zweiten Methode werden die Verbindungseigenschaften mit den Festlegungsmethoden der [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Klasse festgelegt und anschließend die [getConnection](../content/getConnection-Method--SQLServerDataSource-.md)\-Methode aufgerufen, um ein SQLServerConnection\-Objekt zurückzugeben.  
  
 Die Themen in diesem Abschnitt beschreiben die verschiedenen Möglichkeiten, um eine Verbindung zu einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank herzustellen, und die verschiedenen Verfahren, um Daten abzurufen.  
  
## In diesem Abschnitt  
  
|Thema|Beschreibung|  
|-----------|------------------|  
|[Verbindungs-URL - Beispiel](../content/Connection-URL-Sample.md)|Beschreibt die Verwendung einer Verbindungs\-URL, um eine Verbindung zu [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] herzustellen und Daten anschließend mit einer SQL\-Anwendung abzurufen.|  
|[Beispiel für Datenquellen](../content/Data-Source-Sample.md)|Beschreibt die Verwendung einer Datenquelle, um eine Verbindung zu SQL Server herzustellen und Daten anschließend mit einer gespeicherten Prozedur abzurufen.|  
  
## Siehe auch  
 [Beispiele für JDBC-Treiberanwendungen](../content/Sample-JDBC-Driver-Applications.md)  
  
  