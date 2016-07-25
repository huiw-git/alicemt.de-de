---
title: "Verwenden von Anweisungen mit gespeicherten Prozeduren"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0041f9e1-09b6-4487-b052-afd636c8e89a
caps.latest.revision: 20
caps.handback.revision: 19
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
# Verwenden von Anweisungen mit gespeicherten Prozeduren
  Bei einer gespeicherten Prozedur handelt es sich um eine Datenbankprozedur, ähnlich einer Prozedur in anderen Programmiersprachen, die in der eigentlichen Datenbank enthalten ist. In [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] können gespeicherte Prozeduren mit [!INCLUDE[tsql](../content/includes/tsql_md.md)] oder mit der Common Language Runtime \(CLR\) und einer der Visual Studio 2005\-Programmiersprachen wie Visual Basic oder C\# erstellt werden. Im Allgemeinen weisen gespeicherte [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Prozeduren die folgenden Merkmale auf:  
  
-   Annehmen von Eingabeparametern und Zurückgeben mehrerer Werte in Form von Ausgabeparametern an die aufrufende Prozedur oder den aufrufenden Batch.  
  
-   Aufnehmen von Programmierungsanweisungen, die Operationen in der Datenbank ausführen, einschließlich des Aufrufens anderer Prozeduren.  
  
-   Zurückgeben eines Statuswertes an eine aufrufende Prozedur oder einen aufrufenden Batch, der Erfolg oder Fehlschlagen \(sowie die Ursache für das Fehlschlagen\) anzeigt.  
  
> [!NOTE]  
>  Weitere Informationen zu gespeicherten [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Prozeduren finden Sie unter "Grundlegendes zu gespeicherten Prozeduren" in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation.  
  
 Zum Verarbeiten von Daten in einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank mit einer gespeicherten Prozedur verfügt [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] über die Klassen [SQLServerStatement](../content/SQLServerStatement-Class.md), [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md) und [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md). Welche Klasse verwendet wird, hängt davon ab, ob von der gespeicherten Prozedur IN\- \(Eingabe\) oder OUT\-Parameter \(Ausgabe\) benötigt werden. Wenn die gespeicherte Prozedur keine IN\- oder OUT\-Parameter benötigt, können Sie die SQLServerStatement\-Klasse verwenden. Wenn die gespeicherte Prozedur mehrmals aufgerufen wird oder nur IN\-Parameter benötigt, können Sie die SQLServerPreparedStatement\-Klasse verwenden. Wenn die gespeicherte Prozedur IN\- und OUT\-Parameter benötigt, müssen Sie die SQLServerCallableStatement\-Klasse verwenden. Nur in dem Fall, dass die gespeicherte Prozedur OUT\-Parameter benötigt, müssen Sie die relativ aufwendige Verwendung der SQLServerCallableStatement\-Klasse in Kauf nehmen.  
  
> [!NOTE]  
>  Gespeicherte Prozeduren können auch Updatezählungen und mehrere Resultsets zurückgeben. Weitere Informationen finden Sie unter [Verwenden von gespeicherten Prozeduren mit einer Updatezählung](../content/Using-a-Stored-Procedure-with-an-Update-Count.md) und [Verwenden von mehreren Resultsets](../content/Using-Multiple-Result-Sets.md).  
  
 Wenn Sie den JDBC\-Treiber verwenden, um eine gespeicherte Prozedur mit Parametern aufzurufen, müssen Sie die `call` \-SQL\-Escapesequenz zusammen mit der [prepareCall](../content/prepareCall-Method--SQLServerConnection-.md)\-Methode der [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Klasse verwenden. Die vollständige Syntax für die `call` \-Escapesequenz lautet wie folgt:  
  
 `{[?=]call procedure-name[([parameter][,[parameter]]...)]}`  
  
> [!NOTE]  
>  Weitere Informationen zur `call` \-Escapesequenz und anderen SQL\-Escapesequenzen finden Sie unter [Verwenden von SQL-Escapesequenzen](../content/Using-SQL-Escape-Sequences.md).  
  
 Die Themen in diesem Abschnitt beschreiben, wie Sie gespeicherte [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Prozeduren mit dem JDBC\-Treiber und der `call` \-SQL\-Escapesequenz aufrufen können.  
  
## In diesem Abschnitt  
  
|Thema|Beschreibung|  
|-----------|------------------|  
|[Verwenden von gespeicherten Prozeduren ohne Parameter](../content/Using-a-Stored-Procedure-with-No-Parameters.md)|Beschreibt die Verwendung des JDBC\-Treibers zum Ausführen von gespeicherten Prozeduren, die keine Eingabe\- oder Ausgabeparameter enthalten.|  
|[Verwenden von gespeicherten Prozeduren mit Eingabeparametern](../content/Using-a-Stored-Procedure-with-Input-Parameters.md)|Beschreibt die Verwendung des JDBC\-Treibers zum Ausführen von gespeicherten Prozeduren, die Eingabeparameter enthalten.|  
|[Verwenden von gespeicherten Prozeduren mit Ausgabeparametern](../content/Using-a-Stored-Procedure-with-Output-Parameters.md)|Beschreibt die Verwendung des JDBC\-Treibers zum Ausführen von gespeicherten Prozeduren, die Ausgabeparameter enthalten.|  
|[Verwenden von gespeicherten Prozeduren mit einem Rückgabestatus](../content/Using-a-Stored-Procedure-with-a-Return-Status.md)|Beschreibt die Verwendung des JDBC\-Treibers zum Ausführen von gespeicherten Prozeduren, die Rückgabestatuswerte enthalten.|  
|[Verwenden von gespeicherten Prozeduren mit einer Updatezählung](../content/Using-a-Stored-Procedure-with-an-Update-Count.md)|Beschreibt die Verwendung des JDBC\-Treibers zum Ausführen von gespeicherten Prozeduren, die Updatezählungen enthalten.|  
  
## Siehe auch  
 [Verwenden von Anweisungen mit dem JDBC-Treiber](../content/Using-Statements-with-the-JDBC-Driver.md)  
  
  