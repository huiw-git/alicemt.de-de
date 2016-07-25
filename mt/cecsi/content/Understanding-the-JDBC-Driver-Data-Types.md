---
title: "Grundlegendes zu den Datentypen in JDBC Driver"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7802328d-4d23-4775-9573-4169b127d258
caps.latest.revision: 27
caps.handback.revision: 26
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
# Grundlegendes zu den Datentypen in JDBC Driver
  [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] unterstützt die Verwendung von einfachen und erweiterten JDBC\-Datentypen in einer Java\-Anwendung, die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] als Datenbank verwendet.  
  
 Das JDBC\-Typsystem vermittelt die Konvertierung zwischen [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentypen und Java\-Typen und \-Objekten. Die JDBC\-Typen beruhen auf den SQL\-92\- und SQL\-99\-Typen. Der JDBC\-Treiber befolgt die JDBC\-Spezifikation und stellt eine optimale Balance zwischen Vorhersehbarkeit und Flexibilität bereit.  
  
 Die Themen in diesem Abschnitt beschreiben die Verwendung der grundlegenden und erweiterten Datentypen sowie das Konvertieren der Datentypen in andere Datentypen.  
  
## In diesem Abschnitt  
  
|Thema|Beschreibung|  
|-----------|------------------|  
|[Verwenden von Standarddatentypen](../content/Using-Basic-Data-Types.md)|Beschreibt die grundlegenden JDBC\-Datentypen. Umfasst Beispiele zum Arbeiten mit den Datentypen mithilfe von Resultsets, parametrisierten Abfragen und gespeicherten Prozeduren.|  
|[Konfigurieren der Art und Weise, wie java.sql.Time-Werte an den Server gesendet werden](../content/Configuring-How-java.sql.Time-Values-are-Sent-to-the-Server.md)|Beschreibt die Generierung von Datumsangaben durch den JDBC\-Treiber.|  
|[Verwenden von erweiterten Datentypen](../content/Using-Advanced-Data-Types.md)|Beschreibt die erweiterten JDBC\-Datentypen.|  
|[Grundlegendes zu den Unterschieden von Datentypen](../content/Understanding-Data-Type-Differences.md)|Beschreibt Unterschiede zwischen den verschiedenen Datentypen des JDBC\-Treibers.|  
|[Grundlegendes zu Datentypkonvertierungen](../content/Understanding-Data-Type-Conversions.md)|Beschreibt, wie die Datentypkonvertierung bei der Verwendung von Methoden zum Festlegen und Abrufen behandelt wird.|  
|[Unterstützung für nationale Zeichensätze](../content/National-Character-Set-Support.md)|Beschreibt die Unterstützung der Typen für nationale Zeichensätze.|  
|[Unterstützen von XML-Daten](../content/Supporting-XML-Data.md)|Beschreibt die SQLXML\-Schnittstelle. Beschreibt außerdem, wie Sie XML\-Daten mit dem **SQLXML**\-Java\-Datentyp in bzw. aus einer relationalen Datenbank schreiben und lesen.|  
|[Wrapper und Schnittstellen](../content/Wrappers-and-Interfaces.md)|Behandelt die Schnittstellen, die über die [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-spezifischen Methoden und Konstanten verfügen und es einem Anwendungsserver ermöglichen, einen Proxy der Klasse zu erstellen. Behandelt außerdem Unterstützungen für die java.sql.Wrapper\-Schnittstelle.|  
  
## Siehe auch  
 [Übersicht über den JDBC-Treiber](../content/Overview-of-the-JDBC-Driver.md)  
  
  