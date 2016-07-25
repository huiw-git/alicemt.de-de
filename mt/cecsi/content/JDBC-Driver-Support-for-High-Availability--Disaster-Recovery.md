---
title: "JDBC Driver-Unterst&#252;tzung f&#252;r hohe Verf&#252;gbarkeit, Notfallwiederherstellung"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 62de4be6-b027-427d-a7e5-352960e42877
caps.latest.revision: 40
caps.handback.revision: 35
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
  - sv-se
  - zh-cn
  - zh-tw
---
# JDBC Driver-Unterst&#252;tzung f&#252;r hohe Verf&#252;gbarkeit, Notfallwiederherstellung
  In diesem Thema wird die [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-Unterstützung für hohe Verfügbarkeit und Notfallwiederherstellung \([!INCLUDE[ssHADR](../content/includes/ssHADR_md.md)]\) behandelt. Weitere Informationen zu [!INCLUDE[ssHADR](../content/includes/ssHADR_md.md)] finden Sie in der [!INCLUDE[ssSQL11](../content/includes/ssSQL11_md.md)]\-Onlinedokumentation.  
  
 Ab Version 4.0 von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] können Sie den Verfügbarkeitsgruppen\-Listener einer Verfügbarkeitsgruppe \(hohe Verfügbarkeit, Notfallwiederherstellung\) in der Verbindungseigenschaft angeben. Wenn eine [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-Anwendung mit einer AlwaysOn\-Datenbank verbunden ist, für die ein Failover ausgeführt wird, wird die ursprüngliche Verbindung unterbrochen, und die Anwendung muss eine neue Verbindung öffnen, damit ihre Ausführung nach dem Failover fortgesetzt werden kann.  
  
 Wenn Sie keine Verbindung mit einem Verfügbarkeitsgruppen\-Listener herstellen und einem Server mehrere IP\-Adressen zugeordnet sind, versucht [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)], eine Verbindung mit der ersten IP\-Adresse herzustellen. Wenn [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] keine Verbindung mit der ersten IP\-Adresse herstellen kann, tritt ein Verbindungsfehler auf.[!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] versucht nicht, eine Verbindung mit einer der nachfolgenden IP\-Adressen herzustellen, die dem Server zugeordnet sind. Beim Herstellen einer Verbindung mit einem Verfügbarkeitsgruppen\-Listener versucht [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)], gleichzeitig Verbindungen mit sämtlichen IP\-Adressen herzustellen. Bei einem erfolgreichen Versuch verwirft der Treiber alle ausstehenden Verbindungsversuche.  
  
> [!NOTE]  
>  Das Erhöhen des Verbindungstimeouts sowie die Implementierung von Verbindungswiederholungslogik erhöhen die Wahrscheinlichkeit, dass eine Anwendung eine Verbindung zu einer Verfügbarkeitsgruppe herstellt. Da zudem eine Verbindung aufgrund eines Verfügbarkeitsgruppenfailovers fehlschlagen kann, empfiehlt sich die Implementierung von Verbindungswiederholungslogik, wodurch im Fall einer fehlgeschlagenen Verbindung bis zur erneuten Verbindung Wiederholungsversuche erfolgen.  
  
 Die folgenden [Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md) wurden in [!INCLUDE[jdbc_40](../content/includes/jdbc_40_md.md)] eingeführt:  
  
-   **multiSubnetFailover**  
  
-   **applicationIntent**  
  
## Verbinden mit MultiSubnetFailover  
 Geben Sie immer **multiSubnetFailover\=true** an, wenn Sie eine Verbindung mit dem [!INCLUDE[ssSQL11](../content/includes/ssSQL11_md.md)] Verfügbarkeitsgruppenlistener oder einem [!INCLUDE[ssSQL11](../content/includes/ssSQL11_md.md)] Failovercluster\-Verfügbarkeitsgruppenlistener herstellen.**multiSubnetFailover** ermöglicht einen schnelleren Failover für alle Verfügbarkeitsgruppen und Failoverclusterinstanzen in [!INCLUDE[ssSQL11](../content/includes/ssSQL11_md.md)] und verringert die Failoverzeit für AlwaysOn\-Topologien mit einem oder mehreren Subnetzen deutlich. Während eines Multisubnetzfailovers versucht der Client Verbindungen parallel. Während eines Subnetz\-Failovers unternimmt [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] aggressive Wiederholungsversuche zum Herstellen der TCP\-Verbindung.  
  
 Die **multiSubnetFailover**\-Verbindungseigenschaft gibt an, dass die Anwendung in einer Verfügbarkeitsgruppe oder Failover\-Clusterinstanz bereitgestellt wird und dass [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] versucht, eine Verbindung mit der Datenbank der primären [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Instanz herzustellen, indem Verbindungen mit allen IP\-Adressen hergestellt werden. Wenn **MultiSubnetFailover\=true** für eine Verbindung angegeben wird, wiederholt der Client TCP\-Verbindungsversuche schneller als dies bei den standardmäßigen TCP\-Neuübertragungsintervallen des Betriebssystems der Fall ist. Auf diese Weise kann die Verbindung nach einem Failover einer AlwaysOn\-Verfügbarkeitsgruppe oder einer AlwaysOn\-Failoverclusterinstanz schneller wiederhergestellt werden. Diese Einstellung gilt sowohl für Einzelsubnetz\- als auch Multisubnetz\-Verfügbarkeitsgruppen und \-Failoverclusterinstanzen.  
  
 Weitere Informationen zu Schlüsselwörtern der Verbindungszeichenfolge in [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] finden Sie unter [Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md).  
  
 Das Angeben von **multiSubnetFailover\=true** für ein anderes Verbindungsziel als einen Verfügbarkeitsgruppenlistener oder eine Failoverclusterinstanz kann die Leistung beeinträchtigen und wird nicht unterstützt.  
  
 Wenn der Sicherheits\-Manager nicht installiert ist, werden virtuelle IP\-Adressen \(VIPs\) von der Java Virtual Machine für einen begrenzten Zeitraum zwischengespeichert. Die jeweilige Dauer wird durch Ihre JDK\-Implementierung und die Java\-Eigenschaften networkaddress.cache.ttl und networkaddress.cache.negative.ttl bestimmt. Wenn der JDK\-Sicherheits\-Manager installiert ist, werden VIPs von der Java Virtual Machine zwischengespeichert, und der Cache wird standardmäßig nicht aktualisiert. Es empfiehlt sich die Gültigkeitsdauer, d. h. "time\-to\-live" \(networkaddress.cache.ttl\), für den Cache der Java Virtual Machine auf einen Tag festzulegen. Wenn Sie den Standardwert nicht auf einen Tag oder eine ähnliche Einstellung festlegen, wird der alte Wert beim Hinzufügen oder Aktualisieren einer VIP nicht aus dem Java Virtual Machine\-Cache gelöscht. Weitere Informationen zu networkaddress.cache.ttl und networkaddress.cache.negative.ttl, finden Sie unter [http:\/\/download.oracle.com\/javase\/6\/docs\/technotes\/guides\/net\/properties.html](http://download.oracle.com/javase/6/docs/technotes/guides/net/properties.html).  
  
 Befolgen Sie beim Herstellen einer Verbindung mit einem Server in einer Verfügbarkeitsgruppe oder einer Failoverclusterinstanz die folgenden Richtlinien:  
  
-   Der Treiber generiert einen Fehler, wenn die **instanceName**\-Verbindungseigenschaft in derselben Verbindungszeichenfolge wie die **multiSubnetFailover**\-Verbindungseigenschaft verwendet wird. Dies spiegelt den Umstand wider, dass der SQL Browser\-Dienst in Verfügbarkeitsgruppen nicht verwendet wird. Wenn jedoch die **portNumber**\-Verbindungseigenschaft ebenfalls angegeben wird, ignoriert der Treiber **instanceName** und verwendet **portNumber**.  
  
-   Verwenden Sie die **multiSubnetFailover**\-Verbindungseigenschaft, wenn Sie eine Verbindung mit einem Single\-Subnetz oder einem Multi\-Subnetz herstellen; die Leistung wird in beiden Fällen verbessert.  
  
-   Um eine Verbindung mit einer Verfügbarkeitsgruppe herzustellen, geben Sie in der Verbindungszeichenfolge den Verfügbarkeitsgruppenlistener der Verfügbarkeitsgruppe als Server an. Beispiel: jdbc:sqlserver:\/\/VNN1.  
  
-   Ein Verbindungsversuch mit einer mit mehr als 64 IP\-Adressen konfigurierten [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Instanz verursacht einen Verbindungsfehler.  
  
-   Das Verhalten einer Anwendung, die die **multiSubnetFailover**\-Verbindungseigenschaft verwendet, wird nicht vom Authentifizierungstyp beeinflusst: [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Authentifizierung, Kerberos\-Authentifizierung oder Windows\-Authentifizierung.  
  
-   Vergrößern Sie den Wert von **loginTimeout**, um eine ausreichende Failoverzeit zu konfigurieren und die Anzahl der Verbindungsherstellungsversuche der Anwendung zu reduzieren.  
  
-   Verteilte Transaktionen werden nicht unterstützt.  
  
 Wenn das schreibgeschützte Routing nicht aktiviert ist, scheitert das Herstellen der Verbindung mit einem sekundären Replikatspeicherort in einer Verfügbarkeitsgruppe in den folgenden Situationen:  
  
1.  Wenn der sekundäre Replikatspeicherort nicht zum Akzeptieren von Verbindungen konfiguriert ist.  
  
2.  Wenn eine Anwendung **applicationIntent\=ReadWrite** verwendet \(weiter unten erläutert\), und der sekundäre Replikatspeicherort für schreibgeschützten Zugriff konfiguriert ist.  
  
 Es kann keine Verbindung hergestellt werden, wenn ein primäres Replikat so konfiguriert ist, dass schreibgeschützte Arbeitslasten abgelehnt werden, und die Verbindungszeichenfolge **ApplicationIntent\=ReadOnly** enthält.  
  
## Aktualisieren zur Verwendung von Multisubnetzclustern aus Datenbankspiegelung  
 Wenn Sie für eine [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-Anwendung, die derzeit die Datenbankspiegelung verwendet, ein Upgrade auf ein Multi\-Subnetz\-Szenario ausführen, müssen Sie die **failoverPartner**\-Verbindungseigenschaft entfernen und durch **multiSubnetFailover** ersetzen \(festgelegt auf **true**\); der Servername in der Verbindungszeichenfolge muss durch einen Verfügbarkeitsgruppen\-Listener ersetzt werden. Wenn eine Verbindungszeichenfolge **failoverPartner** und **multiSubnetFailover\=true** verwendet, generiert der Treiber einen Fehler. Wenn eine Verbindungszeichenfolge jedoch **failoverPartner** und **multiSubnetFailover\=false** \(oder **ApplicationIntent\=ReadWrite**\) verwendet, verwendet die Anwendung Datenbankspiegelung.  
  
 Der Treiber gibt einen Fehler zurück, wenn die Datenbankspiegelung für die primäre Datenbank in der Verfügbarkeitsgruppe verwendet wird und wenn **multiSubnetFailover\=true** in der Verbindungszeichenfolge angegeben ist, wodurch eine Verbindung mit einer primären Datenbank und nicht mit einem Verfügbarkeitsgruppen\-Listener hergestellt wird.  
  
## Angeben des Anwendungszwecks  
 Wenn **applicationIntent\=ReadOnly** festgelegt ist, fordert der Client beim Herstellen einer Verbindung mit einer AlwaysOn\-fähigen Datenbank eine schreibgeschützte Arbeitslast. Der Server erzwingt den Zweck zur Verbindungszeit und während einer USE\-Datenbankanweisung, jedoch lediglich für eine AlwaysOn\-fähige Datenbank.  
  
 Das **applicationIntent**\-Schlüsselwort funktioniert nicht mit schreibgeschützten Legacy\-Datenbanken.  
  
 Eine Datenbank kann Lesearbeitslasten auf der AlwaysOn\-Zieldatenbank zulassen bzw. nicht zulassen. \(Dies geschieht über die **ALLOW\_CONNECTIONS**\-Klausel der **PRIMARY\_ROLE**\- und **SECONDARY\_ROLE**[!INCLUDE[tsql](../content/includes/tsql_md.md)]\-Anweisungen.\)  
  
 Das **applicationIntent**\-Schlüsselwort wird verwendet, um schreibgeschütztes Routing zu aktivieren.  
  
## Schreibgeschütztes Routing  
 Das schreibgeschützte Routing ist eine Funktion, die die Verfügbarkeit des schreibgeschützten Replikats einer Datenbank sicherstellen kann. So aktivieren Sie schreibgeschütztes Routing:  
  
1.  Sie müssen eine Verbindung mit dem Verfügbarkeitsgruppen\-Listener einer AlwaysOn\-Verfügbarkeitsgruppe herstellen.  
  
2.  Das Schlüsselwort der **applicationIntent**\-Verbindungszeichenfolge muss auf **ReadOnly** festgelegt werden.  
  
3.  Die Verfügbarkeitsgruppe muss vom Datenbankadministrator konfiguriert werden, um schreibgeschütztes Routing zu aktivieren.  
  
 Möglicherweise werden bei mehreren Verbindungen mithilfe von schreibgeschütztem Routing nicht alle mit demselben schreibgeschützten Replikat verbunden. Änderungen in der Datenbanksynchronisierung oder Änderungen in der Routingkonfiguration des Servers können zu Clientverbindungen mit anderen schreibgeschützten Replikaten führen. Um sicherzustellen, dass von allen Schreibschutzanforderungen Verbindungen mit demselben schreibgeschützten Replikat hergestellt werden, übergeben Sie an das **serverName**\-Schlüsselwort der Verbindungszeichenfolge keinen Verfügbarkeitsgruppen\-Listener und keine virtuelle IP\-Adresse. Geben Sie stattdessen den Namen der schreibgeschützten Instanz an.  
  
 Das schreibgeschützte Routing kann länger als das Herstellen einer Verbindung mit dem primären Objekt dauern, da beim schreibgeschützten Routing zunächst eine Verbindung mit dem primären Objekt hergestellt und anschließend nach dem verfügbaren am besten lesbaren sekundären Objekt gesucht wird. Deswegen sollten Sie das Anmeldetimeout vergrößern.  
  
## Neue Methoden, die multiSubnetFailover und applicationIntent unterstützen  
 Die folgenden Methoden ermöglichen den programmgesteuerten Zugriff auf das **multiSubnetFailover**\-Schlüsselwort und das **applicationIntent**\-Schlüsselwort der Verbindungszeichenfolge:  
  
-   [SQLServerDataSource.getApplicationIntent](../content/getApplicationIntent-Method--SQLServerDataSource-.md)  
  
-   [SQLServerDataSource.setApplicationIntent](../content/setApplicationIntent-Method--SQLServerDataSource-.md)  
  
-   [SQLServerDataSource.getMultiSubnetFailover](../content/getMultiSubnetFailover-Method--SQLServerDataSource-.md)  
  
-   [SQLServerDataSource.setMultiSubnetFailover](../content/setMultiSubnetFailover-Method--SQLServerDataSource-.md)  
  
-   [SQLServerDriver.getPropertyInfo](../content/getPropertyInfo-Method--SQLServerDriver-.md)  
  
 Die Methoden **getMultiSubnetFailover**, **setMultiSubnetFailover**, **getApplicationIntent** und **setApplicationIntent** werden ebenfalls [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md), [SQLServerConnectionPoolDataSource-Klasse](../content/SQLServerConnectionPoolDataSource-Class.md) und [SQLServerXADataSource-Klasse](../content/SQLServerXADataSource-Class.md) hinzugefügt.  
  
## Überprüfen des SSL\-Serverzertifikats  
 Eine Verfügbarkeitsgruppe besteht aus mehreren physischen Servern. In [!INCLUDE[jdbc_40](../content/includes/jdbc_40_md.md)] wird die Unterstützung für **Subject Alternate Name** in SSL\-Zertifikaten eingeführt, sodass einem Zertifikat mehrere Hosts zugeordnet werden können. Weitere Informationen zu SSL finden Sie unter [Grundlegendes zur SSL-Unterstützung](../content/Understanding-SSL-Support.md).  
  
## Siehe auch  
 [Verbinden von SQL Server mit dem JDBC-Treiber](../content/Connecting-to-SQL-Server-with-the-JDBC-Driver.md)   
 [Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md)  
  
  