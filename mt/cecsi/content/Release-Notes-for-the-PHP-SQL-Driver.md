---
title: "Versionshinweise f&#252;r den PHP-SQL-Treiber"
ms.custom: na
ms.date: 07/18/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 91cca3d2-ba99-4a6d-b0de-beb9699cb3f8
caps.latest.revision: 36
caps.handback.revision: 34
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
  - zh-cn
  - zh-tw
---
# Versionshinweise f&#252;r den PHP-SQL-Treiber
Dieses Thema erläutert Neuheiten, die in den Versionen 3.2, 3.1, 3.0 und 2.0 von der [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt wurden.  
  
## Neuerungen in Version 3.2  
Unterstützung für PHP 5.6  
  
Enthält die neuesten Updates für vorherige PHP-Versionen 5.5 und 5.4  
  
Erfordert Microsoft ODBC Driver 11 \(oder höher\) für SQL Server  
  
## Neuerungen in Version 3.1  
Unterstützung für PHP 5.5  
  
Erfordert Microsoft ODBC Driver 11 for SQL Server \(oder höher\). Frühere Versionen benötigten SQL Native Client.  
  
## Neuerungen in Version 3.0  
Unterstützung für PHP 5.4  PHP 5.2 wird in Version 3 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]nicht unterstützt.  
  
Verbindungsoption AttachDBFileName wurde hinzugefügt. Weitere Informationen finden Sie unter [Connection Options](../content/Connection-Options.md).  
  
Unterstützung für LocalDB, (ab [!INCLUDE[ssSQL11](../content/includes/ssSQL11_md.md)]). Weitere Informationen finden Sie unter [PHP Driver for SQL Server Support for LocalDB](../Topic/PHP%20Driver%20for%20SQL%20Server%20Support%20for%20LocalDB.md).  
  
Verbindungsoption AttachDBFileName wurde hinzugefügt. Weitere Informationen finden Sie unter [Connection Options](../content/Connection-Options.md).  
  
Unterstützung für hohe Verfügbarkeit bei Notfallwiederherstellung Weitere Informationen finden Sie unter [PHP Driver for SQL Server Support for High Availability, Disaster Recovery](../Topic/PHP%20Driver%20for%20SQL%20Server%20Support%20for%20High%20Availability,%20Disaster%20Recovery.md) (Unterstützung für hohe Verfügbarkeit im PHP-Treiber für SQL Server, Notfallwiederherstellung).  
  
Unterstützung für clientseitige Cursor \(Zwischenspeichern eines Resultsets im\-Arbeitsspeicher\). Weitere Informationen finden Sie unter [Cursortypen &#40;SQLSRV-Treiber&#41;](../Topic/Cursor%20Types%20(SQLSRV%20Driver).md) und [Cursortypen &#40;PDO_SQLSRV-Treiber&#41;](../Topic/Cursor%20Types%20(PDO_SQLSRV%20Driver).md).  
  
Das PDO::ATTR\_EMULATE\_PREPARES-Attribut wurde hinzugefügt.  Weitere Informationen finden Sie unter [PDO::prepare](../Topic/PDO::prepare.md) .  
  
## Neuerungen in Version 2.0  
In Version 2.0 wurde Unterstützung für den PDO\_SQLSRV-Treiber hinzugefügt. Weitere Informationen finden Sie in der [PDO_SQLSRV-Treiberreferenz](../content/PDO_SQLSRV-Driver-Reference.md).  
  
## Siehe auch  
[Übersicht zum PHP-SQL-Treiber](../content/Overview-of-the-PHP-SQL-Driver.md)
  
