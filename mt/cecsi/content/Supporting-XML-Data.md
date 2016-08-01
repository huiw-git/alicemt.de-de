---
title: "Unterst&#252;tzen von XML-Daten"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 32b7217e-1f0c-473d-9a45-176daa81584e
caps.latest.revision: 26
caps.handback.revision: 25
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
# Unterst&#252;tzen von XML-Daten
  [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] umfasst einen **xml**\-Datentyp, mit dem Sie XML\-Dokumente und \-Fragmente in einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank speichern können. Der **xml**\-Datentyp ist ein integrierter Datentyp in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] und ähnelt in gewisser Weise anderen integrierten Typen wie **int** und **varchar**. Wie andere integrierte Typen können Sie den **xml**\-Datentyp beim Erstellen einer Tabelle als Spaltentyp, als Variablentyp, als Parametertyp oder als Funktionsrückgabetyp bzw. in [!INCLUDE[tsql](../content/includes/tsql_md.md)] CAST\- und CONVERT\-Funktionen verwenden. Im JDBC\-Treiber kann der **xml**\-Datentyp als Zeichenfolge\-, Bytearray\-, Datenstrom\-, CLOB\-, BLOB\- oder SQLXML\-Objekt zugeordnet werden. Die Standardzuordnung ist als Zeichenfolge.  
  
 Der JDBC\-Treiber bietet Unterstützung für die JDBC 4.0\-API, in der die SQLXML\-Schnittstelle eingeführt wird. Die SQLXML\-Schnittstelle definiert Methoden für die Interaktion mit und die Bearbeitung von XML\-Daten.**SQLXML** ist ein JDBC 4.0\-Datentyp und ist dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]**xml**\-Datentyp zugeordnet. Um den SQLXML\-Datentyp in der Anwendung verwenden zu können, müssen Sie daher den Klassenpfad so festlegen, dass die Datei „sqljdbc4.jar“ enthalten ist. Wenn die Anwendung beim Zugriff auf das SQLXML\-Objekt und seine Methoden versucht, „sqljdbc3.jar“ zu verwenden, wird eine Ausnahme ausgelöst.  
  
> [!IMPORTANT]  
>  Die XML\-Daten werden von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] immer überprüft, bevor sie in der Datenbankspalte gespeichert werden. Anwendungen können den **SQLXML**\-Datentyp verwenden, da er vom JDBC\-Treiber automatisch dem **xml**\-Datentyp zugeordnet wird. Die **SQLXML**\-Unterstützung wird durch „sqljdbc4.jar“ bereitgestellt. Eine Liste der vom [Systemanforderungen für den JDBC-Treiber](../content/System-Requirements-for-the-JDBC-Driver.md) unterstützten JRE\-Versionen finden Sie unter [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)].  
  
 Die Themen in diesem Abschnitt beschreiben die SQLXML\-Schnittstelle und die Programmierung für den **SQLXML**\-Datentyp mit den Methoden der JDBC\-API.  
  
## In diesem Abschnitt  
  
|Thema|Beschreibung|  
|-----------|------------------|  
|[SQLXML-Schnittstelle](../content/SQLXML-Interface.md)|Beschreibt die SQLXML\-Schnittstelle und ihre Methoden.|  
|[Programmieren mit SQLXML](../content/Programming-with-SQLXML.md)|Beschreibt, wie mithilfe der API\-Methoden von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] XML\-Daten mit dem Java\-Datentyp **SQLXML** in einer relationalen Datenbank gespeichert bzw. aus einer relationalen Datenbank abgerufen werden. Außerdem sind Informationen über die Typen von SQLXML\-Objekten und eine Liste wichtiger Richtlinien und Einschränkungen für die Verwendung von SQLXML\-Objekten enthalten.|  
  
## Siehe auch  
 [Grundlegendes zu den Datentypen in JDBC Driver](../content/Understanding-the-JDBC-Driver-Data-Types.md)  
  
  