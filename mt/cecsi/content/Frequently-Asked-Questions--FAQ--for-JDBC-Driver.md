---
title: "H&#228;ufig gestellte Fragen (FAQ)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cbc0e397-ecf2-4494-87b2-a492609bceae
caps.latest.revision: 7
caps.handback.revision: 5
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
# H&#228;ufig gestellte Fragen (FAQ)
  Dieser Artikel enthält Antworten auf häufig gestellte Fragen zu Microsoft JDBC Driver for SQL Server.  
  
## Häufig gestellte Fragen  
 Welche Versionen von SQL Server und Java werden vom Treiber unterstützt?  
 Detaillierte Informationen hierzu finden Sie auf der Seite [Supportmatrix für Microsoft JDBC Driver for SQL Server](../content/Microsoft-JDBC-Driver-for-SQL-Server-Support-Matrix.md).  
  
 Was sollte ich wissen, bevor ich meinen Treiber aktualisiere?  
 Die Treiber Microsoft JDBC Driver 6.0 \(Preview\) und 4.2 for SQL Server unterstützen sowohl die JDBC\-Spezifikationen 3.0 und 4.2 und die Installationspakete enthalten die folgenden vier JAR\-Klassenbibliotheken.  
  
||||  
|-|-|-|  
|sqljdbc42.jar|JDBC 4.2, 4.1 und 4.0|JDK 8.0, 7.0, 6.0 und 5.0|  
|sqljdbc41.jar|JDBC 4.1 und 4.0|JDK 7.0, 6.0 und 5.0|  
|sqljdbc4.jar|JDBC 4.0|JDK 6.0 und 5.0|  
|sqljdbc.jar|JDBC 3.0|JDK 6.0 und 5.0|  
  
 Der Treiber Microsoft JDBC Driver 4.1 for SQL unterstützt sowohl die JDBC\-Spezifikationen 3.0 und 4.0 und das Installationspaket enthält die folgenden drei JAR\-Klassenbibliotheken.  
  
||||  
|-|-|-|  
|sqljdbc41.jar|JDBC 4.0|JDK 7.0, 6.0 und 5.0|  
|sqljdbc4.jar|JDBC 4.0|JDK 6.0 und 5.0|  
|sqljdbc.jar|JDBC 3.0|JDK 6.0 und 5.0|  
  
 Der Treiber Microsoft JDBC Driver 4.0 for SQL unterstützt sowohl die JDBC\-Spezifikationen 3.0 und 4.0 und das Installationspaket enthält die folgenden zwei JAR\-Klassenbibliotheken: sqljdbc.jar und sqljdbc4.jar.  
  
||||  
|-|-|-|  
|sqljdbc4.jar|JDBC 4.0|JDK 6.0 und 5.0|  
|sqljdbc.jar|JDBC 3.0|JDK 6.0 und 5.0|  
  
 Muss ich Änderungen am Code meiner Anwendung vornehmen, um den neuesten Treiber mit meiner bestehenden Version von SQL Server verwenden zu können?  
 In der Regel entwerfen wir den Treiber abwärtskompatibel , sodass Sie Ihre vorhandenen Anwendungen bei einer Treiberaktualisierung nicht anpassen müssen. Führt eine neue Treiberversion eine erhebliche Änderung ein, enthält der Abschnitt [Neues im JDBC-Treiber](../content/What-s-New-in-the-JDBC-Driver.md) detaillierte Informationen zu dieser Änderung und zu ihren Auswirkungen auf bestehende Anwendungen. Darüber hinaus finden Sie in den Versionsanmerkungen des Treibers eine Liste bekannter Probleme und der in diesem Release behobenen Fehler.  
  
 Wie viel kostet der Treiber?  
 Microsoft JDBC Driver for SQL steht Ihnen kostenlos zur Verfügung.  
  
 Kann ich den Treiber weitervertreiben?  
 Sie können den Treiber unter einer separaten Weitervertreibungslizenz beliebig weitervertreiben. Für diese ist eine Registrierung notwendig. Informationen zur Registrierung finden Sie auf der Seite [Weitervertreiben des Microsoft JDBC-Treibers](../content/Redistributing-the-Microsoft-JDBC-Driver.md).  
  
 Kann ich mithilfe des Treibers von einem Linuxcomputer auf Microsoft SQL Server zugreifen?  
 Ja\! Sie können den Treiber verwenden, um von Linux, Unix und anderen nicht\-Windows\-Plattformen auf SQL Server zuzugreifen. Weitere Informationen finden Sie unter [Supportmatrix für Microsoft JDBC Driver for SQL Server](../content/Microsoft-JDBC-Driver-for-SQL-Server-Support-Matrix.md).  
  
 Unterstützt der Treiber die Secure Sockets Layer\-Verschlüsselung \(SSL\)?  
 Die SSL\-Verschlüsselung wird seit Version 1.2 des Treibers unterstützt. Weitere Informationen finden Sie unter [Verwenden der SSL-Verschlüsselung](../content/Using-SSL-Encryption.md).  
  
 Welche Authentifizierungstypen werden von Microsoft JDBC Driver for SQL Server unterstützt?  
 Die verfügbaren Authentifizierungsoptionen sind in der folgenden Tabelle aufgelistet. Beachten Sie, dass die reine Java Kerberos\-Authentifizierung seit Version 4.0 des Treibers verfügbar ist.  
  
|||  
|-|-|  
|Platform|Authentifizierung|  
|Nicht\-Windows\-System|Reine Java Kerberos|  
|Nicht\-Windows\-System|SQL Server|  
|Windows|Reine Java Kerberos|  
|Windows|SQL Server|  
|Windows|Kerberos mit NTLM als Backup|  
|Windows|NTLM|  
  
 Unterstützt der Treiber Internetadressen des Typs Internet Protokoll, Version 6 \(IPv6\)?  
 Ja, der JDBC\-Treiber unterstützt die Verwendung von IPv6\-Adressen in der Liste der Verbindungseigenschaften und in der Eigenschaft „serverName“ der Verbindungszeichenfolge. Weitere Informationen finden Sie unter [Erstellen der Verbindungs-URL](../content/Building-the-Connection-URL.md).  
  
 Was ist die adaptive Pufferung?  
 Die adaptive Pufferung wurde in Version 1.2 des JDBC\-Treibers für Microsoft SQL Server 2005 eingeführt, um beliebige umfangreiche Daten ohne Verwendung von Servercursorn abzurufen und den damit einhergehenden Overhead zu vermeiden. Die adaptive Pufferung des Microsoft SQL Server JDBC Drivers stellt mit „responseBuffering“ eine Eigenschaft für Verbindungszeichenfolgen bereit, die auf „adaptive“ oder „full“ festgelegt werden kann. Ab Version 2.0 des JDBC\-Treibers ist das Standardverhalten des Treibers „adaptive“. Dies bedeutet, um das Verhalten der adaptiven Pufferung zu verwenden, muss das Verhalten der adaptiven Pufferung in der Anwendung nicht explizit angefordert werden. In Version 1.2 lautete der Puffermodus jedoch standardmäßig „full“, und die Anwendung musste den Modus für die adaptive Pufferung explizit anfordern. Weitere Informationen finden Sie im Thema [Verwenden der adaptiven Pufferung](../content/Using-Adaptive-Buffering.md) und im Blogartikel [Was ist adaptives Response\-Buffering und warum sollte ich es benutzen?](http://go.microsoft.com/fwlink/?LinkId=111575).  
  
 Unterstützt der Treiber Verbindungspooling?  
 Der Treiber unterstützt das Verbindungspooling unter Java Platform, Enterprise Edition 5 \(Java EE 5\). Der Treiber implementiert die erforderlichen JDBC 3.0\-Schnittstellen, damit er implementiertes Verbindungspooling von Anbietern für Anwendungsserver auf Middleware\-Ebene nutzen kann. Der Treiber nutzt in diesen Umgebungen Verbindungspool. Weitere Informationen finden Sie unter [Verwenden von Verbindungspools](../content/Using-Connection-Pooling.md). Der Treiber bietet keine eigene Implementierung des Poolings, sondern es beruht auf Java\-Anwendungsservern von Drittanbietern.  
  
 Wird für den Treiber Support geleistet?  
 Es sind zahlreiche Optionen verfügbar. Sie können Ihre Frage in unseren [Foren](http://go.microsoft.com/fwlink/?LinkID=246673) an Microsoft, MVPs \(Microsoft Most Valuable Professionals\) und die Community richten. Sie können sich auch an den Microsoft Kundendienst wenden. Hierbei kann es erforderlich sein, dass Sie das Problem außerhalb einer Drittanbieteranwendung reproduzieren. Wenn das Problem nicht außerhalb der Umgebung des hostenden Java Containers reproduziert werden kann, müssen Sie den Drittanbieter hinzuziehen, damit wir Ihnen weiterhin helfen können. Zusätzlich kann es für die optimale Hilfe nötig sein, dass Sie Ihr Problem auf einem Betriebssystem, wie z. B. Windows, reproduzieren.  
  
 Ist der Treiber für die Verwendung mit Drittanbieter\-Anwendungsservern zertifiziert?  
 Der Treiber wurde mit allen wichtigen Anwendungsserver getestet, wie z. B. IBM WebSphere und SAP NetWeaver.  
  
 Wie aktiviere ich die Ablaufverfolgung?  
 Der Treiber unterstützt die Verwendung der Ablaufverfolgung \(oder Protokollierung\). Dies hilft Probleme zu lösen, die bei der Verwendung des JDBC\-Treibers in Ihrer Anwendung auftreten können. Der JDBC\-Treiber verwendet die Logging\-API in java.util.logging, um die clientseitige JAR\-Ablaufverfolgung zu aktivieren. Weitere Informationen finden Sie unter [Ablaufverfolgung für Treibervorgänge](../content/Tracing-Driver-Operation.md). Weitere Informationen zur serverseitigen XA\-Ablaufverfolgung finden Sie unter [Verfolgung des Datenzugriffs in SQL Server](http://go.microsoft.com/fwlink/?LinkId=248705).  
  
 Wo kann ich ältere Versionen des Treibers, z. B. SQL Server 2000\-JDBC\-Treiber, 2005\-Treiber, 1.0, 1.1 oder 1.2 herunterladen?  
 Diese Treiberversionen stehen nicht zum Download zur Verfügung, da sie nicht mehr unterstützt werden. Wir arbeiten laufend daran, unsere Unterstützung von Java\-Konnektivität zu verbessern. Daher raten wir dringend zur Verwendung unseres aktuellsten JDBC\-Treibers.  
  
 Ich verwende JRE 1.4. Welcher Treiber ist mit JRE 1.4 kompatibel?  
 Kunden, die SAP\-Produkte verwenden und die Unterstützung für JRE 14. benötigen, können [SAP Service Marketplace](http://service.sap.com/) um den Treiber Microsoft JDBC Driver 1.2 zu erhalten.  
  
 Kann der Treiber mit FIPS\-validierten Algorithmen kommunizieren?  
 Der Microsoft JDBC\-Treiber enthält keine kryptografischen Algorithmen. Wenn ein Kunde Algorithmen für Betriebssysteme, Anwendungen und JVM verwendet, die entsprechend der Federal Information Processing Standards \(FIPS\) zulässig sind, und er den Treiber für diese Algorithmen konfiguriert, so wird dieser für die Kommunikation nur die festgelegten Algorithmen verwenden.  
  
  