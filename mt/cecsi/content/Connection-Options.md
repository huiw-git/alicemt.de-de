---
title: "Verbindungsoptionen"
ms.custom: na
ms.date: 07/18/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6d1ea295-8e34-438e-8468-4bbc0f76192c
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
# Verbindungsoptionen
In diesem Thema werden die Optionen aufgelistet, die im assoziativen Array zulässig sind \(bei Verwendung von [sqlsrv_connect](../content/sqlsrv_connect.md) im SQLSRV-Treiber\), oder die Schlüsselwörter, die im Datenquellennamen \(dsn\) zulässig sind \(bei Verwendung von [PDO::__construct](../Topic/PDO::__construct.md) im PDO\_SQLSRV-Treiber\).  
  
|Key|Wert|Beschreibung|Standardwert|  
|-------|---------|---------------|-----------|  
|APP|String|Gibt den Namen der Anwendung an, der in der Ablaufverfolgung verwendet wird.|Kein Wert festgelegt.|  
|ApplicationIntent|String|Deklariert den Arbeitsauslastungstyp der Anwendung beim Herstellen einer Verbindung mit einem Server. Mögliche Werte sind „ReadOnly“ und „ReadWrite“.<br /><br />Weitere Informationen zur [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]-Unterstützung für [!INCLUDE[ssHADR](../content/includes/ssHADR_md.md)] finden Sie unter [PHP Driver for SQL Server Support for High Availability, Disaster Recovery (Unterstützung für hohe Verfügbarkeit im PHP-Treiber für SQL Server, Notfallwiederherstellung)](../Topic/PHP%20Driver%20for%20SQL%20Server%20Support%20for%20High%20Availability,%20Disaster%20Recovery.md).|ReadWrite|  
|AttachDBFileName|String|Gibt an, welche Datenbankdatei der Server anfügen soll.|Kein Wert festgelegt.|  
|CharacterSet<br /><br />\(vom PDO\_SQLSRV-Treiber nicht unterstützt\)|String|Gibt den Zeichensatz an, mit dem Daten an den Server gesendet werden.<br /><br />Die möglichen Werte sind SQLSRV\_ENC\_CHAR und UTF\-8. Weitere Informationen finden Sie unter [How to: Send and Retrieve UTF-8 Data Using Built-In UTF-8 Support](../Topic/How%20to:%20Send%20and%20Retrieve%20UTF-8%20Data%20Using%20Built-In%20UTF-8%20Support.md).|SQLSRV\_ENC\_CHAR|  
|ConnectionPooling|1 oder **true** , um Verbindungspooling zu aktivieren.<br /><br />0 oder **false** , um Verbindungspooling zu deaktivieren.|Gibt an, ob die Verbindung aus einem Verbindungspool zugewiesen wird \(1 oder **true**\) oder nicht \(0 oder **false**\).|**true** \(1\)|  
|Datenbank|String|Gibt den Namen der Datenbank an, zu der die Verbindung aufgebaut werden soll<sup>1</sup>.|Die Standarddatenbank, die für die Anmeldung verwendet wird.|  
|Encrypt|1 oder **true** , um Verschlüsselung zu aktivieren.<br /><br />0 oder **false** , um Verschlüsselung zu deaktivieren.|Gibt an, ob die Kommunikation mit SQL Server verschlüsselt \(1 oder **true**\) oder unverschlüsselt \(0 oder **false**\)<sup>2</sup> ist.|**false** \(0\)|  
|Failover\_Partner|String|Gibt den Server und die Instanz der Spiegelung der Datenbank an \(sofern aktiviert und konfiguriert\), die verwendet werden soll, wenn der primäre Server nicht verfügbar ist.<br /><br />Es gibt Einschränkungen für die Verwendung von Failover\_Partner mit MultiSubnetFailover. Weitere Informationen finden Sie unter [Unterstützung für hohe Verfügbarkeit im PHP-Treiber für SQL Server, Notfallwiederherstellung](../Topic/PHP%20Driver%20for%20SQL%20Server%20Support%20for%20High%20Availability,%20Disaster%20Recovery.md) ( PHP Driver for SQL Server Support for High Availability, Disaster Recovery).|Kein Wert festgelegt.|  
|LoginTimeout|Integer \(SQLSRV-Treiber<br /><br />Zeichenfolge \(PDO\_SQLSRV-Treiber|Legt die Wartezeit in Sekunden fest, bevor der Verbindungsversuch fehlschlägt.|Kein Timeout.|  
|MultipleActiveResultSets|1 oder **true** zum Verwenden von mehreren aktiven Resultsets.<br /><br />0 oder **false** zum Deaktivieren von mehreren aktiven Resultsets.|Deaktiviert oder aktiviert explizit die Unterstützung für mehrere aktive Resultsets \(MARS\).<br /><br />Weitere Informationen finden Sie unter [Gewusst wie: Deaktivieren von mehreren aktiven Resultsets &#40;MARS&#41;](../Topic/How%20to:%20Disable%20Multiple%20Active%20Resultsets%20(MARS).md).|true \(1\)|  
|MultiSubnetFailover|String|Geben Sie immer **multiSubnetFailover\=yes** an, wenn Sie eine Verbindung mit dem Verfügbarkeitsgruppenlistener einer [!INCLUDE[ssSQL11](../content/includes/ssSQL11_md.md)]-Verfügbarkeitsgruppe oder einer [!INCLUDE[ssSQL11](../content/includes/ssSQL11_md.md)]-Failoverclusterinstanz herstellen. **multiSubnetFailover\=yes** konfiguriert [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)], um eine schnellere Erkennung sowie die Verbindung zu dem \(gerade\) aktiven Server zu gewährleisten. Mögliche Werte sind Yes und No.<br /><br />Weitere Informationen zur [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]-Unterstützung für [!INCLUDE[ssHADR](../content/includes/ssHADR_md.md)] finden Sie unter [PHP Driver for SQL Server Support for High Availability, Disaster Recovery (Unterstützung für hohe Verfügbarkeit im PHP-Treiber für SQL Server, Notfallwiederherstellung)](../Topic/PHP%20Driver%20for%20SQL%20Server%20Support%20for%20High%20Availability,%20Disaster%20Recovery.md).|Nein|  
|PWD<br /><br />\(vom PDO\_SQLSRV-Treiber nicht unterstützt\)|String|Gibt das Kennwort für die Benutzer-ID an, die bei der Verbindung mit SQL Server-Authentifizierung<sup>3</sup>verwendet wird.|Kein Wert festgelegt.|  
|QuotedId|1 oder **true**, um SQL\-92-Regeln zu verwenden.<br /><br />0 oder **false** , um Legacy-Regeln zu verwenden.|Gibt an, ob SQL\-92-Regeln für Bezeichner in Anführungszeichen \(1 oder **true**\) oder ältere Transact\-SQL-Regeln \(0 oder **false**\) verwendet werden sollen.|**true** \(1\)|  
|ReturnDatesAsStrings<br /><br />\(vom PDO\_SQLSRV-Treiber nicht unterstützt\)|1 oder **true** , um Datums- und Uhrzeittypen als Zeichenfolgen zurückzugeben.<br /><br />0 oder **false** um Datums- und Uhrzeittypen als PHP **DateTime** - Typen zurückzugeben.|Ruft Datums- und Uhrzeittypen \(datetime, date, time, datetime2 und datetimeoffset\) als Zeichenfolgen oder als PHP-Typen ab. Wenn Sie den PDO\_SQLSRV-Treiber verwenden, werden Datumsangaben als Zeichenfolgen zurückgegeben. Der PDO\_SQLSRV-Treiber hat keinen **datetime**-Typ.<br /><br />Weitere Informationen finden Sie unter [So wird's gemacht: Datums- und Uhrzeittypen mittels des SQLSRV-Treibers als Zeichenfolgen abrufen](../Topic/How%20to:%20Retrieve%20Date%20and%20Time%20Type%20as%20Strings%20Using%20the%20SQLSRV%20Driver.md).|**false**|  
|Bildlauffähigkeit|String|„gepuffert“ bedeutet, dass Sie einen clientseitigen \(gepufferten\) Cursor möchten, mit dem Sie ein komplettes Resultset im Arbeitsspeicher zwischenspeichern können. Weitere Informationen finden Sie unter [Cursortypen &#40;SQLSRV-Treiber&#41;](../Topic/Cursor%20Types%20(SQLSRV%20Driver).md).|Vorwärtsgerichteter Cursor|  
|Server<br /><br />\(vom SQLSRV-Treiber nicht unterstützt\)|String|Die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Instanz, mit der eine Verbindung hergestellt werden soll.<br /><br />Sie können auch einen virtuellen Netzwerknamen angeben, um eine Verbindung mit einer AlwaysOn-Availability-Gruppe herzustellen. Weitere Informationen zur [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]-Unterstützung für [!INCLUDE[ssHADR](../content/includes/ssHADR_md.md)] finden Sie unter [PHP Driver for SQL Server Support for High Availability, Disaster Recovery (Unterstützung für hohe Verfügbarkeit im PHP-Treiber für SQL Server, Notfallwiederherstellung)](../Topic/PHP%20Driver%20for%20SQL%20Server%20Support%20for%20High%20Availability,%20Disaster%20Recovery.md).|„Server“ ist ein erforderliches Schlüsselwort \(wobei es nicht das erste Schlüsselwort in der Verbindungszeichenfolge sein muss\). Wenn kein Servername an das Schlüsselwort übergeben wird, wird versucht, eine Verbindung mit der lokalen Instanz herzustellen.<br /><br />Der an „Server“ übergebene Wert kann der Name einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Instanz oder die IP-Adresse der Instanz sein. Sie können optional eine Portnummer angeben \(z. B. `sqlsrv:server=(local),1033`\).<br /><br />Ab Version 3.0 der [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] können Sie auch eine LocalDB-Instanz mit `server=(localdb)\instancename`angeben. Weitere Informationen finden Sie unter [PHP Driver for SQL Server Support for LocalDB](../Topic/PHP%20Driver%20for%20SQL%20Server%20Support%20for%20LocalDB.md).|  
|TraceFile|String|Gibt den Pfad für die Datei an, die für Ablaufverfolgungsdaten verwendet wird.|Kein Wert festgelegt.|  
|TraceOn|1 oder **true** zum Aktivieren der Ablaufverfolgung.<br /><br />0 oder **false** zum Deaktivieren der Ablaufverfolgung.|Gibt an, ob für die herzustellende Verbindung die ODBC-Protokollierung aktiviert \(1 oder **true**\) oder deaktiviert \(0 oder **false**\) ist.|**false** \(0\)|  
|TransactionIsolation|Der SQLSRV-Treiber verwendet die folgenden Werte:<br /><br />SQLSRV\_TXN\_READ\_UNCOMMITTED<br /><br />SQLSRV\_TXN\_READ\_COMMITTED<br /><br />SQLSRV\_TXN\_REPEATABLE\_READ<br /><br />SQLSRV\_TXN\_SNAPSHOT<br /><br />SQLSRV\_TXN\_SERIALIZABLE<br /><br />Der PDO\_SQLSRV-Treiber verwendet die folgenden Werte:<br /><br />PDO::SQLSRV\_TXN\_READ\_UNCOMMITTED<br /><br />PDO::SQLSRV\_TXN\_READ\_COMMITTED<br /><br />PDO::SQLSRV\_TXN\_REPEATABLE\_READ<br /><br />PDO::SQLSRV\_TXN\_SNAPSHOT<br /><br />PDO::SQLSRV\_TXN\_SERIALIZABLE|Bestimmt die Isolationsstufe für die Transaktionen.<br /><br />Weitere Informationen zur Transaktionsisolation, finden Sie unter [SET TRANSACTION ISOLATION LEVEL](http://go.microsoft.com/fwlink/?LinkID=191497) in der SQL Server-Dokumentation.|SQLSRV\_TXN\_READ\_COMMITTED<br /><br />oder<br /><br />PDO::SQLSRV\_TXN\_READ\_COMMITTED|  
|TrustServerCertificate|1 oder **true** , um dem Zertifikat zu vertrauen.<br /><br />0 oder **false** , um dem Zertifikat nicht zu vertrauen.|Gibt an, ob der Client einem selbstsignierten Serverzertifikat vertrauen \(1 oder **true**\) oder es ablehnen soll \(0 oder **false**\).|**false** \(0\)|  
|UID<br /><br />\(vom PDO\_SQLSRV-Treiber nicht unterstützt\)|String|Gibt die Benutzer-ID an, die bei der Verbindung mit SQL Server-Authentifizierung<sup>3</sup>verwendet wird.|Kein Wert festgelegt.|  
|WSID|String|Gibt den Namen des Computers für die Ablaufverfolgung an.|Kein Wert festgelegt.|  
  
1. Alle für die hergestellte Verbindung ausgeführten Abfragen werden auf der Datenbank ausgeführt, die durch das *Database*-Attribut festgelegt ist. Allerdings kann auf Daten in anderen Datenbanken zugegriffen werden, indem ein vollqualifizierter Name verwendet wird, wenn der Benutzer über die entsprechenden Berechtigungen verfügt. Wenn beispielsweise die *master*-Datenbank mit dem *Database*-Verbindungsattribut festgelegt wird, ist es weiterhin möglich, eine Transact\-SQL-Abfrage auszuführen, die mit dem vollqualifizierten Namen auf die *AdventureWorks.HumanResources.Employee*\-Tabelle zugreift.  
  
2. Aktivieren von *Verschlüsselung* beeinträchtigt die Leistung einiger Anwendungen aufgrund des aufwändigen Berechnungsprozesses, der erforderlich ist, um Daten zu verschlüsseln.  
  
3. Die *UID* -Authentifizierung müssen sowohl das *PWD* - als auch das [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Attribut festgelegt sein.  
  
Viele der unterstützten Schlüssel sind ODBC-Verbindungszeichenfolgen-Attribute. Informationen zu ODBC-Verbindungszeichenfolgen finden Sie unter [Schlüsselwörter für Verbindungszeichenfolgen mit SQL Native Client benutzen](http://go.microsoft.com/fwlink/?LinkId=105504).  
  
## Siehe auch  
[Verbinden mit dem Server](../content/Connecting-to-the-Server.md)  
  
