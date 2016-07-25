---
title: "&#220;berpr&#252;fen der Benutzereingabe"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8aa867b0-e6f0-49eb-93d3-817ae2ed8f77
caps.latest.revision: 11
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
# &#220;berpr&#252;fen der Benutzereingabe
  Wenn Sie eine Anwendung erstellen, die auf Daten zugreift, sollten Sie davon ausgehen, dass alle Benutzereingaben böswillig sind, solange nicht das Gegenteil bewiesen ist. Andernfalls ist die Anwendung anfällig für Angriffe. Eine Art von möglichen Angriffen wird als SQL Injection bezeichnet. Dabei wird böswilliger Code an Zeichenfolgen angefügt, die später an eine Instanz von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] übergeben und dann analysiert und ausgeführt werden. Zum Verhindern solcher Angriffe sollten Sie, wenn möglich, gespeicherte Prozeduren mit Parametern verwenden und Benutzereingaben immer überprüfen.  
  
 Das Überprüfen von Benutzereingaben im Clientcode ist wichtig, damit Sie keine Roundtrips zum Server verschwenden. Es ist von genauso großer Wichtigkeit, Parameter für gespeicherte Prozeduren auf dem Server zu überprüfen, um Eingaben abzufangen, die ungültig sind und die clientseitige Überprüfung umgehen.  
  
 Weitere Informationen zu SQL Injection und Möglichkeiten, dies zu verhindern, finden Sie unter "SQL Injection" in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation. Weitere Informationen zum Überprüfen von Parametern für gespeicherte Prozeduren finden Sie unter "Gespeicherte Prozeduren \([!INCLUDE[ssDE](../content/includes/ssDE_md.md)]\)" und den untergeordneten Themen in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation.  
  
## Siehe auch  
 [Sichern von JDBC-Treiberanwendungen](../content/Securing-JDBC-Driver-Applications.md)  
  
  