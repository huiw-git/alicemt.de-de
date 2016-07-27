---
title: "Treiberf&#228;higes Verbindungspooling im ODBC-Treiber f&#252;r SQL Server."
ms.custom: na
ms.date: 06/16/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 455ab165-8e4d-4df9-a1d7-2b532bfd55d6
caps.latest.revision: 15
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
  - zh-cn
  - zh-tw
---
# Treiberf&#228;higes Verbindungspooling im ODBC-Treiber f&#252;r SQL Server.
  Der ODBC-Treiber für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] unterstützt [Treiberfähiges Verbindungspooling](http://msdn.microsoft.com/library/hh405031(VS.85).aspx). Dieses Thema beschreibt die Erweiterungen der Funktion „Treiberfähiges Verbindungspooling“ im Microsoft ODBC-Treiber für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] unter Windows:  
  
-   Unabhängig von den Verbindungseigenschaften wechseln Verbindungen, die SQLDriverConnect verwenden, in einen separaten Pool von Verbindungen, welche SQLConnect verwenden.  
  
-   Bei Verwendung der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Authentifizierung und des treiberfähigen Verbindungspoolings verwendet der Treiber nicht den Sicherheitskontext des Windows-Benutzers für den aktuellen Thread, um Verbindungen im Pool zu trennen. Das bedeutet, wenn Verbindungen in ihren Parametern für Identitätswechsel-Szenarien unter Windows mit der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Authentifizierung äquivalent sind und die gleichen [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Anmeldeinformationen zur Verbindung mit dem Back-End verwenden, können andere Windows-Benutzer möglicherweise den gleichen Pool aus Verbindungen verwenden. Bei Verwendung der Windows\-Authentifizierung und des treiberfähigen Verbindungspoolings verwendet der Treiber den aktuellen Sicherheitkontext des Windows-Benutzers für den aktuellen Thread, um Verbindungen im Pool zu trennen. D. h. für Windows-Identitätswechsel-Szenarios teilen sich verschiedene Windows-Benutzer keine Verbindungen, auch wenn die Verbindungen dieselben Parameter verwenden.  
  
-   Treiberfähiges Verbindungspooling verhindert, dass eine fehlerhafte Verbindung aus dem Pool zurückgegeben wird.  
  
-   Treiberfähiges Verbindungspooling erkennt treiberspezifische Verbindungsattribute. Wenn also eine Verbindung einen schreibgeschützten SQL\_COPT\_SS\_APPLICATION\_INTENT-Satz verwendet, erhält diese Verbindung ihren eigenen Verbindungspool.  
  
-   Wenn eine der folgenden Verbindungsattribut-IDs oder eines der Schlüsselwörter für Verbindungszeichenfolgen zwischen Ihrer Verbindungszeichenfolge und der in einem Pool zusammengefassten Verbindungszeichenfolge abweicht, verwendet der Treiber eine gepoolte Verbindung. Allerdings ist die Leistung besser, wenn alle Verbindungsattribut-IDs oder Schlüsselwörter für Verbindungszeichenfolgen übereinstimmen. \(Um eine Übereinstimmung einer Verbindung im Pool herzustellen, setzt der Treiber das Attribut zurück. Die Leistung wird beeinträchtigt, da ein zusätzlicher Netzwerkaufruf notwendig ist, um die folgenden Parameter zurückzusetzen.  
  
     Wenn sich zwei oder mehr der folgenden Verbindungsattribute oder Verbindungsschlüsselwörter unterscheiden, wird keine gepoolte Verbindung verwendet.  
  
    -   Sprache  
  
    -   QuoteId  
  
    -   SQL\_ATTR\_TXN\_ISOLATION  
  
    -   SQL\_COPT\_SS\_QUOTED\_IDENT  
  
-   Gibt es einen Unterschied in einem der folgenden Verbindungsschlüsselwörter zwischen Ihrer Verbindungszeichenfolge und einer gepoolten Verbindungszeichenfolge, wird keine gepoolte Verbindung verwendet.  
  
    ||||  
    |-|-|-|  
    |Adresse|AnsiNPW|App|  
    |ApplicationIntent|Datenbank|Encrypt|  
    |Failover\_Partner|FailoverPartnerSPN|MARS\_Verbindung|  
    |Netzwerk|PWD|Server|  
    |ServerSPN|Vertrauenswürdige\_Verbindung|TrustServerCertificate|  
    |UID|WSID||  
  
     Gibt es einen Unterschied in einem der folgenden Verbindungsattribute zwischen Ihrer Verbindungszeichenfolge und einer gepoolten Verbindungszeichenfolge, wird keine gepoolte Verbindung verwendet.  
  
    ||||  
    |-|-|-|  
    |SQL\_ATTR\_CURRENT\_CATALOG|SQL\_ATTR\_PACKET\_SIZE|SQL\_COPT\_SS\_ANSI\_NPW|  
    |SQL\_COPT\_SS\_ATTACHDBFILENAME|SQL\_COPT\_SS\_BCP|SQL\_COPT\_SS\_CONCAT\_NULL|  
    |SQL\_COPT\_SS\_ENCRYPT|SQL\_COPT\_SS\_FAILOVER\_PARTNER|SQL\_COPT\_SS\_FAILOVER\_PARTNER\_SPN|  
    |SQL\_COPT\_SS\_INTEGRATED\_SECURITY|SQL\_COPT\_SS\_MARS\_ENABLED|SQL\_COPT\_SS\_OLDPWD|  
    |SQL\_COPT\_SS\_SERVER\_SPN|SQL\_COPT\_SS\_TRUST\_SERVER\_CERTIFICATE|SSPROP\_AUTH\_REPL\_SERVER\_NAME|  
  
-   Der Treiber kann die folgenden Verbindungsschlüsselwörter und Attribute zurücksetzen und anpassen, ohne einen zusätzlichen Netzwerkaufruf durchzuführen. Der Treiber setzt diese Parameter zurück, um sicherzustellen, dass die Verbindung keine falschen Informationen enthält.  
  
     Diese Schlüsselwörter werden nicht berücksichtigt, wenn der Treiber-Manager versucht, eine Übereinstimmung zwischen Ihrer Verbindung und einer Verbindung im Pool zu erzielen. \(Auch wenn Sie einen dieser Parameter ändern, kann eine vorhandene Verbindung wiederverwendet werden. Der Treiber setzt die Optionen nach Bedarf zurück.\) Diese Attribute können clientseitig ohne einen zusätzliche Netzwerkaufruf zurückgesetzt werden.  
  
    ||||  
    |-|-|-|  
    |AutoTranslate|Beschreibung|MultisubnetFailover|  
    |QueryLog\_On|QueryLogFile|QueryLogTime|  
    |Regional|StatsLog\_On|StatsLogFile|  
  
     Wenn Sie eine der folgenden Verbindungsattribute ändern, kann eine vorhandene Verbindung wiederverwendet werden.  Der Treiber wird je nach Bedarf den Wert zurücksetzen. Der Treiber kann diese Attribute clientseitig ohne einen zusätzliche Netzwerkaufruf zurücksetzen  
  
    ||||  
    |-|-|-|  
    |Alle Anweisungsattribute|SQL\_ATTR\_AUTOCOMMIT|SQL\_ATTR\_CONNECTION\_TIMEOUT|  
    |SQL\_ATTR\_DISCONNECT\_BEHAVIOR SQL\_ATTR\_CONNECTION\_TIMEOUT|SQL\_ATTR\_LOGIN\_TIMEOUT|SQL\_ATTR\_ODBC\_CURSORS|  
    |SQL\_COPT\_SS\_PERF\_DATA|SQL\_COPT\_SS\_PERF\_DATA\_LOG|SQL\_COPT\_SS\_PERF\_DATA\_LOG\_NOW|  
    |SQL\_COPT\_SS\_PERF\_QUERY|SQL\_COPT\_SS\_PERF\_QUERY\_INTERVAL|SQL\_COPT\_SS\_PERF\_QUERY\_LOG|  
    |SQL\_COPT\_SS\_PRESERVE\_CURSORS|SQL\_COPT\_SS\_TRANSLATE|SQL\_COPT\_SS\_USER\_DATA|  
    |SQL\_COPT\_SS\_WARN\_ON\_CP\_ERROR|||  
  
## Siehe auch  
 [Microsoft ODBC Driver for SQL Server on Windows](../content/Microsoft-ODBC-Driver-for-SQL-Server-on-Windows.md)  
  
  