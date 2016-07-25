---
title: "SQL Server Management Studio - Changelog (SSMS)"
ms.custom: na
ms.date: 07/21/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3dc76cc1-3b4c-4719-8296-f69ec1b476f9
caps.latest.revision: 50
caps.handback.revision: 33
translation.priority.mt: 
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
# SQL Server Management Studio - Changelog (SSMS)
### SSMS April 2016 Preview (13.0.14000.36)
* **Zur Verbesserung der im SSMS-Installer, um lesbare Fehlermeldungen hinzufügen.**

* **Verbesserung der Stretch-Assistent zum Hinzufügen der Unterstützung für Prädikate**.

* **Verbesserung der AlwaysEncrypted-Powershell-Cmdlet Verschlüsselung APIs hinzufügen**.

* **Fehlerkorrektur IntelliSense in der SSMS-Symbolleiste deaktivieren, wenn er in den Tools, Dialogfeld "Optionen" deaktiviert wurde.**
*Fehler von Kundenanfragen verknüpft:*
<https://connect.microsoft.com/SQLServer/feedback/details/2555163/sql-2016-rc2-turning-off-intellisense-from-options-does-not-turn-it-off-on-toolbar/>
  
* **Verbesserungen und Fehlerbehebungen in der Benutzeroberfläche des Showplan-Vergleich um den Abstand von langen Abfragepläne verwendet reduzieren**.

* **Fehlerbehebungen in SSMS SSMS stürzt beim Beenden verursachten Probleme beheben**. 

* **Fehlerbehebungen im Assistenten immer verschlüsselt Benutzerberechtigungen während der Verschlüsselung beizubehalten und um zu ermöglichen, Vorgänge trennen, nach Abschluss des Assistenten**.

* **Fehlerkorrektur immer verschlüsselt neue Spaltenhauptschlüssel im Dialogfeld zum Bereitstellen von Feedback auf einen Schlüssel mit einem nicht unterstützten kryptografischen Algorithmus (CNG)-Anbieter zu generieren.**

---
### SSMS März 2016 Preview aktualisieren (13.0.13000.55)
* **SSMS verwendet jetzt Visual Studio 2015 isolierte Shell.**
*Fehler von Kundenanfragen verknüpft:*
<https://connect.microsoft.com/SQLServer/feedback/details/2390544/update-ssms-to-use-visual-studio-2015-dependencies/>

* **Neue Schnellstart-Symbolleiste, mit denen Sie Menübefehle und Optionen schnell finden kann. (VS 2015 Isolated Shell)**

* **Verbesserungen in SSMS Designs Optionen zum Hinzufügen der Unterstützung für eine SSMS helles Design. (VS 2015 Isolated Shell)**

* **Fehlerbehebung in SSMS tools Menüoption Tastaturkombinationen für Abfragen korrekt zurückgesetzt, wenn die Schaltfläche "Standard" geklickt wird.**

* **Fehlerbehebung in SSMS neue Projektvorlagen leicht lesbaren Namen angezeigt.**

* **Fehler beim Anzeigen von Auftragsverlauf des SQL-Agents in SSMS aufgelöst.**
*Fehler von Kundenanfragen verknüpft:*
<https://connect.microsoft.com/SQLServer/feedback/details/2458860/error-viewing-job-history-microsoft-datawarehouse-sqm/>
  
* **Fehlerkorrektur, die offline-Installation von SSMS zuzulassen. Dadurch können Sie ohne Internetzugang installieren. (VS 2015 Isolated Shell)**
*Fehler von Kundenanfragen verknüpft:*
<https://connect.microsoft.com/SQLServer/feedback/details/2497178/cannot-install-ssms-when-server-has-no-internet-access/>
  
* **Fehlerkorrektur zum aktuellen Verzeichnis des Benutzers beibehalten, wenn SQL Server PowerShell (SQLPS) Modul importiert wird.**
*Fehler von Kundenanfragen verknüpft:*
<https://connect.microsoft.com/SQLServer/feedback/details/2434605/loading-sqlps-module-changes-current-directory-to-ps-sqlserver/>
  
* **Fehlerbehebung in SQL Server PowerShell (SQLPS)-Modul mit PowerShell-Verben genehmigt.**
*Fehler von Kundenanfragen verknüpft:*
<https://connect.microsoft.com/SQLServer/feedback/details/2432891/sqlps-module-uses-unapproved-powershell-verbs/>
  
* **Fehlerbehebung in SQL Server Powershell (SQLPS)-Modul Modul schneller zu laden.**
*Fehler von Kundenanfragen verknüpft:*
<https://connect.microsoft.com/SQLServer/feedback/details/2429153/sqlps-module-is-slow-to-load/>
  
* **Fehlerbehebung in SQL-Agent-Auftragsschritten zu ermöglichen, ändern einen Auftragsschritt.**
*Fehler von Kundenanfragen verknüpft:*
<https://connect.microsoft.com/SQLServer/feedback/details/2453996/issues-with-agent-in-ssms-2016-rc0-13-0-12000-65/>
  
* **Fehlerbehebung im SSMS-Objekt-Explorer, um die Liste alphabetisch Tabellen.**
*Fehler von Kundenanfragen verknüpft:*
<https://connect.microsoft.com/SQLServer/feedback/details/2424718/sql-server-2016-ssms-table-list-confusing/>
  
* **Fehlerbehebung in "Verfügbare Datenbanken", Dropdownliste anzeigen präzise Liste von Datenbanknamen verwendet, wenn eine SQL Server-Verbindung geändert wird.**
*Fehler von Kundenanfragen verknüpft:*
<https://connect.microsoft.com/SQLServer/feedback/details/2513420/available-databases-drop-down-box-does-not-update-when-connection-changes-in-ssms/>
  
* **Fehlerbehebung in SSMS Tastaturbefehle zum Verschieben des Fokus auf Dropdownmenü "Verfügbare Datenbanken", wenn die Tastenkombination 'STRG + U' gedrückt**
*Kundenanfragen Fehler verknüpft:*
<https://connect.microsoft.com/SQLServer/feedback/details/2534820/ssms-ctrl-u-doesnt-work/>

---
### SSMS März 2016 Preview (13.0.12500.29)
* **Verbesserung der SSMS-Webinstaller, drücken Sie Tasten Navigation zu ermöglichen.**

* **Zur Verbesserung der AlwaysEncrypted-Assistenten, um den alias-Datentypen für die Verschlüsselung unterstützt.**

* **Fehlerbehebung in AlwaysOn "Neuen Availability Group" die richtige Anzahl von maximal Automatisches Failover-Ziele angezeigt.**
*Fehler von Kundenanfragen verknüpft:* <https://connect.microsoft.com/SQLServer/feedback/details/2333670/ssms-is-showing-the-wrong-number-of-maximum-automatic-failover-targets/>
  
* **Fehlerbehebung in SSMS Webinstaller zur Behebung von Fehlern, die Installation beeinträchtigen.**
*Fehler von Kundenanfragen verknüpft:*
<https://connect.microsoft.com/SQLServer/feedback/details/2181548/sql-server-2016-ctp-3-2-management-studio-setup/>
  
* **Fehlerbehebung in SSMS Vorabversion zum Speichern von Wartungsplänen unter SQL Server 2012 und aktivieren.**
    
* **Fehlerbehebungen im Assistenten benutzerdefinierte mehrere Sicherungsnamen Stripesetvolumes Sicherungen zulassen und entsprechenden Sicherungsdatei Name angezeigt, wenn ein neuer Name eingegeben wird, sobald ein speicheranmeldeinformationen aktiviert ist.**

---
### SSMS Februar 2016 Preview (13.0.12000.65)
* **Verbesserung der Aktivitätsmonitor Textoptionen angezeigt, wenn die Einstellung für hohen Kontrast in SSMS aktiviert sind.**

* **Zur Verbesserung der im Dialogfeld Assistent immer verschlüsselt zum Anzeigen einer Warnung, wenn die Sortierung für eine Spalte während des Verschlüsselungsvorgangs geändert wird.**

* **Verbesserung der Policy-Management zur Unterstützung für das Erstellen von Bedingungen für Spalten-Verschlüsselungsschlüssel, Spaltenverschlüsselungswerte Schlüssel und Hauptschlüssel Spalte hinzufügen.**

* **Fehlerkorrektur zur Verbesserung der Nutzbarkeit Hauptschlüssel Cleanup-Dialogfeld immer verschlüsselt und Fehlermeldungen immer verschlüsselt.**

* **Fehlerkorrektur spaltenhauptschlüssel-Drehung immer verschlüsselt deaktivieren, wenn nur ein Schlüssel vorhanden ist.**

* **Fehlerbehebung für "Initialisierer Typ" Fehler tritt auf, wenn immer verschlüsselt angezeigt, mit der SSMS-Januar-Version oder der SSMS-Version, die mit der SQL Server RC0-Medien gebündelt werden.**

---
### SSMS Januar 2016 Preview (13.0.11000.78)
* **Fehlerbehebung in SSMS, um das Löschen von Sitzungen für erweiterte Ereignisse (XEvent) zu ermöglichen.**

* **Fehlerkorrektur Eigenschaftendialogfeld für eine verfügbarkeitsgruppe von SQL Server 2014 geöffnet.**
 *Fehler von Kundenanfragen verknüpft:*
 <https://connect.microsoft.com/SQLServer/feedback/details/1609719/>
   
* **Fehlerkorrektur aktivieren Sie die Möglichkeit, ein Azure-Replikat einer verfügbarkeitsgruppe hinzufügen.**
 *Fehler von Kundenanfragen verknüpft:*
 <https://connect.microsoft.com/SQLServer/feedback/details/2029135/>
   
* **Fehlerkorrektur Eigenschaftendialogfeld für SQL Server 2014-Datenbanken zu öffnen.**
 *Fehler von Kundenanfragen verknüpft:*
 <https://connect.microsoft.com/SQLServer/feedback/details/2080209/>
   
* **Fehlerkorrektur, doppelte Spalten zu entfernen, die für jede Tabelle, die beim Verbinden mit einer Azure SQL-Datenbank angezeigt werden.**
 *Fehler von Kundenanfragen verknüpft:*
 <https://connect.microsoft.com/SQLServer/feedback/details/2103116/>
---
### SSMS Dezember 2015 Preview (13.0.900.73)
* **Verbesserungen und Showplan im Vergleich zu Vergleich der aktuellen Abfrageausführungsplans mit einem in einer Datei gespeichert.**

* **Verbesserte IntelliSense-Unterstützung für Inline-Indizes in SSMS.**

* **Fehlerkorrektur Extended Events-Sitzung-Assistenten, um die Auswahl von Vorlagen bei Verbindung mit einer Azure-V12-Server zu aktivieren.**

* **New-Tabstopps in den Dialogfeldern "Audit erstellen" und "Neuer Benutzername", unter dem Ordner Sicherheit einfacher Tastaturnavigation zu aktivieren.**

* **Fehlerkorrektur Funktionalität "Umschalten auf der Registerkarte Ergebnisse nach der Ausführung der Abfrage" zu aktivieren, wenn SSMS, zum Anzeigen der Ergebnisse im Rasterformat festgelegt ist.** 
 *Fehler von Kundenanfragen verknüpft:*
  <https://connect.microsoft.com/SQLServer/feedback/details/1390296/switch-to-results-tab-after-query-execution-grid-mode-in-ssms-2016>

* **Fehlerkorrektur, nicht abgeschnitten Spaltenüberschriften angezeigt, wenn SSMS, zum Anzeigen der Ergebnisse im Rasterformat festgelegt ist.**
 *Fehler von Kundenanfragen verknüpft:*
  <https://connect.microsoft.com/SQLServer/feedback/details/2004111/bugbash-column-headers-in-grid-mode-truncated-with-courier-new-8>
    
* **Updates für die Installation von SSMS ermöglichen Webinstaller.**
 *Fehler von Kundenanfragen verknüpft:*
<https://connect.microsoft.com/SQLServer/feedback/details/2003865/ssms-october-preview-incoherent-error-message>
<https://connect.microsoft.com/SQLServer/feedback/details/2079557/unable-to-instal-sql-server-update-13-0-800-111-over-13-0-700-242-error-code-2711>

---
### SSMS November 2015 Preview (13.0.800.111)
* **Bitmapskalierung Unterstützung für High-DPI in SSMS angezeigt.**

* **Verbesserungen an der Benutzeroberfläche von AlwaysEncrypted Dialogfelder und Assistenten vereinfacht das Erstellen von Datenbank-Verschlüsselungsschlüssel.**

* **Neue mit der rechten Maustaste Option im Kontextmenü in der Liste "Prozesse" im Aktivitätsmonitor Live-Abfragestatistik anzeigen.**

* **Fehlerkorrektur richtigen Aktivieren von SSMS Preview-Versionen auf Clientcomputern zu deinstallieren.**
  *Fehler von Kundenanfragen verknüpft:*
  <http://connect.microsoft.com/SQLServer/feedback/details/1868474/ssms-2016-preview-can-be-installed-but-not-uninstalled>

* **Fehlerkorrektur, damit der Auftrag bearbeitet werden kann Schritte auch, wenn eine Datei fehlt in der SQL-Agent für**.
  *Fehler von Kundenanfragen verknüpft:*
  <https://connect.microsoft.com/SQLServer/feedback/details/1769778/management-studio-2016-sql-job-agent>
    <https://connect.microsoft.com/SQLServer/feedback/details/1502100/ssms-preview-error>
    
* **Fehlerbehebung in "Zieldaten anzeigen" Menüoption für eine Extended Events-Sitzung auf einer Datenbank, die in einer Azure Virtual machines.**
  *Verknüpften Fehler Kundenanfragen*: <https://connect.microsoft.com/SQLServer/feedback/details/1769778/management-studio-2016-sql-job-agent>
***
### SSMS Oktober 2015 Preview (13.0.700.242)
* **Neue modernisierten einfache Web-Installationsprogramm, das die SSMS vereinfacht herunterladen und Installieren von Prozess.**

* **Neue immer verschlüsselt Spalte Verschlüsselung-Assistenten die clientseitige Verschlüsselung und Entschlüsselung der ausgewählten Spalten.**

* **Dialogfeld "Neues Spalte Master Key (CMK) Drehung" für Datenbanken immer verschlüsselt, das den Prozess der Verschlüsselungsschlüssel zum Schützen von Daten vereinfacht.**

* **Erweitern Sie neue Datenbank überwachen, die Problembehandlung und zum Überwachen des Migrationsstatus von Daten in die Cloud ermöglicht.**

* **Verbesserungen an der Stretch-Assistent zur Unterstützung einen Microsoft Azure-Server, die nicht in der standardmäßigen Microsoft Azure-Abonnement auswählen.**
  *Fehler von Kundenanfragen verknüpft:*
  <https://connect.microsoft.com/SQLServer/feedback/details/1687063/cannot-choose-from-multiple-microsoft-azure-subscriptions>
* **Fehlerkorrektur einwandfreie Anzeige von live-Ausführungsplan in SSMS zulässig.**
  *Fehler von Kundenanfragen verknüpft:*
<https://connect.microsoft.com/SQLServer/feedback/details/1774446/viewing-live-execution-plan-from-activity-monitor-crashes-ssms>  
* **Fehlerkorrektur So entfernen Sie ungültige Optionen in SSMS scripting von Datenbank-Momentaufnahmen**
  *Kundenanfragen Fehler verknüpft:*
<https://connect.microsoft.com/SQLServer/feedback/details/1515168/ssms-scripting-of-database-snapshots-includes-invalid-options>
* **Fehlerbehebung in Abfrage Data Store-Benutzeroberfläche zum Anzeigen von Details im Bereich "Top-Ressource Abfragen".**
  *Fehler von Kundenanfragen verknüpft:*
<https://connect.microsoft.com/SQLServer/feedback/details/1737185/sql-server-2016-overall-resource-consumption-query-store-pane-issue>
***
### SSMS September 2015 Preview (13.0.600.65)
* **Dialogfeld "neue Firewall Regel", das das Herstellen einer Verbindung mit einer Azure SQL-Datenbank vereinfacht.**    
  
* **Aktualisierte "Neuer Index" Dialogfeld ermöglicht das Erstellen von gruppierten Rowstore indiziert, auch wenn ein gruppierter columnstore-Index vorhanden ist. Diese Funktion ist für SQL 2016 und höher verfügbar.**    
  *Verknüpften Fehler Kundenanfragen:*  
  <https://Connect.Microsoft.com/SQLServer/Feedback/Details/1552617/Creation-of-NC-Index-When-Clustered-columnstore-Index>
    
* **Fehlerkorrektur zu ermöglichen, anzeigen und Bearbeiten von SQL-Agent-Auftrag Schritte in SSMS Preview-Versionen, die auf Windows 7 ausgeführt wird.**    
  *Verknüpften Fehler Kundenanfragen:*  
  <https://Connect.Microsoft.com/SQLServer/Feedback/Details/1548140/Cannot-View-or-Edit-Any-SQL-Agent-Job-Step>,  
  <https://Connect.Microsoft.com/SQLServer/Feedback/Details/1626895/Unable-to-Load-DLL-DTS>,  
  <https://Connect.Microsoft.com/SQLServer/Feedback/Details/1576662/Error-Creating-New-Job-Step>   
    
* **Fehlerkorrektur Trigger Knoten in SSMS für SQL Server 2014 oder höher angezeigt.**    
  *Verknüpften Fehler Kundenanfragen:*  
  <https://Connect.Microsoft.com/SQLServer/Feedback/Details/1617533/Trigger-Node-Missing> 
    
* **Fehlerbehebungen im Datenbank- und der Standardbericht Benutzeroberfläche Header Versionsinformationen ausgeschlossen.**    
  *Verknüpften Fehler Kundenanfragen:*  
  <https://Connect.Microsoft.com/SQLServer/Feedback/Details/1387471/Report-Headings-wrongly-Named>
    
* **Fehlerkorrektur, um zu verhindern, dass einen Live-Abfragestatistik-Knoten als abgeschlossen angezeigt wird, wenn er nicht vollständig ist.**    
  *Verknüpften Fehler Kundenanfragen:*  
  <https://Connect.Microsoft.com/SQLServer/Feedback/Details/1589096/Live-Query-STATISTICS-Node-Shows-As-Completed>

***    
### SSMS August 2015 Preview (13.0.500.53)
* **Objekt-Explorer wird aktualisiert und die Verzögerung beim Laden zu reduzieren, wenn eine große Anzahl von Datenbanken vorhanden sind.**

* **Verbesserungen für die Installation von SSMS auf Windows 10-Computern.**

* **Fehlerbehebungen und Updates für SQL Server-Konfigurations-Manager und SSMS Benutzer Berichte-Benutzeroberfläche**  
***

### SSMS Juli 2015 Preview (13.0.400.91)
* **Datenbankdiagramme für Azure SQL-Datenbank (V12).**

* **Verbesserte IntelliSense-Unterstützung für neue temporaltabelle-Syntax.**

* **Aktualisierte DacFx-Bibliothek zur Unterstützung der neuesten Azure SQL-Datenbanken-Features einschließlich zeilenbasierter Sicherheit und Azure Active Directory-Authentifizierung.**

* **Fehlerkorrekturen (aktualisiert "auf Updates überprüfen" Benutzeroberfläche, die Benutzeroberfläche zu beheben, auf 'Kompatibilitätsgrad' Liste und vieles mehr).**
***

### SSMS Juni 2015 Preview (13.0.300.44)
* **Neue SSMS Lightweight-Web-Installer.**

* **Automatische Prüfung auf Updates.**

* **SSMS verfügt jetzt über Full-Text-Search-Unterstützung für Azure SQL-Datenbank (V12).**

* **Top Kundenanfragen behandelt:**
  * 'Bearbeiten oberste 200 Zeilen' für Tabellen und Sichten im Objekt-Explorer aktiviert.
  * Tabellen-Designer für Azure SQL-Datenbank (V12) aktiviert.
  * Datenbank und Tabelle Eigenschaftendialogfelder für Azure SQL-Datenbank (V12) aktiviert.
  
 * **Neue Option zum Überspringen der Aufforderung zum Speichern von T-SQL-Dateien.**
 
 * **Import/Export-assistentenunterstützung für neue Azure SQL-Datenbank-Dienstebenen (Basic, Standard und Premium).**
 
 * **Zahlreiche Fehlerkorrekturen (scripting Szenarien, Aktivieren der änderungsnachverfolgung für SQL-Datenbanken und mehr).** 
   






  
