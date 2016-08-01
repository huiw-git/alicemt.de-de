---
title: "Verwenden von Parametermetadaten"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: db2c1957-91c6-4989-a07b-9f8be6d2033a
caps.latest.revision: 17
caps.handback.revision: 13
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
# Verwenden von Parametermetadaten
  Für die Abfrage der enthaltenen Parameter bei [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\- oder [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Objekten ist in [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] die [SQLServerParameterMetaData](../content/SQLServerParameterMetaData-Class.md)\-Klasse implementiert. Diese Klasse enthält eine Vielzahl von Feldern und Methoden, die Informationen in der Form eines einzelnen Werts zurückgeben.  
  
 Um ein SQLServerParameterMetaData\-Objekt zu erstellen, können Sie die[getParameterMetaData](../content/getParameterMetaData-Method--SQLServerPreparedStatement-.md)\-Methoden der SQLServerPreparedStatement\-Klasse und SQLServerCallableStatement\-Klasse verwenden.  
  
 Im folgenden Beispiel werden eine offene Verbindung zur [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)][!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank an die Funktion übergeben, mit der getParameterMetaData\-Methode der SQLServerCallableStatement\-Klasse ein SQLServerParameterMetaData\-Objekt zurückgegeben und dann mit den verschiedenen Methoden des SQLServerParameterMetaData\-Objekts Informationen zu Typ und Modus der Parameter angezeigt, die in der gespeicherten Prozedur „HumanResources.uspUpdateEmployeeHireInfo“ enthalten sind.  
  
 [!CODE [JDBC#UsingParamMetaData1](../CodeSnippet/SQLDrivers/jdbc#usingparammetadata1)]  
  
> [!NOTE]  
>  Wenn die SQLServerParameterMetaData\-Klasse mit vorbereiteten Anweisungen verwendet wird, gibt es einige Einschränkungen. Mit SQL Server 2008 oder 2008 R2 unterstützt der JDBC\-Treiber SELECT\-, DELETE\-, INSERT\- und UPDATE\-Anweisungen. Diese Anweisungen dürfen jedoch keine Unterabfragen enthalten. Auch MERGE\-Abfragen werden bei SQL Server 2008 oder 2008 R2 nicht für die SQLServerParameterMetaData\-Klasse unterstützt. Bei SQL Server 2012 und höheren werden Parametermetadaten in komplexen Abfragen unterstützt.  
  
## Siehe auch  
 [Verarbeiten von Metadaten mit dem JDBC-Treiber](../content/Handling-Metadata-with-the-JDBC-Driver.md)  
  
  