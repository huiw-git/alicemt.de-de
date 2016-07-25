---
title: "Verarbeiten komplexer Anweisungen"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6b807a45-a8b5-4b1c-8b7b-d8175c710ce0
caps.latest.revision: 18
caps.handback.revision: 16
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
# Verarbeiten komplexer Anweisungen
  Bei Verwendung von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] müssen Sie u. U. komplexe Anweisungen verarbeiten, z. B. Anweisungen, die zur Laufzeit dynamisch generiert werden. Komplexe Anweisungen führen oftmals eine Vielzahl von Tasks aus, wie z. B. Update\-, Insert\- und Delete\-Operationen. Diese Anweisungstypen können auch mehrere Resultsets und Ausgabeparameter zurückgeben. In diesen Situationen kann es vorkommen, dass der Java\-Code, der die Anweisungen ausführt, die Typen und die Anzahl der zurückgegebenen Objekte und Daten zunächst nicht kennt.  
  
 Um komplexe Anweisungen effizient auszuführen, umfasst der JDBC\-Treiber eine Reihe von Methoden, um die zurückgegebenen Objekte und Daten abzufragen, damit sie in der Anwendung ordnungsgemäß verarbeitet werden können. Der Schlüssel für die Verarbeitung komplexer Anweisungen ist die [execute](../content/execute-Method--SQLServerStatement-.md)\-Methode der [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Klasse. Diese Methode gibt einen **boolean**\-Wert zurück. Ist der Wert "true", handelt es sich bei dem ersten zurückgegebenen Ergebnis der Anweisungen um ein Resultset. Ist der Wert "false", handelt es sich bei dem ersten zurückgegebenen Ergebnis um eine Updatezählung.  
  
 Wenn Sie den Typ der zurückgegebenen Objekte oder Daten kennen, können Sie diese Daten mit der [getResultSet](../content/getResultSet-Method--SQLServerStatement-.md)\-Methode bzw. der [getUpdateCount](../content/getUpdateCount-Method--SQLServerStatement-.md)\-Methode verarbeiten. Um die nächsten Objekte oder Daten zu verarbeiten, die von der komplexen Anweisung zurückgegeben werden, können Sie die [getMoreResults](../content/getMoreResults-Method---.md)\-Methode aufrufen.  
  
 Im folgenden Beispiel werden eine offene Verbindung zur [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)][!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank an die Funktion übergeben, eine komplexe Anweisung erstellt, die den Aufruf einer gespeicherten Prozedur mit einer SQL\-Anweisung kombiniert, die Anweisungen ausgeführt und dann alle zurückgegebenen Resultsets und Updatezählungen in einer `do`\-Schleife verarbeitet.  
  
 [!CODE [JDBC#HandlingComplexStatements1](../CodeSnippet/SQLDrivers/jdbc#handlingcomplexstatements1)]  
  
## Siehe auch  
 [Verwenden von Anweisungen mit dem JDBC-Treiber](../content/Using-Statements-with-the-JDBC-Driver.md)  
  
  