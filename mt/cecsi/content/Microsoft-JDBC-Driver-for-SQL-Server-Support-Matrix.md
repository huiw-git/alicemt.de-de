---
title: "Supportmatrix f&#252;r Microsoft JDBC Driver for SQL Server"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c5769e67-99f7-4bc1-a4fa-8941dad33d35
caps.latest.revision: 10
caps.handback.revision: 7
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
# Supportmatrix f&#252;r Microsoft JDBC Driver for SQL Server
  Auf dieser Seite finden Sie die Unterstützungsmatrix und die Support Lifecycle\-Richtlinie für Microsoft JDBC Driver for SQL Server.  
  
## Unterstützungsmatrix und Support Lifecycle\-Richtlinie für Microsoft JDBC\-Treiber  
 Die Microsoft Support Lifecycle\-Richtlinie \(MLS\) bietet transparente, vorhersagbare Informationen hinsichtlich der Supportdauer bei Microsoft\-Produkten. Für die Versionen 3.0 und 4.x des JDBC\-Treibers wird ab dem Veröffentlichungsdatum fünf Jahre grundlegender Support \(Mainstream\-Support\) geleistet. Die Definition für Mainstream\-Support finden Sie auf der Website der Microsoft Support Lifecycle\-Richtlinie.  
  
 Erweiterte und benutzerdefinierte Support\-Optionen sind für den Microsoft JDBC\-Treiber nicht verfügbar.  
  
 Die folgenden Microsoft JDBC\-Treiber sind als Preview verfügbar.  
  
||||  
|-|-|-|  
|Treibername|Treiberversion|Supportende|  
|Microsoft JDBC Driver 6.0 \(Preview\) for SQL Server|6.0|TBD|  
  
 Die folgenden Microsoft JDBC\-Treiber werden bis zum angegebenen Supportende unterstützt.  
  
||||  
|-|-|-|  
|Treibername|Treiberversion|Supportende|  
|Microsoft JDBC Driver 4.2 for SQL Server|4.2|24. August 2020|  
|Microsoft JDBC Driver 4.1 for SQL Server|4.1|12. Dezember 2019|  
|Microsoft JDBC\-Treiber 4.0 für SQL Server|4.0|6. März 2017|  
  
 Die folgenden Microsoft JDBC\-Treiber werden nicht länger unterstützt.  
  
||||  
|-|-|-|  
|Treibername|Treiberversion|Supportende|  
|Microsoft SQL Server JDBC Driver 3.0|3.0|23. April 2015|  
|Microsoft SQL Server JDBC Driver 2.2|2.0|31. Dezember 2012|  
|Microsoft SQL Server 2005 JDBC Driver 1.2|1.2|25. Juni 2011|  
|Microsoft SQL Server 2005 JDBC Driver 1.1|1.1|25. Juni 2011|  
|Microsoft SQL Server 2005 JDBC Driver 1.0|1,0|25. Juni 2011|  
|Microsoft SQL Server 2000 JDBC Driver|2000|9. Juli 2010|  
  
## SQL\-Versionskompatibilität  
  
|||||||||||  
|-|-|-|-|-|-|-|-|-|-|  
|Treiberversion|SQL Server 2000|SQL Server 2005|SQL Server 2008|SQL Server 2008R2|SQL Server 2012|Azure SQL\-Datenbank|PDW 2008R2 AU3<sup>4</sup>|SQL Server 2014|SQL Server 2016 \(Preview\)|  
|6.0|N|J|J|J|J|J|J|J|J|  
|4.2|N|N|J|J|J|J|J|J|J|  
|4.1|N|N|J|J|J|J|J|J|J|  
|4.0|N|J|J|J|J|J|J|J|J|  
|3.0|J|J|J|J|J<sup>1</sup>|J<sup>2</sup>|N|J<sup>5</sup>|N|  
|2.0|J|J|J<sup>3</sup>|J<sup>3</sup>|N|N|N|N|N|  
|1.2|J|J|J<sup>3</sup>|N|N|N|N|N|N|  
|1.1|J|J|N|N|N|N|N|N|N|  
|1,0|J|J|N|N|N|N|N|N|N|  
|2000|J|N|N|N|N|N|N|N|N|  
  
 <sup>1</sup>Die Version 3.0 des Treibers Microsoft SQL Server JDBC Driver kann sich als kompatibler Client mit SQL Server 2012 verbinden.  
  
 <sup>2</sup>Die Unterstützung für Azure SQL\-Datenbank wurde in Version 3.0 als Hotfix eingeführt. Es wird empfohlen, dass Azure SQL\-Datenbank\-Kunden die neuesten Treiber verwenden.  
  
 <sup>3</sup>Die Version 2.0 des Treibers Microsoft SQL Server JDBC Driver und die Version 2.1 des Treibers Microsoft SQL Server 2005 JDBC kann als Client eine abwärtskompatible Verbindung mit SQL Server 2008 herstellen. Sind abwärtskompatible Konvertierungen erlaubt, kann die Anwendung Abfragen ausführen und Aktualisierungen auf die neuen Datentypen von SQL Server 2008 durchführen, wie z. B. „time“, „date“, „datetime2“, „datetimeoffset“ und FILESTREAM. Weitere Informationen zur Verwendung dieser neuen Datentypen mit dem JDBC\-Treiber finden Sie unter [Verwenden der Date\/Time\-Datentypen in SQL Server 2008 mithilfe eines JDBC\-Treibers](http://go.microsoft.com/fwlink/?LinkId=145198) und unter [Verwenden von Filestream in SQL Server 2008 mithilfe eines JDBC\-Treibers](http://go.microsoft.com/fwlink/?LinkId=145199). Weitere Informationen zur Abwärtskompatibilität dieser neuen Datentypen finden Sie in den Themen [Verwenden von Datums\- und Zeitdaten](http://go.microsoft.com/fwlink/?LinkId=145211)und [FILESTREAM\-Unterstützung](http://go.microsoft.com/fwlink/?LinkId=145212) in der SQL Server\-Onlinedokumentation  
  
 <sup>4</sup>Die Unterstützung von Verbindungen zwischen dem Microsoft JDBC\-Treiber und Parallel Data Warehouse wurde erstmals in Microsoft JDBC Driver 4.0 for SQL Server und in Microsoft SQL Server 2008 R2 Parallel Data Warehouse Appliance Update 3 bereitgestellt.  
  
 <sup>5</sup>Die Version 3.0 des Treibers Microsoft SQL Server JDBC Driver kann sich als kompatibler Client mit SQL Server 2014 verbinden.  
  
## Unterstützung der Java\- und JDBC\-Spezifikation  
  
||||  
|-|-|-|  
|Version des JDCB\-Treibers|JRE\-Version|JDBC\-API\-Version|  
|6.0|1.5, 1.6, 1.7, 1.8|3.0, 4.0, 4.1, 4.2|  
|4.2|1.5, 1.6, 1.7, 1.8|3.0, 4.0, 4.1, 4.2|  
|4.1|1.5, 1.6, 1.7|3.0, 4.0|  
|4.0|1.5, 1.6, 1.7|3.0, 4.0|  
|3.0|1.5, 1.6,|3.0, 4.0|  
|2.0|1.5, 1.6|3.0, 4.0|  
|1.2|1.4, 1.5, 1.6|3.0|  
|1.1|1.4|3.0|  
|1,0|1.4|3.0|  
|2000|1.4|3.0|  
  
## Unterstützte Betriebssysteme  
 Der JDBC\-Treiber ist für die Verwendung mit allen Betriebssystemen konzipiert, die die Java Virtual Machine \(JVM\) unterstützen. Einige weitverbreitete Plattformen enthalten Windows 10, Windows 8.1, Windows 8, Windows 7, Windows Server 2008 R2, Windows Vista, Linux, Unix, AIX, Mac OS und andere.  
  
 Das JDBC\-Produktteam testet unsern Treiber unter Windows, Sun Solaris, SUSE Linux und RedHat Linux.  Der Kundendienst steht dem Kunden auf allen Plattformen zur Verfügung. Jedoch kann es vorkommen, dass Sie gebeten werden, Ihr Problem auf einer anderen Plattform, z. B. auf Windows, zu reproduzieren.  
  
## Support für Anwendungsserver  
 Der Microsoft JDBC\-Treiber für SQL Server wird mit verschiedenen Anwendungsservern getestet.  Wenden Sie sich an den Anbieter Ihres Anwendungsserver, um detaillierte Informationen über die zu seinem Produkt kompatible Treiberversion zu erhalten.  
  
  