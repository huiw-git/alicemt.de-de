---
title: "&#196;nderungsprotokoll f&#252;r SQL Server Data Tools (SSDT)"
ms.custom: na
ms.date: 06/30/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b071f8b8-c8e5-44e0-bbb6-04804dd1863a
caps.latest.revision: 25
caps.handback.revision: 8
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
# &#196;nderungsprotokoll f&#252;r SQL Server Data Tools (SSDT)
Dieses Änderungsprotokoll bezieht sich auf [SQL Server Data Tools-Vorschau (SSDT-Vorschau) für Visual Studio 2015](https://msdn.microsoft.com/en-us/library/mt204009.aspx), das zusammen mit SQL Server 2016 Vorschau bereitgestellt wird.  
  
## SSDT\-Vorschau Januar 2016  
  
-   **SQL Server\-Projektvorlagen**  
  
    Keine Ankündigungen für diese SSDT\-Vorschauversion . Unter [Neuigkeiten im Datenbankmodul](https://msdn.microsoft.com/en-us/library/bb510411.aspx) finden Sie Informationen zu anderen Funktionen in dieser CTP\-Version.  
  
-   **SSIS\-Paket\-Projektvorlage**  
  
    Bietet Unterstützung für ODBC\-Quell\- und Zielkomponenten, einen CDC\-Steuerungstask, eine CDC\-Quell\- und \-Splitterkomponente, einen Microsoft\-Connector für SAP BW und ein Integration Services Feature Pack für Azure. Unter [Neuigkeiten in Integration Services](https://msdn.microsoft.com/en-us/library/bb522534.aspx) finden Sie weitere Details.  
  
-   **SSAS\-Projektvorlagen**  
  
    Enthält Verbesserungen für tabellarische Modelle mit Kompatibilitätsgrad 1200, berechnete Spalten und Sicherheit auf Zeilenebene für Modelle im DirectQuery\-Modus, Übersetzungen von Modellmetadaten, TMSL\-Skriptausführung in der SSIS\-Analysis Services\-Task 'DDL ausführen' und zahlreiche Programmfehlerbehebungen. Unter [Neuigkeiten in Analysis Services (MSDN)](https://msdn.microsoft.com/en-US/library/bb522628.aspx) oder [Neuigkeiten in Analysis Services (Blogbeitrag)](http://blogs.msdn.com/b/analysisservices/archive/2016/01/28/what-s-new-for-sql-server-2016-analysis-services-in-ctp3-3.aspx) finden Sie detailliertere Informationen.  
  
-   **Vorlagen für SSRS\-Berichtsprojekte**  
  
    Keine Ankündigungen für diese SSDT\-Vorschauversion . Unter [Neuigkeiten in Reporting Services](https://msdn.microsoft.com/en-us/library/ms170438.aspx) finden Sie Informationen zu anderen Funktionen in dieser CTP\-Version.  
  
## SSDT\-Vorschau Dezember 2015  
  
-   **SQL Server\-Projektvorlagen** enthalten Programmfehlerbehebungen für das Dialogfeld „Verbindung“, für aktuelle Verlaufslisten sowie für die ordnungsgemäße Verwendung von Authentifizierungskontext, der beim Laden einer Datenbank in der Verbindungseigenschaft festgelegt wird.  
  
    -   Der Timeoutwert zum Testen einer Verbindung wurde auf 15 Sekunden geändert.  
  
    -   Erstellen Sie eine Firewallregel für den Azure SQL\-Datenbankserver, wenn die Client\-IP beim Laden einer Datenbankliste nicht registriert wird.  
  
    -   SQL Server 2016 CTP3.2 bietet Unterstützung für Programmierbarkeit.  
  
-   **SSAS\-Projektvorlagen** unterstützen nun das Erstellen berechneter Tabellen anhand von DAX\-Ausdrücken und anderen Objekten, die bereits im Modell definiert sind.  
  
-   Zusätze zur  **SSIS\-Paket\-Projektvorlage** enthalten SSIS\-Hadoop\-Connector\-Unterstützung für das Avro\-Dateiformat und Kerberos\-Authentifizierung. Beachten Sie bitte, dass in diesem Update noch keine SSIS\-Designer\-Unterstützung für SSIS 2012 und 2014 enthalten ist.  
  
## SSDT\-Vorschau November 2015  
  
-   **SQL Server\-Projektvorlagen**. Vorschau der verbesserten Verbindungsschnittstelle für SQL Server und Azure SQL\-Datenbank.  
  
-   **SSIS\-Paket\-Projektvorlagen**. Verbesserung der Leistung des SSIS\-Katalogs: Die Leistung für die meisten SSIS\-Katalogansichten für Benutzer, die keine SSIS\-Administratoren sind, ist verbessert.  
  
-   **SSAS\-Projektvorlagen** enthalten Erweiterungen für Projekte mit tabellarischen Modellen in Analysis Services. Sie können den Befehl **Code anzeigen** verwenden, um die Modelldefinition im JSON\-Format anzuzeigen. Wenn Sie nicht mit einer Komplettedition von Visual Studio 2015 arbeiten, benötigen Sie eine solche, um den JSON\-Editor zu erhalten. Sie können die [Visual Studio Community Edition](https://www.visualstudio.com/en-us/downloads/download-visual-studio-vs.aspx) kostenlos herunterladen.  
  
## SSDT\-Vorschau Oktober 2015  
  
-   Neue Projektvorlagen für BI (Analysis Services\-Modelle, Reporting Services\-Berichte und Integration Services\-Pakete). Alle SQL Server\-Projektvorlagen befinden sich nun in einer SSDT.  
  
-   Neue SSIS\-Funktionen, etwa Hadoop\-Connector, Ablaufsteuerungsvorlage, gelockerte maximale Puffergröße für Datenflusstask.  
  
-   SQL Server 2016 CTP 3.0 bietet Unterstützung für Projekte für relationale Datenbanken.  
  
-   Verschiedene Programmfehlerbehebungen in SSIS und Unterstützung für Windows 7.  
  
## SSDT\-Vorschau September 2015  
  
-   Unterstützung mehrerer Sprachen ist neu in dieser Vorschau.  
  
## SSDT\-Vorschau August 2015  
  
-   Neues eigenständiges Setup.exe\-Programm für die Installation von SSDT.  Es ist nicht mehr erforderlich, eine geänderte Version von SQL Server\-Setup zu verwenden. Diese Version von SSDT enthält eine Projektvorlage zum Erstellen von relationalen Datenbanken, die in SQL Server oder Azure SQL\-Datenbank bereitgestellt werden sollen.  
  
## Siehe auch  
[Herunterladen von SQL Server Data Tools &#40;SSDT&#41;](../content/Download-SQL-Server-Data-Tools--SSDT-.md)  
[Vorgängerversionen von SQL Server Data Tools &#40;SSDT und SSDT-BI&#41;](../content/Previous-releases-of-SQL-Server-Data-Tools--SSDT-and-SSDT-BI-.md)  
[Neuigkeiten im Datenbankmodul](https://msdn.microsoft.com/ibrary/bb510411.aspx)  
[Neuigkeiten in Analysis Services](https://msdn.microsoft.com/library/bb522628.aspx)  
[Neuigkeiten in Integration Services](https://msdn.microsoft.com/library/bb522534.aspx)  
  
