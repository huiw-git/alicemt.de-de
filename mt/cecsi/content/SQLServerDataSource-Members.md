---
title: "SQLServerDataSource-Elemente"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7e749bc5-d765-4864-be2b-7822d4c20c09
caps.latest.revision: 43
caps.handback.revision: 42
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
# SQLServerDataSource-Elemente
  In den folgenden Tabellen sind die Elemente aufgeführt, die von der [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Klasse verfügbar gemacht werden.  
  
## Konstruktoren  
  
|Name|Beschreibung|  
|----------|------------------|  
|[SQLServerDataSource \(\)](../content/SQLServerDataSource-Constructor---.md)|Initialisiert eine neue Instanz der [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Klasse.|  
  
## Felder  
 Keine  
  
## Geerbte Felder  
 Keine  
  
## Methoden  
  
|Name|Beschreibung|  
|----------|------------------|  
|[getApplicationIntent](../content/getApplicationIntent-Method--SQLServerDataSource-.md)|Gibt den Wert der **applicationIntent**\-Verbindungseigenschaft zurück.|  
|[getApplicationName](../content/getApplicationName-Method--SQLServerDataSource-.md)|Gibt den Anwendungsnamen zurück.|  
|[getConnection](../content/getConnection-Method--SQLServerDataSource-.md)|Stellt eine Verbindung mit der Datenquelle her, für die dieses [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Objekt steht.|  
|[getDatabaseName](../content/getDatabaseName-Method--SQLServerDataSource-.md)|Gibt den Datenbanknamen zurück.|  
|[getEncrypt](../content/getEncrypt-Method--SQLServerDataSource-.md)|Gibt einen Wert vom Typ **Boolean** zurück, mit dem angegeben wird, ob die encrypt\-Eigenschaft aktiviert ist.|  
|[getDescription](../content/getDescription-Method--SQLServerDataSource-.md)|Gibt eine Beschreibung der Datenquelle zurück.|  
|[getFailoverPartner](../content/getFailoverPartner-Method--SQLServerDataSource-.md)|Gibt den Namen des Failoverservers zurück, der in einer Datenbankspiegelungskonfiguration verwendet wird.|  
|[getHostNameInCertificate](../content/getHostNameInCertificate-Method--SQLServerDataSource-.md)|Gibt den Hostnamen zurück, der bei der Überprüfung des Secure Sockets Layer \(SSL\)\-Zertifikats von SQL Server verwendet wird.|  
|[getInstanceName](../content/getInstanceName-Method--SQLServerDataSource-.md)|Gibt den Namen der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Instanz zurück.|  
|[getLastUpdateCount](../content/getLastUpdateCount-Method--SQLServerDataSource-.md)|Gibt einen Wert vom Typ **boolean** zurück, mit dem angegeben wird, ob die lastUpdateCount\-Eigenschaft aktiviert ist.|  
|[getLockTimeout](../content/getLockTimeout-Method--SQLServerDataSource-.md)|Gibt einen Wert vom Typ **int** zurück, mit dem angegeben wird, wie lange von der Datenbank bis zum Melden eines Sperrtimeouts gewartet wird \(in Millisekunden\).|  
|[getLoginTimeout](../content/getLoginTimeout-Method--SQLServerDataSource-.md)|Gibt die Anzahl von Sekunden zurück, die vom [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Objekt bei der Verbindungsherstellung gewartet wird.|  
|[getLogWriter](../content/getLogWriter-Method--SQLServerDataSource-.md)|Gibt einen Zeichenausgabedatenstrom für alle Protokollierungs\- und Ablaufverfolgungsmeldungen zurück.|  
|[getMultiSubnetFailover](../content/getMultiSubnetFailover-Method--SQLServerDataSource-.md)|Gibt den Wert der **multiSubnetFailover**\-Verbindungseigenschaft zurück.|  
|[getPacketSize](../content/getPacketSize-Method--SQLServerDataSource-.md)|Gibt die aktuelle Netzwerkpaketgröße \(in Bytes\) für die Kommunikation mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] zurück.|  
|[getPortNumber](../content/getPortNumber-Method--SQLServerDataSource-.md)|Gibt die aktuelle Portnummer für die Kommunikation mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] zurück.|  
|[getReference](../content/getReference-Method--SQLServerDataSource-.md)|Gibt einen Verweis auf dieses [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Objekt zurück.|  
|[getResponseBuffering](../content/getResponseBuffering-Method--SQLServerDataSource-.md)|Gibt den Antwortpuffermodus für dieses [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Objekt zurück.|  
|[getSelectMethod](../content/getSelectMethod-Method--SQLServerDataSource-.md)|Gibt den Standardcursortyp zurück, der für alle Resultsets verwendet wird, die mithilfe dieses [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Objekts erstellt werden.|  
|[getSendStringParametersAsUnicode](../content/getSendStringParametersAsUnicode-Method--SQLServerDataSource-.md)|Gibt einen Wert vom Typ **Boolean** zurück, mit dem angegeben wird, ob das Senden von Zeichenfolgenparametern an den Server im Unicode\-Format aktiviert ist.|  
|[getSendTimeAsDatetime](../content/getSendTimeAsDatetime-Method--SQLServerDataSource-.md)|Sie gibt die Einstellung der **SendTimeAsDatetime**\-Verbindungseigenschaft zurück.|  
|[getServerName](../content/getServerName-Method--SQLServerDataSource-.md)|Gibt den Namen des Computers zurück, auf dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ausgeführt wird.|  
|[getTrustServerCertificate](../content/getTrustServerCertificate-Method--SQLServerDataSource-.md)|Gibt einen Wert vom Typ **Boolean** zurück, mit dem angegeben wird, ob die trustServerCertificate\-Eigenschaft aktiviert ist.|  
|[getTrustStore](../content/getTrustStore-Method--SQLServerDataSource-.md)|Gibt den Pfad \(einschließlich Dateiname\) zur trustStore\-Zertifikatsdatei zurück.|  
|[getURL](../content/getURL-Method--SQLServerDataSource-.md)|Gibt die URL zurück, die zum Herstellen einer Verbindung mit der Datenquelle verwendet wird.|  
|[getUser](../content/getUser-Method--SQLServerDataSource-.md)|Gibt den Benutzernamen zurück, der zum Herstellen einer Verbindung mit der Datenquelle verwendet wird.|  
|[getUseSQLServerBaseDate](../content/getSendTimeAsDatetime-Method--SQLServerDataSource-.md)|Sie gibt die Einstellung der useSQLServerBaseDate\-Verbindungseigenschaft zurück.|  
|[getWorkstationID](../content/getWorkstationID-Method--SQLServerDataSource-.md)|Gibt den Namen des Clientcomputers zurück, der zum Herstellen einer Verbindung mit der Datenquelle verwendet wird.|  
|[getXopenStates](../content/getXopenStates-Method--SQLServerDataSource-.md)|Gibt einen Wert vom Typ **Boolean** zurück, mit dem angegeben wird, ob das Konvertieren von SQL\-Status in XOPEN\-kompatible Status aktiviert ist.|  
|[isWrapperFor](../content/isWrapperFor-Method--SQLServerDataSource-.md)|Gibt an, ob es sich bei diesem Datenquellenobjekt um einen Wrapper für die angegebene Schnittstelle handelt.|  
|[setApplicationIntent](../content/setApplicationIntent-Method--SQLServerDataSource-.md)|Legt den Wert der **applicationIntent**\-Verbindungseigenschaft fest.|  
|[setApplicationName](../content/setApplicationName-Method--SQLServerDataSource-.md)|Legt den Anwendungsnamen fest.|  
|[setAuthenticationScheme](../content/setAuthenticationScheme--SQLServerDataSource-.md)|Gibt die Art der integrierten Sicherheit an, die für die Anwendung verwendet werden soll.|  
|[setDatabaseName](../content/setDatabaseName-Method--SQLServerDataSource-.md)|Legt den Namen der Datenbank fest, mit der eine Verbindung hergestellt werden soll.|  
|[setDescription](../content/setDescription-Method--SQLServerDataSource-.md)|Legt die Beschreibung der Datenquelle fest.|  
|[setEncrypt](../content/setEncrypt-Method--SQLServerDataSource-.md)|Legt einen Wert vom Typ **Boolean** fest, mit dem angegeben wird, ob die encrypt\-Eigenschaft aktiviert ist.|  
|[setFailoverPartner](../content/setFailoverPartner-Method--SQLServerDataSource-.md)|Legt den Namen des Failoverservers fest, der in einer Datenbankspiegelungskonfiguration verwendet wird.|  
|[setHostNameInCertificate](../content/setHostNameInCertificate-Method--SQLServerDataSource-.md)|Legt den Hostnamen fest, der bei der Überprüfung des Secure Sockets Layer \(SSL\)\-Zertifikats von SQL Server verwendet werden soll.|  
|[setInstanceName](../content/setInstanceName-Method--SQLServerDataSource-.md)|Legt den Namen der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Instanz fest.|  
|[setIntegratedSecurity](../content/setIntegratedSecurity-Method--SQLServerDataSource-.md)|Legt einen Wert vom Typ **Boolean** fest, mit dem angegeben wird, ob die integratedSecurity\-Eigenschaft aktiviert ist.|  
|[setLastUpdateCount](../content/setLastUpdateCount-Method--SQLServerDataSource-.md)|Legt einen Wert vom Typ **Boolean** fest, mit dem angegeben wird, ob die lastUpdateCount\-Eigenschaft aktiviert ist.|  
|[setLockTimeout](../content/setLockTimeout-Method--SQLServerDataSource-.md)|Legt einen Wert vom Typ **int** fest, mit dem angegeben wird, wie lange von der Datenbank bis zum Melden eines Sperrtimeouts gewartet wird \(in Millisekunden\).|  
|[setLoginTimeout](../content/setLoginTimeout-Method--SQLServerDataSource-.md)|Legt die Anzahl von Sekunden fest, die vom [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Objekt bei der Verbindungsherstellung gewartet wird.|  
|[setLogWriter](../content/setLogWriter-Method--SQLServerDataSource-.md)|Legt einen Zeichenausgabedatenstrom für alle Protokollierungs\- und Ablaufverfolgungsmeldungen fest.|  
|[setMultiSubnetFailover](../content/setMultiSubnetFailover-Method--SQLServerDataSource-.md)|Legt den Wert der **multiSubnetFailover**\-Verbindungseigenschaft fest.|  
|[setPacketSize](../content/setPacketSize-Method--SQLServerDataSource-.md)|Legt die aktuelle Netzwerkpaketgröße \(in Bytes\) für die Kommunikation mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] fest.|  
|[setPassword](../content/setPassword-Method--SQLServerDataSource-.md)|Legt das Kennwort fest, das für die Verbindung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verwendet wird.|  
|[setPortNumber](../content/setPortNumber-Method--SQLServerDataSource-.md)|Legt die Portnummer für die Kommunikation mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] fest.|  
|[setResponseBuffering](../content/setResponseBuffering-Method--SQLServerDataSource-.md)|Legt den Antwortpuffermodus für Verbindungen fest, die unter Verwendung dieses [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Objekts erstellt werden.|  
|[setSelectMethod](../content/setSelectMethod-Method--SQLServerDataSource-.md)|Legt den Standardcursortyp fest, der für alle Resultsets verwendet wird, die mithilfe dieses [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Objekts erstellt werden.|  
|[setSendStringParametersAsUnicode](../content/setSendStringParametersAsUnicode-Method--SQLServerDataSource-.md)|Legt einen Wert vom Typ **Boolean** fest, mit dem angegeben wird, ob das Senden von Zeichenfolgenparametern an den Server im Unicode\-Format aktiviert ist.|  
|[setSendTimeAsDatetime](../content/setSendTimeAsDatetime-Method--SQLServerDataSource-.md)|Gibt die Art und Weise an, wie java.sql.Time\-Werte an den Server gesendet werden.|  
|[setServerName](../content/setServerName-Method--SQLServerDataSource-.md)|Legt den Namen des Computers fest, auf dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ausgeführt wird.|  
|[setTrustServerCertificate](../content/setTrustServerCertificate-Method--SQLServerDataSource-.md)|Legt einen Wert vom Typ **Boolean** fest, mit dem angegeben wird, ob die trustServerCertificate\-Eigenschaft aktiviert ist.|  
|[setTrustStore](../content/setTrustStore-Method--SQLServerDataSource-.md)|Legt den Pfad \(einschließlich Dateiname\) zur trustStore\-Zertifikatsdatei fest.|  
|[setTrustStorePassword](../content/setTrustStorePassword-Method--SQLServerDataSource-.md)|Legt das Kennwort fest, das zum Überprüfen der Integrität der trustStore\-Daten verwendet wird.|  
|[setURL](../content/setURL-Method--SQLServerDataSource-.md)|Legt die URL fest, die zum Herstellen einer Verbindung mit der Datenquelle verwendet wird.|  
|[setUser](../content/setUser-Method--SQLServerDataSource-.md)|Legt den Benutzernamen fest, der zum Herstellen einer Verbindung mit der Datenquelle verwendet wird.|  
|[setWorkstationID](../content/setWorkstationID-Method--SQLServerDataSource-.md)|Legt den Namen des Clientcomputers fest, der zum Herstellen einer Verbindung mit der Datenquelle verwendet wird.|  
|[setXopenStates](../content/setXopenStates-Method--SQLServerDataSource-.md)|Legt einen Wert vom Typ **Boolean** fest, mit dem angegeben wird, ob das Konvertieren von SQL\-Status in XOPEN\-kompatible Status aktiviert ist.|  
|[unwrap](../content/unwrap-Method--SQLServerDataSource-.md)|Gibt ein Objekt zurück, das die angegebene Schnittstelle implementiert, um den Zugriff auf die [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-spezifischen Methoden zu ermöglichen.|  
  
## Geerbte Methoden  
  
|Klasse geerbt von:|Methoden|  
|------------------------|--------------|  
|java.lang.Object|clone, equals, finalize, getClass, hashCode, notify, notifyAll, toString, wait|  
|java.sql.Wrapper|isWrapperFor, unwrap|  
  
## Siehe auch  
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  