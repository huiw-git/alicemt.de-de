---
title: "SQLServerConnectionPoolDataSource-Elemente"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dac0337e-8088-488c-a25a-801a2190f6ca
caps.latest.revision: 25
caps.handback.revision: 24
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
# SQLServerConnectionPoolDataSource-Elemente
  Die folgenden Tabellen enthalten die Elemente, die von der [SQLServerConnectionPoolDataSource](../content/SQLServerConnectionPoolDataSource-Class.md)\-Klasse verfügbar gemacht werden.  
  
## Konstruktoren  
  
|Name|Beschreibung|  
|----------|------------------|  
|[SQLServerConnectionPoolDataSource \(\)](../content/SQLServerConnectionPoolDataSource-Constructor---.md)|Initialisiert eine neue Instanz der [SQLServerConnectionPoolDataSource](../content/SQLServerConnectionPoolDataSource-Class.md)\-Klasse.|  
  
## Felder  
 Keine  
  
## Geerbte Felder  
 Keine  
  
## Methoden  
  
|Name|Beschreibung|  
|----------|------------------|  
|[getApplicationIntent](../content/getApplicationIntent-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Gibt den Wert der **applicationIntent**\-Verbindungseigenschaft zurück.|  
|[getApplicationName](../content/getApplicationName-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Gibt den Anwendungsnamen zurück.|  
|[getConnection](../content/getConnection-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Stellt eine Verbindung mit der Datenquelle her, für die dieses DataSource\-Objekt steht.|  
|[getDatabaseName](../content/getDatabaseName-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Gibt den Datenbanknamen zurück.|  
|[getDescription](../content/getDescription-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Gibt eine Beschreibung der Datenquelle zurück.|  
|[getFailoverPartner](../content/getFailoverPartner-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Gibt den Namen des Failoverservers zurück, der in einer Datenbankspiegelungskonfiguration verwendet wird.|  
|[getInstanceName](../content/getInstanceName-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Gibt den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Instanznamen zurück.|  
|[getLastUpdateCount](../content/getLastUpdateCount-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Gibt einen Wert vom Typ **boolean** zurück, mit dem angegeben wird, ob die lastUpdateCount\-Eigenschaft aktiviert ist.|  
|[getLockTimeout](../content/getLockTimeout-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Gibt einen Wert vom Typ **int** zurück, mit dem angegeben wird, wie lange von der Datenbank bis zum Melden eines Sperrtimeouts gewartet wird \(in Millisekunden\).|  
|[getLoginTimeout](../content/getLoginTimeout-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Gibt die Anzahl von Sekunden zurück, die vom DataSource\-Objekt bei der Verbindungsherstellung gewartet wird.|  
|[getLogWriter](../content/getLogWriter-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Gibt einen Zeichenausgabedatenstrom für alle Protokollierungs\- und Ablaufverfolgungsmeldungen zurück.|  
|[getMultiSubnetFailover](../content/getMultiSubnetFailover-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Gibt den Wert der **multiSubnetFailover**\-Verbindungseigenschaft zurück.|  
|[getPooledConnection](../content/getPooledConnection-Method--SQLServerConnectionPoolDataSource-.md)|Stellt eine physische Datenbankverbindung her, die als Poolverbindung verwendet werden kann.|  
|[getPortNumber](../content/getPortNumber-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Gibt die aktuelle Portnummer zurück, die für die Kommunikation mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verwendet wird.|  
|[getReference](../content/getReference-Method--SQLServerConnectionPoolDataSource-.md)|Gibt einen Verweis auf dieses DataSource\-Objekt zurück.|  
|[getSelectMethod](../content/getSelectMethod-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Gibt den Standardcursortyp zurück, der für alle Resultsets verwendet wird, die mithilfe dieses DataSource\-Objekts erstellt werden.|  
|[getSendStringParametersAsUnicode](../content/getSendStringParametersAsUnicode-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Gibt einen Wert vom Typ **Boolean** zurück, mit dem angegeben wird, ob das Senden von Zeichenfolgenparametern an den Server im Unicode\-Format aktiviert ist.|  
|[getServerName](../content/getServerName-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Gibt den Namen des Computers zurück, auf dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ausgeführt wird.|  
|[getURL](../content/getURL-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Gibt die URL zurück, die zum Herstellen einer Verbindung mit der Datenquelle verwendet wird.|  
|[getUser](../content/getUser-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Gibt den Benutzernamen zurück, der zum Herstellen einer Verbindung mit der Datenquelle verwendet wird.|  
|[getWorkstationID](../content/getWorkstationID-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Gibt den Namen des Clientcomputers zurück, der zum Herstellen einer Verbindung mit der Datenquelle verwendet wird.|  
|[getXopenStates](../content/getXopenStates-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Gibt einen Wert vom Typ **Boolean** zurück, mit dem angegeben wird, ob das Konvertieren von SQL\-Status in XOPEN\-kompatible Status aktiviert ist.|  
|[isWrapperFor](../content/isWrapperFor-Method--SQLServerConnectionPoolDataSource-.md)|Gibt an, ob es sich bei diesem Objekt um einen Wrapper für die angegebene Schnittstelle handelt.|  
|[setApplicationIntent](../content/setApplicationIntent-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Legt den Wert der **applicationIntent**\-Verbindungseigenschaft fest.|  
|[setApplicationName](../content/setApplicationName-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Legt den Anwendungsnamen fest.|  
|[setAuthenticationSceme](../content/setAuthenticationScheme--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Gibt die Art der integrierten Sicherheit an, die für die Anwendung verwendet werden soll.|  
|[setDatabaseName](../content/setDatabaseName-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Legt den Datenbanknamen fest, mit dem eine Verbindung hergestellt werden soll.|  
|[setDescription](../content/setDescription-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Legt die Beschreibung der Datenquelle fest.|  
|[setFailoverPartner](../content/setFailoverPartner-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Legt den Namen des Failoverservers fest, der in einer Datenbankspiegelungskonfiguration verwendet wird.|  
|[setInstanceName](../content/setInstanceName-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Legt den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Instanznamen fest.|  
|[setIntegratedSecurity](../content/setIntegratedSecurity-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Legt einen Wert vom Typ **Boolean** fest, mit dem angegeben wird, ob die integratedSecurity\-Eigenschaft aktiviert ist.|  
|[setLastUpdateCount](../content/setLastUpdateCount-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Legt einen Wert vom Typ **Boolean** fest, mit dem angegeben wird, ob die lastUpdateCount\-Eigenschaft aktiviert ist.|  
|[setLockTimeout](../content/setLockTimeout-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Legt einen Wert vom Typ **int** fest, mit dem angegeben wird, wie lange von der Datenbank bis zum Melden eines Sperrtimeouts gewartet werden soll \(in Millisekunden\).|  
|[setLoginTimeout](../content/setLoginTimeout-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Legt die Anzahl von Sekunden fest, die vom DataSource\-Objekt bei der Verbindungsherstellung gewartet wird.|  
|[setLogWriter](../content/setLogWriter-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Legt einen Zeichenausgabedatenstrom für alle Protokollierungs\- und Ablaufverfolgungsmeldungen fest.|  
|[setMultiSubnetFailover](../content/setMultiSubnetFailover-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Legt den Wert der **multiSubnetFailover**\-Verbindungseigenschaft fest.|  
|[setPassword](../content/setPassword-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Legt das Kennwort fest, das zum Herstellen einer Verbindung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verwendet wird.|  
|[setPortNumber](../content/setPortNumber-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Legt die Portnummer fest, die für die Kommunikation mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verwendet werden soll.|  
|[setSelectMethod](../content/setSelectMethod-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Legt den Standardcursortyp fest, der für alle Resultsets verwendet wird, die mithilfe dieses DataSource\-Objekts erstellt werden.|  
|[setSendStringParametersAsUnicode](../content/setSendStringParametersAsUnicode-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Legt einen Wert vom Typ **Boolean** fest, mit dem angegeben wird, ob das Senden von Zeichenfolgenparametern an den Server im Unicode\-Format aktiviert ist.|  
|[setServerName](../content/setServerName-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Legt den Namen des Computers fest, auf dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ausgeführt wird.|  
|[setURL](../content/setURL-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Legt die URL fest, die zum Herstellen einer Verbindung mit der Datenquelle verwendet wird.|  
|[setUser](../content/setUser-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Legt den Benutzernamen fest, der zum Herstellen einer Verbindung mit der Datenquelle verwendet wird.|  
|[setWorkstationID](../content/setWorkstationID-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Legt den Namen des Clientcomputers fest, der zum Herstellen einer Verbindung mit der Datenquelle verwendet wird.|  
|[setXopenStates](../content/setXopenStates-Method--SQLServerDataSource-.md)|\(Geerbt von [SQLServerDataSource](../content/SQLServerDataSource-Class.md).\) Legt einen Wert vom Typ **boolean** fest, mit dem angegeben wird, ob das Konvertieren von SQL\-Status in XOPEN\-kompatible Status aktiviert ist.|  
|[unwrap](../content/unwrap-Method--SQLServerConnectionPoolDataSource-.md)|Gibt ein Objekt zurück, das die angegebene Schnittstelle implementiert, um den Zugriff auf die [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-spezifischen Methoden zu ermöglichen.|  
  
## Geerbte Methoden  
  
|Klasse geerbt von:|Methoden|  
|------------------------|--------------|  
|com.microsoft.sqlserver.jdbc.SQLServerDataSource|getApplicationName, getConnection, getDatabaseName, getDescription, getFailoverPartner, getInstanceName, getLastUpdateCount, getLockTimeout, getLoginTimeout, getLogWriter, getPortNumber, getSelectMethod, getSendStringParametersAsUnicode, getServerName, getURL, getUser, getWorkstationID, getXopenStates, setApplicationName, setDatabaseName, setDescription, setFailoverPartner, setInstanceName, setIntegratedSecurity, setLastUpdateCount, setLockTimeout, setLoginTimeout, setLogWriter, setPassword, setPortNumber, setSelectMethod, setSendStringParametersAsUnicode, setServerName, setURL, setUser, setWorkstationID, setXopenStates|  
|java.lang.Object|clone, equals, finalize, getClass, hashCode, notify, notifyAll, toString, wait|  
|java.sql.Wrapper|isWrapperFor, unwrap|  
|javax.sql.ConnectionPoolDataSource|getLoginTimeout, getLogWriter, setLoginTimeout, setLogWriter, getPooledConnection|  
  
## Siehe auch  
 [SQLServerConnectionPoolDataSource-Klasse](../content/SQLServerConnectionPoolDataSource-Class.md)  
  
  