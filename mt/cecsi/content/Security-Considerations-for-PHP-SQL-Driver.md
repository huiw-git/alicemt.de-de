---
title: "&#220;berlegungen zur Sicherheit f&#252;r den PHP-SQL-Treiber"
ms.custom: na
ms.date: 06/16/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a8c1a570-9204-454f-b94c-ba34f54d487c
caps.latest.revision: 37
caps.handback.revision: 36
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
# &#220;berlegungen zur Sicherheit f&#252;r den PHP-SQL-Treiber
Dieses Thema beschreibt Sicherheitsüberlegungen speziell für die Entwicklung, die Bereitstellung und den Betrieb von Anwendungen, die [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]verwenden. Ausführlichere Informationen zum Thema SQL Server-Sicherheit finden Sie unter [Datensicherheit und -konformität](http://go.microsoft.com/fwlink/?LinkId=129225).  
  
## Herstellen einer Verbindung mithilfe der Windows-Authentifizierung  
Aus folgenden Gründen sollte, wann immer möglich, die Windows-Authentifizierung für die Verbindung zu SQL Server verwendet werden:  
  
-   **Während der Authentifizierung werden keine Anmeldeinformationen über das Netzwerk übergeben.** Benutzernamen und Kennwörter werden nicht in die Verbindungszeichenfolge der Datenbank eingebettet. Dies bedeutet, dass böswillige Benutzer oder Angreifer die Anmeldeinformationen nicht durch Überwachen des Netzwerks oder durch Einsehen der Verbindungszeichenfolgen in Konfigurationsdateien erhalten können.  
  
-   **Die Benutzer werden über eine zentralisierte Kontoverwaltung verwaltet** Sicherheitsrichtlinien, wie z. B. Gültigkeitszeiträume für Passwörter, Vorgaben zur Mindestlänge von Passwörtern und die Sperrung von Konten nach mehreren ungültigen Anmeldeanfragen werden umgesetzt.  
  
Informationen zum Herstellen einer Verbindung mit einem Server mithilfe der Windows-Authentifizierung finden Sie unter [Vorgehensweise: Herstellen einer Verbindung mithilfe der Windows-Authentifizierung](../Topic/How%20to:%20Connect%20Using%20Windows%20Authentication.md).  
  
Wenn Sie eine Verbindung mithilfe der Windows-Authentifizierung herstellen, sollten Sie Ihre Umgebung so konfigurieren, dass SQL Server das Kerberos-Authentifizierungsprotokoll verwenden kann. Weitere Informationen finden Sie unter [Gewusst wie: Sicherstellen, dass Sie Kerberos-Authentifizierung verwenden, wenn Sie eine Remoteverbindung mit einer Instanz von SQL Server 2005 erstellen](http://go.microsoft.com/fwlink/?LinkId=121862) oder unter [Kerberos-Authentifizierung und SQL Server](http://go.microsoft.com/fwlink/?LinkId=129226).  
  
## Verwenden Sie verschlüsselte Verbindungen, wenn Sie sensible Daten übertragen.  
Sie sollten immer verschlüsselte Verbindungen verwenden, wenn der SQL Server sensible Daten empfangen/senden soll. Informationen zum Aktivieren verschlüsselter Verbindungen finden Sie unter [Aktivieren von verschlüsselten Verbindungen für das Datenbankmodul \(SQL Server-Konfigurations-Manager\)](http://go.microsoft.com/fwlink/?LinkId=121864). Zum Herstellen einer sicheren Verbindung mit dem [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)], verwenden Sie das Attribut „Encrypt connection“ beim Verbinden mit dem Server. Weitere Informationen zu Verbindungsattributen finden Sie unter [Connection Options](../content/Connection-Options.md).  
  
## Verwenden parametrisierter Abfragen  
Verwenden Sie parametrisierte Abfragen, um das Risiko von Angriffen durch Einschleusung von SQL-Befehlen zu senken. Beispiele für die Ausführung parametrisierter Abfragen finden Sie unter [How to: Perform Parameterized Queries](../Topic/How%20to:%20Perform%20Parameterized%20Queries.md).  
  
Weitere Informationen zu Angriffen durch Einschleusung von SQL-Befehlen und Sicherheitsüberlegungen dazu finden Sie unter [Einschleusen von SQL-Befehlen](http://go.microsoft.com/fwlink/?LinkId=104224).  
  
## Akzeptieren Sie KEINE Server- oder Verbindungszeichenfolgeinformationen von Endbenutzern.  
Schreiben Sie Anwendungen so, dass Endbenutzer keine Server- oder Verbindungszeichenfolgeinformationen an die Anwendungen übermitteln können. Sie können die Angriffsfläche für böswillige Aktivitäten reduzieren, indem Sie strikte Kontrolle über die Server- und Verbindungszeichenfolgeinformationen behalten.  
  
## Aktivieren von „WarningsAsErrors“ während der Anwendungsentwicklung  
Legen Sie während der Anwendungsentwicklung für den Schalter „ **WarningsAsErrors** “ den Wert **true** fest, damit vom Treiber ausgegebenen Warnungen wie Fehler behandelt werden. Dadurch können Sie Warnungen angehen, bevor Sie Ihre Anwendung bereitstellen. Weitere Informationen finden Sie unter [Handling Errors and Warnings](../content/Handling-Errors-and-Warnings.md).  
  
## Sichere Protokolle für bereitgestellte Anwendungen  
Stellen Sie sicher, dass die Protokolle bereitgestellter Anwendungen an einem sicheren Ort gespeichert werden, oder dass die Protokollierung deaktiviert ist. Dies schützt gegen mögliche Zugriffe von Endbenutzern auf Informationen, die in die Protokolldateien geschrieben wurden. Weitere Informationen finden Sie unter [Logging Activity](../content/Logging-Activity.md).  
  
## Siehe auch  
[Programmierhandbuch für den PHP-SQL-Treiber](../content/Programming-Guide-for-PHP-SQL-Driver.md)
  
