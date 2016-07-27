---
title: "Herunterladen von SQL Server Management Studio (SSMS)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: adafeeef-4255-4924-8042-02f503d599ca
caps.latest.revision: 101
caps.handback.revision: 101
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
# Herunterladen von SQL Server Management Studio (SSMS)
SQL Server Management Studio (SSMS) ist eine integrierte Umgebung für den Zugriff, die Konfiguration, die Verwaltung und die Entwicklung aller SQL Server-Komponenten. SSMS kombiniert eine Vielzahl grafischer Tools mit einer Reihe umfassender Skript-Editoren, um Entwicklern und Administratoren mit verschiedenem Kenntnisstand den Zugriff auf SQL Server zu ermöglichen. Dieses Release bietet verbesserte Kompatibilität mit früheren Releases von SQL Server, ein eigenständiges Webinstallationsprogramm und Popupbenachrichtigungen innerhalb von SSMS, wenn neue Releases verfügbar sind.  
     
| ![Download verfügbar ist](../content/media/download.png) Herunterladen von SQL Server Management Studio (SSMS)  |  
|---|  
|**[Aktualisierten Hotfix für SQL Server Management Studio Juli 2016 herunterladen](http://go.microsoft.com/fwlink/?LinkID=822301)**|  

> [!IMPORTANT]
> * Auf der Setupseite für dieses Release ist aufgrund einer internen Buildeinstellung „August“ angegeben. Bei diesem Paket handelt es sich jedoch um einen Hotfix für das Juli-Release.  
> * In dieser Version von SSMS ist die [Option 'XACT_ABORT' in SSMS](https://msdn.microsoft.com/library/ms188792.aspx#Anchor_1) standardmäßig aktiviert. Diese Option weist SQL Server an, beim Auftreten eines Laufzeitfehlers ein Rollback der gesamten Transaktion auszuführen und den Batch abzubrechen. Sie können diese Option auf der Optionsseite des SQL Server-Dialogfelds „Abfrageausführung“ deaktivieren.

> [!NOTE]  
> Diese allgemein verfügbare Version von SSMS ist kostenlos, und für ihre Installation und Verwendung ist keine SQL Server-Lizenz erforderlich.  

 
## SQL Server Management Studio   
**Versionsinformationen**  
  
*In dieser Version von SSMS wird die Visual Studio 2015 Isolated Shell verwendet.*   
Die Versionsnummer des Hotfix für SQL Server Management Studio Juli 2016 lautet: 13.0.15600.2
  
**Unterstützte SQL Server-Versionen**  
  
* Diese Version von SSMS funktioniert mit allen [unterstützten Versionen von SQL Server (SQL Server 2008 – SQL Server 2016) ](https://support.microsoft.com/en-us/lifecycle?C2=1044) und bietet das höchste verfügbare Maß an Unterstützung für die Arbeit mit den neuesten Cloudfeatures in Azure SQL-Datenbank.  
* Es besteht keine explizite Sperre für SQL Server 2000 oder SQL Server 2005, jedoch funktionieren einige Features möglicherweise nicht ordnungsgemäß.  
* Darüber hinaus kann dieses Release von SSMS parallel zu früheren, nicht als Vorschau veröffentlichten Releases installiert werden.  
  
**Unterstützte Betriebssysteme**  
  
Diese Version von SSMS unterstützt die folgenden Plattformen, wenn sie mit dem aktuellen Servicepack ausgestattet sind:   
 Windows 10, Windows 8, Windows 8.1, Windows 7 (SP1), Windows Server 2012 (64-Bit), Windows Server 2012 R2 (64-Bit), Windows Server 2008 R2 (64-Bit)  
   
 **Verfügbare Sprachen**  
> [!NOTE]  
> In andere Sprachen als Englisch lokalisierte Versionen von SSMS benötigen das [KB 2862966-Sicherheitsupdate-Paket](https://support.microsoft.com/en-us/kb/2862966) für die Installation unter: Windows 8, Windows 7, Windows Server 2012 und Windows Server 2008 R2. 
  
 Diese Version von SSMS kann in folgenden Sprachen installiert werden:  
[Chinesisch (Volksrepublik China)](http://go.microsoft.com/fwlink/?LinkID=822301&clcid=0x804) | [Chinesisch (Taiwan)](http://go.microsoft.com/fwlink/?LinkID=822301&clcid=0x404) | [Englisch (Vereinigte Staaten)](http://go.microsoft.com/fwlink/?LinkID=822301&clcid=0x409) | [Französisch](http://go.microsoft.com/fwlink/?LinkID=822301&clcid=0x40c)  
[Deutsch](http://go.microsoft.com/fwlink/?LinkID=822301&clcid=0x407) | [Italienisch](http://go.microsoft.com/fwlink/?LinkID=822301&clcid=0x410) | [Japanisch](http://go.microsoft.com/fwlink/?LinkID=822301&clcid=0x411) | [Koreanisch](http://go.microsoft.com/fwlink/?LinkID=822301&clcid=0x412) | [Portugiesisch (Brasilien)](http://go.microsoft.com/fwlink/?LinkID=822301&clcid=0x416) | [Russisch](http://go.microsoft.com/fwlink/?LinkID=822301&clcid=0x419) | [Spanisch](http://go.microsoft.com/fwlink/?LinkID=822301&clcid=0x40a)  

 
## Änderungsprotokoll  
* ***Bearbeitung, 13. Juli:*** Fehlerbehebung in SSMS zur Aktivierung der fehlenden Kontextmenüelemente [(Microsoft Connect-Element #2883440)](https://connect.microsoft.com/SQLServer/feedback/details/2883440/lost-table-design-and-edit-top-n-rows-in-tables-context-menu).
* ***Bearbeitung 5. Juli:*** Verbesserte Unterstützung für SQL Server 2016-Tabellendatenbanken (Kompatibilitätsstufe 1200) im Dialogfeld „Analysis Services-Prozess“ und dem Bereitstellungs-Assistenten für Analysis Services.

* ***Bearbeitung 5. Juli:*** Neue Option im SSMS-Dialogfeld „Abfrageausführungsoptionen“ zum Festlegen von XACT_ABORT. Diese Option ist in dieser Version von SSMS standardmäßig aktiviert und weist SQL Server an, beim Auftreten eines Laufzeitfehlers ein Rollback der gesamten Transaktion auszuführen und den Batch abzubrechen.

* Unterstützung für Azure SQL Data Warehouse in SSMS.

* Umfangreiche Updates am SQL Server PowerShell-Modul. Zu diesen gehören ein neues [SQL PowerShell-Modul und neue CMDLETs für Always Encrypted, SQL Agent und SQL-Fehlerprotokolle](https://blogs.technet.microsoft.com/dataplatforminsider/2016/06/30/sql-powershell-july-2016-update).

* Unterstützung für die PowerShell-Skripterstellung im Always Encrypted-Assistenten.

* Deutlich verbesserte Verbindungszeiten für Azure SQL-Datenbanken.

* Neues Dialogfeld „URL-Sicherung“, das die Erstellung von Azure-Speicheranmeldeinformationen für Datenbanksicherungen von SQL Server 2016 unterstützt. Es bietet eine optimierte Benutzeroberfläche zum Speichern von Datenbanksicherungen unter einem Azure-Speicherkonto.
 
* Neues Wiederstellen-Dialogfeld zur Optimierung der Wiederherstellung einer SQL Server 2016-Datenbanksicherung aus dem Microsoft Azure-Speicherdienst. 

* Fehlerbehebung im SSMS-Abfrage-Designer, um das Hinzufügen von Tabellen zum Designer zu ermöglichen, wenn ein Benutzer nicht über SELECT-Berechtigungen für die Tabellen verfügt.

* Fehlerbehebung zum Hinzufügen von IntelliSense-Unterstützung für die Funktionen TRY_CAST() und TRY_CONVERT() [(Microsoft Connect-Element #2453461)](https://connect.microsoft.com/SQLServer/feedback/details/2453461/sql-server-2012-issue-with-try-cast).

* Fehlerbehebung im PowerShell-Modul, um das Laden der SQLAS-Erweiterung [(Microsoft Connect-Element #2544902)](https://connect.microsoft.com/SQLServer/feedback/details/2544902/ssms-march-2016-refresh-sqlps-failed-to-load-the-sqlas-extension) zu ermöglichen.

* Fehlerbehebung im SSMS-Editor-Fenster, um das Öffnen von SQL-Dateien per Drag-&-Drop zu ermöglichen [(Microsoft Connect-Element #2690658)](https://connect.microsoft.com/SQLServer/feedback/details/2690658/cannot-drag-sql-files-into-management-studios).

* Fehlerbehebung im Profiler, um den Absturz von Profiler beim Beenden zu beheben. [(Microsoft Connect-Element #2616550)](https://connect.microsoft.com/SQLServer/feedback/details/2616550/sql-server-2016-rc2-profiler-version-13-0-1300-275-wont-close-after-trace-is-started-even-after-trace-is-stopped).

* Fehlerbehebung in SSMS zum Verhindern des Absturzes beim Bearbeiten einer Join-Verknüpfung im SSMS-Tabellen-Designer [(Microsoft Connect-Element #2721052)](https://connect.microsoft.com/SQLServer/feedback/details/2721052/ssms-view-design-mode-right-click-on-join-crashes-ssms).

* Fehlerbehebung in SSMS, um die Datenbank-Skripterstellung für Mitglieder der db_owner-Rolle zu ermöglichen. [(Microsoft Connect-Element #2869241)](https://connect.microsoft.com/SQLServer/feedback/details/2869241/error-with-script-database-as-create-to-in-ssms-2008r2-and-ssms-2016-june).

* Fehlerbehebung im SSMS-Editor zum Entfernen der Verzögerung beim Schließen einer Abfrageregisterkarte, wenn der Server offline gesetzt wurde [(Microsoft Connect-Element #2656058)](https://connect.microsoft.com/SQLServer/feedback/details/2656058/ssms-2014-2016-query-tab-takes-significantly-longer-to-close-if-the-instance-it-was-connected-to-is-now-offline).

* Fehlerbehebung zum Aktivieren der Sicherungsoption in SQL Server Express-Datenbanken [(Microsoft Connect-Element #2801910)](https://connect.microsoft.com/SQLServer/feedback/details/2801910/ssms-2016-backup-option-not-appearing-in-tasks).

* Fehlerbehebung in Analysis Services, um den Data Feed-Anbieter für mehrdimensionale Analysis Services-Modelle ordnungsgemäß anzuzeigen.

Eine vollständige Auflistung der einzelnen Funktionen finden Sie unter   
                [SQL Server Management Studio – Änderungsprotokoll &#40;SSMS&#41;](../content/SQL-Server-Management-Studio---Changelog--SSMS-.md)  
  
Eine Liste der bekannten Probleme und Problemumgehungen finden Sie unter   
                [Versionshinweise für SQL Server Management Studio](../content/SQL-Server-Management-Studio----Release-Notes.md)  
  
Informationen zur Sammlung von Benutzerdaten finden Sie unter   
                [SQL Server-Datenschutzerklärung](http://www.microsoft.com/privacystatement/en-us/SQLServer/Default.aspx).  
  
## Vorgängerversionen  
[Vorgängerversionen von SQL Server Management Studio](../content/Previous-SQL-Server-Management-Studio-Releases.md)  
  
## Feedback  
  
![needhelp_person_icon](../content/media/needhelp_person_icon.png) [SQL Client Tools-Forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=sqltools) |  [Ein Problem oder einen Vorschlag bei Microsoft Connect verzeichnen](https://connect.microsoft.com/SQLServer/Feedback).  
  
## Siehe auch  
[Lernprogramm: SQL Server Management Studio](assetId:///d2bade70-07cf-4d94-b5d2-88aecb538ed1)  
[Dokumentation von SQL Server Management Studio](https://msdn.microsoft.com/library/hh213248(v=sql.130).aspx)  
[Microsoft SQL Server](https://msdn.microsoft.com/library/bb545450.aspx)  
[Weitere Updates und Service Packs](https://technet.microsoft.com/sqlserver/ff803383.aspx)  
[Herunterladen von SQL Server Data Tools (SSDT)](../content/Download-SQL-Server-Data-Tools--SSDT-.md)  
