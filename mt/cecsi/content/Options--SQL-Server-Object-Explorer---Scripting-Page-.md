---
title: "Optionen (SQL Server Objekt-Explorer - Seite Scripting)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6105aec9-1b72-4cb2-bd24-fc35f6d95240
caps.latest.revision: 5
caps.handback.revision: 4
manager: jhubbard
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
# Optionen (SQL Server Objekt-Explorer - Seite Scripting)
Mithilfe dieser Seite können Sie Skripterstellungsoptionen festlegen, die für die folgenden Befehle in objektkontextmenüs im gelten **Objekt-Explorer**:  
  
-   **Bearbeiten Sie** Befehle für Benutzertabellen und Sichten.  
  
-   **Skript <object> als** Befehle für Benutzer\-Objekte erstellt.  
  
-   **Ändern Sie** Befehl für den Benutzer\-Objekte erstellt.  
  
-   Auf dieser Seite wird auch die Standardwerte der Skripterstellungsoptionen für den **Generieren von SQL Server-Skript-Assistenten**.  
  
## Hinweise  
Die **Bearbeiten** und **Ändern** Befehle können Ergebnisse erzeugen, die nicht mit der **Skript <object> als** -Befehl für die gleiche optionseinstellung. Die **Bearbeiten** und **Ändern** Befehle dienen zum Ändern von Objekten in der aktuellen Datenbank während einer Abfrage-Editor-Sitzung. Die **Skript <object> als** Befehl dient zum Generieren eines Skripts, damit sie später verwendet werden kann, um Objekte zu erstellen.  
  
## Optionen  
Geben Sie Skriptoptionen an, indem Sie eine Auswahl aus den verfügbaren Einstellungen in der Liste rechts neben den einzelnen Optionen treffen.  
  
### Allgemeine Skripterstellungsoptionen  
**Einzelne Anweisungen begrenzen**  
Trennt die einzelnen [!INCLUDE[tsql](../content/includes/tsql_md.md)]-Anweisungen mithilfe eines Batchtrennzeichens voneinander ab. So ändern Sie das standardbatchtrennzeichen für **-Abfrage-Editor**, wählen **Tools**\/**Optionen**\/**Abfrageausführung**\/**SQL Server**\/**Allgemeine**\/**Batchtrennzeichen**. Der Standardwert lautet False. Weitere Informationen finden Sie unter [GO (Transact-SQL)](assetId:///b2ca6791-3a07-4209-ba8e-2248a92dd738).  
  
**Beschreibende Header einschließen**  
Fügt dem Skript beschreibende Kommentare hinzu, indem das Skript in Abschnitte für die einzelnen Objekte aufgeteilt wird. Der Standardwert lautet "True". Weitere Informationen finden Sie unter [/*...*/ (Kommentar) (Transact-SQL)](assetId:///4d9ab1b2-4bbb-4c16-beb1-cafc1af7417c).  
  
**vardecimal-Optionen einschließen**  
Schließt die vardecimal-Speicheroptionen ein. Der Standardwert lautet False. Weitere Informationen finden Sie unter und [Sp_db_vardecimal_storage_format (Transact-SQL)](assetId:///9920b2f7-b802-4003-913c-978c17ae4542).  
  
**Skript für Änderungsnachverfolgung erstellen**  
Schließt Nachverfolgungsinformationen für Änderungen im Skript ein.  
  
**Skripterstellung für Serverversion**  
Erstellt ein Skript, das für die ausgewählte Version von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ausgeführt werden kann. Funktionen, die in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] neu sind, können für eine Skripterstellung für frühere Versionen nicht verwendet werden. Einige für erstellte Skripts [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] kann nicht ausgeführt werden, auf dem Server, auf denen eine frühere Version von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)], oder auf eine Datenbank mit einer früheren [Datenbank-Kompatibilitätsgrad](assetId:///ca5fd220-d5ea-4182-8950-55d4101a86f6).  
  
**Vollständige Skript\-Text Kataloge**  
Enthält ein Skript für die vollständige\-Text Kataloge. Der Standardwert lautet False. Weitere Informationen finden Sie unter [CREATE FULLTEXT CATALOG (Transact-SQL)](assetId:///d7a8bd93-e2d7-4a40-82ef-39069e65523b).  
  
**Skript verwenden <database>**  
Fügt die USE DATABASE-Anweisung an das Skript zum Erstellen von Datenbankobjekten im Kontext des aktuellen **Objekt-Explorer** Datenbank. Wenn das Skript für die Verwendung in einer anderen Datenbank vorgesehen ist, wählen Sie False aus, um dies auszulassen. Der Standardwert lautet "True". Weitere Informationen finden Sie unter [verwenden (Transact-SQL)](assetId:///c05acac8-c063-4770-8e36-d7f71d500b10).  
  
### Skriptoptionen für Objekte  
**Skript für abhängige Objekte generieren.**  
Generiert ein Skript für zusätzliche Objekte, die erforderlich sind, wenn das Skript für das ausgewählte Objekt ausgeführt wird. Der Standardwert lautet False.  
  
**IF NOT EXISTS-Klausel einschließen**  
Schließt eine Anweisung ein, mit der überprüft wird, ob die einzelnen Objekte nicht in der Datenbank vorhanden sind, bevor versucht wird, das Objekt zu erstellen. Der Standardwert lautet False. Weitere Informationen finden Sie unter [IF... ELSE (Transact-SQL)](assetId:///676c881f-dee1-417a-bc51-55da62398e81) und [EXISTS (Transact-SQL)](assetId:///b6510a65-ac38-4296-a3d5-640db0c27631).  
  
**Schema für Objektnamen qualifizieren**  
Qualifiziert Objektnamen mit dem Objektschema. Der Standardwert lautet False. Weitere Informationen finden Sie unter [Erstellen eines Datenbankschemas](assetId:///ed2a5522-f4d2-4111-95a4-d3e1e5081739).  
  
**Skripterstellung für erweiterte Eigenschaften**  
Enthält erweiterte Eigenschaften im Skript, wenn das Objekt über erweiterte Eigenschaften verfügt. Der Standardwert lautet False. Weitere Informationen finden Sie unter [Sp_addextendedproperty (Transact-SQL)](assetId:///565483ea-875b-4133-b327-d0006d2d7b4c).  
  
**Skriptbesitzer**  
Schließt den Besitzer im generierten Skript ein. Der Standardwert lautet False.  
  
**Skripterstellung für Berechtigungen**  
Schließt Berechtigungen für Datenbankobjekte im Skript ein. Der Standardwert lautet "True". Weitere Informationen finden Sie unter [Berechtigungen](assetId:///f28e3dea-24e6-4a81-877b-02ec4c7e36b9).  
  
### Tabelle\/Optionen anzeigen  
Die folgenden Optionen gelten nur für Skripts für Tabellen oder Sichten.  
  
**Konvertieren von Benutzer\-definierten Typen Basisdatentypen**  
Konvertiert Benutzer\-definierten Datentypen in die Basistypen, aus denen sie erstellt wurden. Verwenden Sie True, wenn die Quelle Datenbankbenutzer\-benutzerdefinierte Daten, die Typen gibt es nicht in der Datenbank, in dem das Skript ausgeführt werden soll. Verwenden Sie False, damit sich Benutzer\-Datentypen definiert. Der Standardwert lautet False. Weitere Informationen finden Sie unter [CREATE TYPE (Transact-SQL)](assetId:///2202236b-e09f-40a1-bbc7-b8cff7488905).  
  
**SET ANSI PADDING-Befehle generieren**  
Fügt die SET ANSI\_PADDING-Anweisung vor und nach jeder CREATE TABLE-Anweisung. Der Standardwert lautet "True". Weitere Informationen finden Sie unter [SET ANSI_PADDING (Transact-SQL)](assetId:///92bd29a3-9beb-410e-b7e0-7bc1dc1ae6d0).  
  
**Sortierung einschließen**  
Schließt eine Sortierung in die Spaltendefinition ein. Der Standardwert lautet "True". Weitere Informationen finden Sie unter [Sortierung und Unicode-Unterstützung](assetId:///92d34f48-fa2b-47c5-89d3-a4c39b0f39eb).  
  
**IDENTITY-Eigenschaft einschließen**  
Schließt Definitionen für den IDENTITY-Ausgangswert und das IDENTITY-Inkrement ein. Der Standardwert lautet "True". Weitere Informationen finden Sie unter [IDENTITY (Eigenschaft) (Transact-SQL)](assetId:///8429134f-c821-4033-a07c-f782a48d501c).  
  
**Schema für Fremdschlüsselverweise qualifizieren**  
Fügt Tabellenverweisen für FOREIGN KEY-Einschränkungen den Schemanamen hinzu. Der Standardwert lautet "True".  
  
**Skripterstellung für gebundene Standardwerte und Regeln**  
Enthält die **sp\_Bindefault** und **sp\_Bindrule** Bindung Aufrufe gespeicherter Prozeduren. Der Standardwert lautet "True". Weitere Informationen finden Sie unter [Sp_bindefault (Transact-SQL)](assetId:///3da70c10-68d0-4c16-94a5-9e84c4a520f6) und [Sp_bindrule (Transact-SQL)](assetId:///2606073e-c52f-498d-a923-5026b9d97e67).  
  
**Skripterstellung für CHECK-Einschränkungen**  
Fügt [CHECK-Einschränkungen](assetId:///637098af-2567-48f8-90f4-b41df059833e) an das Skript. Der Standardwert lautet "True".  
  
**Skripterstellung für Standard**  
Schließt Spaltenstandardwerte in das Skript ein. Der Standardwert lautet False. Weitere Informationen finden Sie unter [CREATE DEFAULT (Transact-SQL)](assetId:///08475db4-7d90-486a-814c-01a99d783d41).  
  
**Skripterstellung für Dateigruppen**  
Gibt die Dateigruppe in der ON -Klausel für Tabellendefinitionen an. Der Standardwert lautet False. Weitere Informationen finden Sie unter [CREATE TABLE (Transact-SQL)](assetId:///1e068443-b9ea-486a-804f-ce7b6e048e8b).  
  
**Skripterstellung für Fremdschlüssel**  
Enthält [FOREIGN KEY-Einschränkungen](assetId:///31fbcc9f-2dc5-4bf9-aa50-ed70ec7b5bcd) im Skript. Der Standardwert lautet False.  
  
**Vollständige Skript\-von Volltextindizes**  
Enthält vollständige\-Textindizes im Skript. Der Standardwert lautet False. Weitere Informationen finden Sie unter [CREATE FULLTEXT INDEX (Transact-SQL)](assetId:///8b80390f-5f8b-4e66-9bcc-cabd653c19fd).  
  
**Skripterstellung für Indizes**  
Schließt gruppierte Indizes, nicht gruppierte Indizes und XML-Indizes in das Skript ein. Der Standardwert lautet "True". Weitere Informationen finden Sie unter [CREATE INDEX (Transact-SQL)](assetId:///d2297805-412b-47b5-aeeb-53388349a5b9).  
  
**Skripterstellung für Partitionsschemas**  
Schließt Tabellenpartitionierungsschemas in das Skript ein. Der Standardwert lautet False. Weitere Informationen finden Sie unter [CREATE PARTITION SCHEME (Transact-SQL)](assetId:///5b21c53a-b4f4-4988-89a2-801f512126e4).  
  
**Skripterstellung für Primärschlüssel**  
Enthält [primären und Foreign Key-Einschränkungen](assetId:///31fbcc9f-2dc5-4bf9-aa50-ed70ec7b5bcd) im Skript. Der Standardwert lautet "True".  
  
**Skripterstellung für Statistiken**  
Enthält Benutzer\-Statistiken im Skript definiert. Der Standardwert lautet False. Weitere Informationen finden Sie unter [CREATE STATISTICS (Transact-SQL)](assetId:///b23e2f6b-076c-4e6d-9281-764bdb616ad2).  
  
**Skripterstellung für Trigger**  
Schließt Trigger in das Skript ein. Der Standardwert lautet False. Weitere Informationen finden Sie unter [CREATE TRIGGER (Transact-SQL)](assetId:///edeced03-decd-44c3-8c74-2c02f801d3e7).  
  
**Skripterstellung für eindeutige Schlüssel**  
Enthält [Unique-Einschränkungen und Check-Einschränkungen](assetId:///637098af-2567-48f8-90f4-b41df059833e) im Skript. Der Standardwert lautet False.  
  
**Skripterstellung für Sichtspalten**  
Deklariert Sichtspalten in Sichtheadern. Der Standardwert lautet False. Weitere Informationen finden Sie unter [CREATE VIEW (Transact-SQL)](assetId:///aecc2f73-2ab5-4db9-b1e6-2f9e3c601fb9).  
  
**ScriptDriIncludeSystemNames**  
Schließt vom System generierte Einschränkungsnamen ein, damit die deklarative referenzielle Integrität erzwungen wird. Der Standardwert lautet False. Weitere Informationen finden Sie unter [REFERENTIAL_CONSTRAINTS (Transact-SQL)](assetId:///5d358f18-0a85-4b55-af4b-98d5f4cd1020).  
  
## Siehe auch  
[Erstellen von Skripts (SQL Server Management Studio)](assetId:///9711c617-3c68-4e5a-aea3-befc64d51524)  
  
