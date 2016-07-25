---
title: "Arbeiten mit Datentypen (JDBC)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b39f44d0-3710-4bc6-880c-35bd8c10a734
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
# Arbeiten mit Datentypen (JDBC)
  Die Hauptfunktion von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] liegt darin, Java\-Entwicklern den Zugriff auf Daten in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbanken zu ermöglichen. Der JDBC\-Treiber sorgt dazu für die Konvertierung der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentypen sowie den Java\-Typen und \-Objekten.  
  
> [!NOTE]  
>  Eine ausführliche Beschreibung der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\- und JDBC\-Treiberdatentypen, einschließlich deren Unterschiede und deren Konvertierung in Java\-Datentypen, finden Sie unter [Grundlegendes zu den Datentypen in JDBC Driver](../content/Understanding-the-JDBC-Driver-Data-Types.md).  
  
 Um SQL Server\-Datentypen verarbeiten zu können, enthält der JDBC\-Treiber get\<Type\>\- und set\<Type\>\-Methoden für die [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\- und [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Klasse sowie get\<Type\>\- und update\<Type\>\-Methoden für die [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Klasse. Die verwendete Methode hängt vom Datentyp ab, der verarbeitet wird, sowie davon, ob Resultsets oder Abfragen verwendet werden.  
  
 Die Themen in diesem Abschnitt beschreiben, wie Sie in Java\-Anwendungen unter Verwendung von JDBC\-Treiberdatentypen auf [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Daten zugreifen.  
  
## In diesem Abschnitt  
  
|Thema|Beschreibung|  
|-----------|------------------|  
|[Standarddatentypen - Beispiel](../content/Basic-Data-Types-Sample.md)|Beschreibt, wie Werte von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Standarddatentypen mithilfe von Abrufmethoden für Resultsets abgerufen und diese Werte mithilfe von Updatemethoden für Resultsets aktualisiert werden.|  
|[Beispiel für den SQLXML-Datentyp](../content/SQLXML-Data-Type-Sample.md)|Beschreibt das Speichern von XML\-Daten in einer relationalen Datenbank, das Abrufen von XML\-Daten aus einer Datenbank sowie das Analysieren von XML\-Daten mit dem Java\-Datentyp **SQLXML**.|  
  
## Siehe auch  
 [Beispiele für JDBC-Treiberanwendungen](../content/Sample-JDBC-Driver-Applications.md)  
  
  