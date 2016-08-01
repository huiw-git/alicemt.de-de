---
title: "Unterst&#252;tzung f&#252;r nationale Zeichens&#228;tze"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4fceacfd-df4f-40cd-b7a2-5e5e58a5979f
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
# Unterst&#252;tzung f&#252;r nationale Zeichens&#228;tze
  Der JDBC\-Treiber bietet Unterstützung für die JDBC 4.0\-API, die neue API\-Methoden für die Konvertierung nationaler Zeichensätze enthält. Teil dieser Unterstützung sind neue Methoden zum Festlegen, Abrufen und Aktualisieren der JDBC\-Typen **NCHAR**, **NVARCHAR**, **LONGNVARCHAR** und **NCLOB**.  
  
 In der folgenden Liste sind die Methoden zum Abrufen, Festlegen und Aktualisieren für die Unterstützung der Konvertierung nationaler Zeichensätze aufgeführt:  
  
-   [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md): [setNString](../content/setNString-Method--int--java.lang.String-.md), [setNCharacterStream](../content/setNCharacterStream-Method--SQLServerPreparedStatement-.md), [setNClob](../content/setNClob-Method--SQLServerPreparedStatement-.md).  
  
-   [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md): [getNClob](../content/getNClob-Method--SQLServerCallableStatement-.md), [getNString](../content/getNString-Method--SQLServerCallableStatement-.md), [getNCharacterStream](../content/getNCharacterStream-Method--SQLServerCallableStatement-.md), [setNString](../content/setNString-Method--SQLServerCallableStatement-.md), [setNCharacterStream](../content/setNCharacterStream-Method--SQLServerCallableStatement-.md), [setNClob](../content/setNClob-Method--SQLServerCallableStatement-.md).  
  
-   [SQLServerResultSet](../content/SQLServerResultSet-Class.md): [getNClob](../content/getNClob-Method--SQLServerResultSet-.md), [getNString](../content/getNString-Method--SQLServerResultSet-.md), [getNCharacterStream](../content/getNCharacterStream-Method--SQLServerResultSet-.md), [updateNClob](../content/updateNClob-Method--SQLServerResultSet-.md), [updateNString](../content/updateNString-Method--SQLServerResultSet-.md), [updateNCharacterStream](../content/updateNCharacterStream-Method--SQLServerResultSet-.md).  
  
> [!NOTE]  
>  Um diese Methoden in einer Anwendung verwenden zu können, müssen Sie den Klassenpfad so festlegen, dass die Datei „sqljdbc4.jar“ enthalten ist.  
  
 Damit String\-Parameter im Unicode\-Format an den Server gesendet werden, sollten die Anwendungen entweder die neuen JDBC 4.0\-Methoden für nationale Zeichensätze verwenden oder die **sendStringParametersAsUnicode**\-Verbindungseigenschaft auf "**true**" festlegen, wenn die Methoden für nicht nationale Zeichensätze verwendet werden. Es wird empfohlen, nach Möglichkeit die neuen JDBC 4.0\-Methoden für nationale Zeichensätze zu verwenden. Weitere Informationen zur **sendStringParametersAsUnicode**\-Verbindungseigenschaft finden Sie unter [Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md).  
  
## Siehe auch  
 [Grundlegendes zu den Datentypen in JDBC Driver](../content/Understanding-the-JDBC-Driver-Data-Types.md)  
  
  