---
title: "Warnungen"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3f57d0f0-4781-46ec-82cd-b751dc5affef
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
# Warnungen
Ereignisse werden von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] erzeugt und in das [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] Windows-Anwendungsprotokoll geschrieben. [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent liest das Anwendungsprotokoll und vergleicht die dort festgehaltenen Ereignisse mit den von Ihnen definierten Warnungen. Wenn der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent eine Übereinstimmung findet, wird eine Warnung ausgelöst, also eine automatische Antwort auf das Ereignis. Mit dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent können Sie nicht nur [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Ereignisse überwachen, sondern auch den Leistungsstatus und die WMI-Ereignisse (Windows Management Instrumentation oder Windows-Verwaltungsinstrumentation).  
  
Zur Definition einer Warnung geben Sie Folgendes an:  
  
-   Der Name der Warnung.  
  
-   Das Ereignis oder den Leistungsstatus, mit dem die Warnung ausgelöst wird.  
  
-   Die Aktion, die der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent als Reaktion auf das Ereignis oder den Leistungsstatus ausführt.  
  
## Benennen einer Warnung  
Jede Warnung muss einen Namen aufweisen. Warnungsnamen müssen innerhalb der jeweiligen Instanz von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] eindeutig sein und dürfen nicht länger als **128** Zeichen lang sein.  
  
## Auswählen eines Ereignistyps  
Eine Warnung beantwortet ein Ereignis eines bestimmten Typs. Die folgenden Ereignistypen werden mithilfe von Warnungen beantwortet:  
  
-   [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Ereignisse  
  
-   [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Leistungsbedingungen  
  
-   WMI-Ereignisse  
  
Der Typ des Ereignisses bestimmt die Parameter, mit denen Sie das jeweilige Ereignis angeben.  
  
## Angeben eines SQL Server-Ereignisses  
Sie können angeben, dass eine Warnung als Antwort auf ein Ereignis oder mehrere Ereignisse eintritt. Mit den folgenden Parametern geben Sie die Ereignisse an, die eine Warnung auslösen:  
  
-   **Fehlernummer**  
  
    [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent löst eine Warnung aus, wenn ein bestimmter Fehler eintritt. Geben Sie beispielsweise an, dass die Fehlernummer 2571 als Antwort auf den unbefugten Versuch, die Datenbank-Konsolenbefehle (Database Console Commands, DBCC) aufzurufen, ausgegeben werden soll.  
  
-   **Schweregrad**  
  
    [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent löst eine Warnung aus, wenn ein Fehler des bestimmten Schweregrades eintritt. Beispielsweise können Sie angeben, einen Schweregrad von 15 für Syntaxfehler in Transact\-SQL-Anweisungen.  
  
-   **Datenbank**  
  
    [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent löst nur dann eine Warnung aus, wenn das Ereignis in einer bestimmten Datenbank auftritt. Diese Option kann zusätzlich zur Fehlernummer und zum Schweregrad verwendet werden. Enthält eine Instanz beispielsweise eine Datenbank für die Produktion und eine zweite Datenbank für die Berichterstellung, können Sie eine Warnung definieren, die nur bei Syntaxfehlern in der Produktionsdatenbank ausgelöst werden soll.  
  
-   **Fehlermeldungstext**  
  
    [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent löst eine Warnung aus, wenn die Ereignismeldung für das angegebene Ereignis eine bestimmte Textzeichenfolge enthält. Definieren Sie beispielsweise eine Warnung als Antwort auf Meldungen, die den Namen einer bestimmten Tabelle oder Einschränkung enthält.  
  
## Auswählen einer Leistungsbedingung  
Sie können Warnungen als Reaktion auf einen bestimmten Leistungsstatus angeben. In diesem Fall geben Sie den zu überwachenden Leistungsindikator, einen Schwellwert für die Warnung sowie das Verhalten des Leistungsindikators, an, bei dem die Warnung ausgelöst werden soll. Zum Festlegen eines Leistungsstatus definieren Sie die folgenden Punkte im [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent auf der Seite **Allgemein** im Dialogfeld **Neue Warnung** oder **Eigenschaften von Warnung** :  
  
-   **Objekt**  
  
    Das Objekt stellt den zu überwachenden Leistungsbereich dar.  
  
-   **Leistungsindikator**  
  
    Ein Leistungsindikator ist ein Attribut des zu überwachenden Leistungsbereichs.  
  
-   **Instanz**  
  
    Die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Instanz (sofern vorhanden) bestimmt die Instanz des zu überwachenden Attributs.  
  
-   **Warnung, falls Leistungsindikator** und **Wert**  
  
    Der Schwellwert für die Warnung sowie das Verhalten, bei dem die Warnung ausgelöst wird. Der Schwellwert ist ein numerischer Wert. Das Verhalten ist eine **der folgenden: unterschreitet**, **gleich**, oder **übersteigt eine für den Wert festgelegte Zahl**. Der **Wert** ist eine Zahl, die den Leistungsindikator beschreibt. Beispielsweise, um eine Warnung für das Leistungsobjekt **SQLServer: Sperren** bei der **Wartezeit für Sperre** länger als 30 Minuten, wählen Sie **übersteigt** und **Geben Sie 30 als Wert**.  
  
    Ein weiteres Beispiel wäre, wenn Sie festlegen, dass eine  Warnung für das Leistungsobjekt **SQLServer:Transactions** ausgegeben wird, wenn der freie Speicherplatz in **tempdb** unter 1000 KB fällt. Um dies festzulegen, wählen Sie den Leistungsindikator **freien Speicherplatz in ' tempdb ' (KB)**, **unterschreitet**,und ein **Wert** des **1000**.  
  
    > [!NOTE]  
    > Leistungsdaten werden in regelmäßigen Abständen geprüft, was zu einer geringfügigen Verzögerung (wenige Sekunden) zwischen dem Erreichen des Schwellwerts und dem Auslösen der Leistungswarnung führen kann.  
  
## Auswählen eines WMI-Ereignisses  
Sie können Warnungen als Reaktion auf ein bestimmtes WMI-Ereignis angeben. Zum Auswählen eines WMI-Ereignisses definieren Sie die folgenden Punkte im [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent auf der Seite **Allgemein** im Dialogfeld **Neue Warnung** oder **Eigenschaften von Warnung** :  
  
-   **Namespace**  
  
    [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent wird als WMI-Client im WMI-Namespace registriert, der zur Abfrage nach Ereignissen dient.  
  
-   **Query**  
  
    [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent verwendet die Windows Management Instrumentation Query Language (WQL)-Anweisung bereitgestellt, um das Ereignis zu identifizieren.  
  
Die folgenden Links führen zu häufig anfallenden Aufgaben:  
  
**So erstellen Sie eine Warnung auf der Grundlage einer Meldungsnummer**  
  
-   [SQL Server Management Studio](../content/Create-an-Alert-Using-an-Error-Number.md)  
  
-   [Transact-SQL](assetId:///d9b41853-e22d-4813-a79f-57efb4511f09)  
  
**So erstellen Sie eine Warnung auf der Grundlage von Schweregraden**  
  
-   [SQL Server Management Studio](../content/Create-an-Alert-Using-Severity-Level.md)  
  
-   [Transact-SQL](assetId:///d9b41853-e22d-4813-a79f-57efb4511f09)  
  
**So erstellen Sie eine Warnung auf der Grundlage eines WMI-Ereignisses**  
  
-   [SQL Server Management Studio](../content/Create-a-WMI-Event-Alert.md)  
  
-   [Transact-SQL](assetId:///d9b41853-e22d-4813-a79f-57efb4511f09)  
  
**So definieren Sie die Antwort auf eine Warnung**  
  
-   [SQL Server Management Studio](../content/Define-the-Response-to-an-Alert--SQL-Server-Management-Studio-.md)  
  
-   [Transact-SQL](assetId:///0525e0a2-ed0b-4e69-8a4c-a9e3e3622fbd)  
  
**Zum Erstellen eines Benutzers\-Ereignisfehlermeldung definiert**  
  
-   [Transact-SQL](assetId:///54746d30-f944-40e5-a707-f2d9be0fb9eb)  
  
**Bearbeiten eines Benutzers\-Ereignisfehlermeldung definiert**  
  
-   [Transact-SQL](assetId:///1b28f280-8ef9-48e9-bd99-ec14d79abaca)  
  
**Zum Löschen eines Benutzers\-Ereignisfehlermeldung definiert**  
  
-   [Transact-SQL](assetId:///17287a15-cdde-43d1-bb18-9f920bc15db8)  
  
**So deaktivieren oder reaktivieren Sie eine Warnung**  
  
-   [SQL Server Management Studio](../content/Disable-or-Reactivate-an-Alert.md)  
  
-   [Transact-SQL](assetId:///4bbaeaab-8aca-4c9e-abc1-82ce73090bd3)  
  
## Siehe auch  
[sp_update_alert (Transact-SQL)](assetId:///bcd731b1-3c4e-4086-b58a-af7a3af904ad)  
  
