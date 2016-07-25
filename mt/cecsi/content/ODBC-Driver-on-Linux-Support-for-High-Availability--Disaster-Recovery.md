---
title: "ODBC-Treiber mit der Linux-Unterst&#252;tzung f&#252;r hohe Verf&#252;gbarkeit, Notfallwiederherstellung"
ms.custom: na
ms.date: 06/09/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fa656c5b-a935-40bf-bc20-e517ca5cd0ba
caps.latest.revision: 16
caps.handback.revision: 12
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
# ODBC-Treiber mit der Linux-Unterst&#252;tzung f&#252;r hohe Verf&#252;gbarkeit, Notfallwiederherstellung
Der ODBC\-Treiber für Linux unterstützt [!INCLUDE[ssHADR](../content/includes/ssHADR_md.md)]. Weitere Informationen zu [!INCLUDE[ssHADR](../content/includes/ssHADR_md.md)] finden Sie hier:  
  
-   [Verfügbarkeitsgruppenlistener, Clientkonnektivität und Anwendungsfailover \(SQL Server\)](http://msdn.microsoft.com/library/hh213417.aspx)  
  
-   [Erstellung und Konfiguration von Verfügbarkeitsgruppen \(SQL Server\)](http://msdn.microsoft.com/library/ff878265.aspx)  
  
-   [Failoverclustering und AlwaysOn\-Verfügbarkeitsgruppen \(SQL Server\)](http://msdn.microsoft.com/library/ff929171.aspx)  
  
-   [Aktive sekundäre Replikate: Lesbare sekundäre Replikate \(AlwaysOn\-Verfügbarkeitsgruppen\)](http://msdn.microsoft.com/library/ff878253.aspx)  
  
Sie können den Verfügbarkeitsgruppenlistener einer bestimmten Verfügbarkeitsgruppe in der Verbindungszeichenfolge angeben. Falls ein OBCD\-Treiber auf einer Linux\-Anwendung mit einer Datenbank in einer Verfügbarkeitsgruppe verbunden ist, die einen Failover ausführt, wird die ursprüngliche Verbindung getrennt.  Die Anwendung muss dann eine neue Verbindung herstellen, um nach dem Failover weiterzuarbeiten.  
  
Der ODBC\-Treiber für Linux iteriert sequentiell durch alle IP\-Adressen, die einem DNS\-Eintrag zugeordneten sind, falls:  
  
-   Sie sind mit keinem Verfügbarkeitsgruppenlistener verbunden. Und  
  
-   einem Hostnamen mehrere IP\-Adressen zugeordnet sind.  
  
Diese Iterationen können zeitaufwendig sein, falls die erste vom DNS\-Server zurückgegebene IP\-Adresse an keine Netzwerkschnittstellenkarte gebunden ist.  Beim Verbinden mit einem Verfügbarkeitsgruppenlistener versucht der ODBC\-Treiber in Linux mit allen IP\-Adressen parallel Verbindungen herzustellen. Falls ein Verbindungsversuch erfolgreich war, bricht der Treiber alle weiteren laufenden Verbindungsversuche ab.  
  
> [!NOTE]  
> Das Erhöhen des Verbindungstimeouts sowie die Implementierung einer Verbindungswiederholungslogik erhöhen die Chance auf eine Verbindung mit der Verfügbarkeitsgruppe. Da zudem eine Verbindung aufgrund eines Verfügbarkeitsgruppenfailovers fehlschlagen kann, empfiehlt sich die Implementierung einer Verbindungswiederholungslogik, wodurch im Fall einer fehlgeschlagenen Verbindung bis zur erneuten Verbindung Wiederholungsversuche erfolgen.  
  
## Verbinden mit MultiSubnetFailover  
Geben Sie immer **MultiSubnetFailover\=Yes** \(oder **\=True**\) an, wenn Sie eine Verbindung mit einem [!INCLUDE[ssSQL11](../content/includes/ssSQL11_md.md)]Verfügbarkeitsgruppenlistener oder einer [!INCLUDE[ssSQL11](../content/includes/ssSQL11_md.md)] Failoverclusterinstanz herstellen. **MultiSubnetFailover** ermöglicht für alle Verfügbarkeitsgruppen und Failoverclusterinstanzen in [!INCLUDE[ssSQL11](../content/includes/ssSQL11_md.md)] ein schnelleres Failover.**MultiSubnetFailover** reduziert auch die Failoverzeit für Einzel\- und Multisubnetz AlwaysOn\-Topologien. Während eines Multisubnetzfailovers versucht der Client, Verbindungen parallel herzustellen. Während eines Subnetzfailovers versucht der ODBC\-Treiber energisch, die TCP\-Verbindung wiederherzustellen.  
  
Die **MultiSubnetFailover**\-Verbindungseigenschaft zeigt an, dass die Anwendung in einer Verfügbarkeitsgruppe oder einer Failoverclusterinstanz bereitgestellt wird. Der ODBC\-Treiber für Linux versucht, sich mit der Datenbank auf der primären [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Instanz zu verbinden, indem er versucht, sich mit allen IP\-Adressen zu verbinden. Bei der Verbindung mit **MultiSubnetFailover\=Yes** wiederholt der Client die Verbindungsversuche mit der TCP\-Verbindung mit TCP\-Neuübertragungsintervallen, die kürzer sind, als vom Betriebssystem vorgegebenen.**MultiSubnetFailover\=Yes** ermöglicht eine schnellere Verbindungswiederherstellung nach dem Failover entweder einer AlwaysOn\-Verfügbarkeitsgruppe oder einer AlwaysOn\-Failoverclusterinstanz. **MultiSubnetFailover\=Yes** gelten sowohl für Einzel\- als auch Multisubnetzverfügbarkeitsgruppen und Failoverclusterinstanzen.  
  
Verwenden Sie **MultiSubnetFailover\=Yes** wenn Sie eine Verbindung mit einem Verfügbarkeitsgruppenlistener oder einer Failoverclusterinstanz herstellen. Andernfalls kann die Leistung Ihrer Anwendung negativ beeinträchtigt werden.  
  
Zum Herstellen einer Verbindung mit einem Server in einer Verfügbarkeitsgruppe oder einer Failoverclusterinstanz:  
  
-   **MultiSubnetFailover** verbessert die Leistung bei der Verbindung mit einem einzelnen Subnetz oder einem Multisubnetz.  
  
-   Um eine Verbindung mit einer Verfügbarkeitsgruppe herzustellen, geben Sie in der Verbindungszeichenfolge den Verfügbarkeitsgruppenlistener der Verfügbarkeitsgruppe als Server an.  
  
-   Sie können keine Verbindung mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Instanz herstellen, die mit mehr als 64 IP\-Adressen konfiguriert ist.  
  
-   Das Verhalten einer Anwendung, welche die **MultiSubnetFailover**\-Verbindungseigenschaft  verwendet, wird nicht vom Authentifizierungstyp beeinflusst: [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Authentifizierung oder Kerberos\-Authentifizierung.  
  
-   Sie können den Wert von **loginTimeout** erhöhen, um die Failoverzeit zu berücksichtigen und die Anzahl der von der Anwendung durchgeführten Verbindungsversuche zu reduzieren.  
  
-   Verteilte Transaktionen werden nicht unterstützt.  
  
Wenn das schreibgeschützte Routing nicht aktiviert ist, scheitert die Verbindungsherstellung mit einem sekundären Replikatspeicherort in einer Verfügbarkeitsgruppe in den folgenden Situationen:  
  
1.  Wenn der sekundäre Replikatspeicherort nicht zum Akzeptieren von Verbindungen konfiguriert ist.  
  
2.  Wenn eine Anwendung **ApplicationIntent\=ReadWrite** verwendet wird und der sekundäre Replikatspeicherort für den schreibgeschützten Zugriff konfiguriert ist.  
  
Es kann keine Verbindung hergestellt werden, wenn ein primäres Replikat so konfiguriert ist, dass schreibgeschützte Arbeitsauslastungen abgelehnt werden und die Verbindungszeichenfolge **ApplicationIntent\=ReadOnly** enthält.  
  
## Angeben des Anwendungszwecks  
Im Fall von **ApplicationIntent\=ReadOnly** fordert der Client eine Lesearbeitslast an, wenn eine Verbindung mit einer AlwaysOn\-aktivierten Datenbank hergestellt wird. Der Server erzwingt den Versuch zur Verbindungszeit und während einer USE\-Datenbankanweisung, aber nur für eine AlwaysOn\-aktivierte Datenbank.  
  
Das Schlüsselwort **ApplicationIntent** funktioniert nicht mit schreibgeschützten Legacy\-Datenbanken.  
  
Eine Datenbank kann Lesearbeitslasten auf der AlwaysOn\-Zieldatenbank zulassen bzw. nicht zulassen. \(Verwenden Sie Klausel **ALLOW\_CONNECTIONS** der **PRIMARY\_ROLE** und **SECONDARY\_ROLE** [!INCLUDE[tsql](../content/includes/tsql_md.md)] \-Anweisungen.\)  
  
Das Schlüsselwort **ApplicationIntent** wird verwendet, um das schreibgeschützte Routing zu aktivieren.  
  
## Schreibgeschütztes Routing  
Das schreibgeschützte Routing ist eine Funktion, die die Verfügbarkeit des schreibgeschützten Replikats einer Datenbank sicherstellen kann. So aktivieren Sie schreibgeschütztes Routing:  
  
1.  Stellen Sie eine Verbindung zum Verfügbarkeitsgruppenlistener einer AlwaysOn\-Verfügbarkeitsgruppe her.  
  
2.  Das Verbindungszeichenfolge\-Schlüsselwort **ApplicationIntent**\- muss auf **ReadOnly** eingerichtet sein.  
  
3.  Der Datenbankadministrator muss die Verfügbarkeitsgruppe entsprechend konfigurieren, um schreibgeschütztes Routing zu aktivieren.  
  
Es ist möglich das mehrere Verbindungen die schreibgeschütztes Routing verwenden, mit verschiedenen schreibgeschützten Replikaten verbunden werden.  Änderungen in der Datenbanksynchronisierung oder Änderungen in der Routingkonfiguration des Servers können zu Clientverbindungen mit anderen schreibgeschützten Replikaten führen. Sie gewährleisten, dass alle schreibgeschützten Anforderungen Verbindungen mit demselben schreibgeschützten Replikat herstellen, indem Sie keinen Verfügbarkeitsgruppenlistener an das **Server**\-Verbindungsschlüsselwort übermitteln. Geben Sie stattdessen den Namen der schreibgeschützten Instanz an.  
  
Die Zeit bis zum Verbindungsaufbau ist beim schreibgeschützten Routing länger als beim Zugriff auf das primäre Replikat.  Erhöhen Sie deshalb Ihr Anmeldetimout. Schreibgeschütztes Routing verbindet sich zunächst mit dem primären Replikat und sucht dann nach dem besten verfügbaren lesbaren sekundären Replikat.  
  
## ODBC\-Syntax  
Zwei ODBC\-Verbindungszeichenfolgen\-Schlüsselwörter unterstützen [!INCLUDE[ssHADR](../content/includes/ssHADR_md.md)]:  
  
-   **ApplicationIntent**  
  
-   **MultiSubnetFailover**  
  
Weitere Informationen zu ODBC\-Verbindungszeichenfolgen\-Schlüsselwörter finden Sie unter [Schlüsselwörtern für Verbindungszeichenfolgen mit SQL Native Client verwenden](http://msdn.microsoft.com/library/ms130822.aspx).  
  
Die entsprechenden Verbindungseigenschaften sind:  
  
-   **SQL\_COPT\_SS\_APPLICATION\_INTENT**  
  
-   **SQL\_COPT\_SS\_MULTISUBNET\_FAILOVER**  
  
Weitere Informationen zu den ODBC\-Verbindungseigenschaften finden Sie unter [SQLSetConnectAttr](http://msdn.microsoft.com/library/ms131709.aspx).  
  
Ein ODBC\-Treiber auf einer Linux\-Anwendung die [!INCLUDE[ssHADR](../content/includes/ssHADR_md.md)] verwendet kann eine von zwei Funktionen verwenden um die Verbindung herzustellen:  
  
|Funktion|Beschreibung|  
|------------|----------------|  
|[SQLConnect](assetId:///6da74e3a-4388-4907-81cb-987389bae467)|**SQLConnect** unterstützt sowohl **ApplicationIntent** als auch **MultiSubnetFailover** über entweder den Namen der Datenquelle \(DSN\) oder die Verbindungseigenschaften.|  
|[SQLDriverConnect](assetId:///a1e38e2c-3a97-42d1-9c45-a0ca3282ffd1)|**SQLDriverConnect** unterstützt **ApplicationIntent** und **MultiSubnetFailover** durch Verbindungszeichenfolgen\-Schlüsselwörter,Verbindungseigenschaften oder DSN.|  
  
## Siehe auch  
[Microsoft ODBC Driver for SQL Server on Linux](../content/Microsoft-ODBC-Driver-for-SQL-Server-on-Linux.md)  
  
