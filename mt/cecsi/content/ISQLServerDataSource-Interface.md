---
title: "ISQLServerDataSource-Schnittstelle"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ba1d3242-19ca-4321-83fe-867a4f69f1d4
caps.latest.revision: 15
caps.handback.revision: 14
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
# ISQLServerDataSource-Schnittstelle
  Eine Factory zur Erstellung von Verbindungen zur von diesem Objekt dargestellten Datenquelle. Die Schnittstelle wurde in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 hinzugefügt.  
  
 **Paket:** com.microsoft.sqlserver.jdbc  
  
 **Erweitert:** java.sql.CommonDataSource  
  
## Syntax  
  
```  
  
public interface ISQLServerDataSource  
```  
  
## Hinweise  
 Diese Schnittstelle wird durch [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md) implementiert.  
  
 Diese Schnittstelle legt die folgenden [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-spezifischen Methoden dar:  
  
|Methode|Weitere Informationen finden Sie unter|  
|-------------|--------------------------------------------|  
|öffentliche Zeichenkette getApplicationName\(\)|[getApplicationName](../content/getApplicationName-Method--SQLServerDataSource-.md)|  
|öffentliche Zeichenkette getDatabaseName\(\)|[getDatabaseName](../content/getDatabaseName-Method--SQLServerDataSource-.md)|  
|öffentliche Zeichenkette getDescription\(\)|[getDescription](../content/getDescription-Method--SQLServerDataSource-.md)|  
|öffentlicher boolescher Wert getEncrypt\(\)|[getEncrypt](../content/getEncrypt-Method--SQLServerDataSource-.md)|  
|öffentliche Zeichenkette getFailoverPartner\(\)|[getFailoverPartner](../content/getFailoverPartner-Method--SQLServerDataSource-.md)|  
|öffentliche Zeichenkette getHostNameInCertificate\(\)|[getHostNameInCertificate](../content/getHostNameInCertificate-Method--SQLServerDataSource-.md)|  
|öffentliche Zeichenkette getInstanceName\(\)|[getInstanceName](../content/getInstanceName-Method--SQLServerDataSource-.md)|  
|öffentlicher boolescher Wert getLastUpdateCount\(\)|[getLastUpdateCount](../content/getLastUpdateCount-Method--SQLServerDataSource-.md)|  
|öffentliches int getLockTimeout\(\)|[getLockTimeout](../content/getLockTimeout-Method--SQLServerDataSource-.md)|  
|öffentlicher boolescher Wert getMultiSubnetFailover\(\)|[getMultiSubnetFailover](../content/getMultiSubnetFailover-Method--SQLServerDataSource-.md)|  
|öffentliches int getPacketSize\(\)|[getPacketSize](../content/getPacketSize-Method--SQLServerDataSource-.md)|  
|öffentliches int getPortNumber\(\)|[getPortNumber](../content/getPortNumber-Method--SQLServerDataSource-.md)|  
|öffentliche Zeichenfolge getResponseBuffering\(\)|[getResponseBuffering](../content/getResponseBuffering-Method--SQLServerDataSource-.md)|  
|öffentliche Zeichenkette getSelectMethod\(\)|[getSelectMethod](../content/getSelectMethod-Method--SQLServerDataSource-.md)|  
|öffentlicher boolescher Wert getSendStringParametersAsUnicode\(\)|[getSendStringParametersAsUnicode](../content/getSendStringParametersAsUnicode-Method--SQLServerDataSource-.md)|  
|öffentlicher boolescher Wert getSendTimeAsDatetime\(\)|[getSendTimeAsDatetime](../content/getSendTimeAsDatetime-Method--SQLServerDataSource-.md)|  
|öffentliche Zeichenkette getServerName\(\)|[getServerName](../content/getServerName-Method--SQLServerDataSource-.md)|  
|öffentlicher boolescher Wert getTrustServerCertificate\(\)|[getTrustServerCertificate](../content/getTrustServerCertificate-Method--SQLServerDataSource-.md)|  
|öffentliche Zeichenkette getTrustStore\(\)|[getTrustStore](../content/getTrustStore-Method--SQLServerDataSource-.md)|  
|öffentliche Zeichenkette getURL\(\)|[getURL](../content/getURL-Method--SQLServerDataSource-.md)|  
|öffentliche Zeichenkette getUser\(\)|[getUser](../content/getUser-Method--SQLServerDataSource-.md)|  
|öffentliche Zeichenkette getWorkstationID\(\)|[getWorkstationID](../content/getWorkstationID-Method--SQLServerDataSource-.md)|  
|öffentlicher boolescher Wert getXopenStates\(\)|[getXopenStates](../content/getXopenStates-Method--SQLServerDataSource-.md)|  
|öffentliches void setApplicationName\(String\)|[setApplicationName](../content/setApplicationName-Method--SQLServerDataSource-.md)|  
|öffentliches void setAuthenticationSceme\(String\)|[setAuthenticationSceme](../content/setAuthenticationScheme--SQLServerDataSource-.md)|  
|öffentliches void setDatabaseName\(String\)|[setDatabaseName](../content/setDatabaseName-Method--SQLServerDataSource-.md)|  
|öffentliches void setDescription\(String\)|[setDescription](../content/setDescription-Method--SQLServerDataSource-.md)|  
|öffentliches void setEncrypt\(boolean\)|[setEncrypt](../content/setEncrypt-Method--SQLServerDataSource-.md)|  
|öffentliches void setFailoverPartner\(String\)|[setFailoverPartner](../content/setFailoverPartner-Method--SQLServerDataSource-.md)|  
|öffentliches void setHostNameInCertificate\(String\)|[setHostNameInCertificate](../content/setHostNameInCertificate-Method--SQLServerDataSource-.md)|  
|öffentliches void setInstanceName\(String\)|[setInstanceName](../content/setInstanceName-Method--SQLServerDataSource-.md)|  
|öffentliches void setIntegratedSecurity\(boolean\)|[setIntegratedSecurity](../content/setIntegratedSecurity-Method--SQLServerDataSource-.md)|  
|öffentliches void setLastUpdateCount\(boolean\)|[setLastUpdateCount](../content/setLastUpdateCount-Method--SQLServerDataSource-.md)|  
|öffentliches void setLockTimeout\(int\)|[setLockTimeout](../content/setLockTimeout-Method--SQLServerDataSource-.md)|  
|öffentliches setMultiSubnetFailover\(boolesches multiSubnetFailover\)|[setMultiSubnetFailover](../content/setMultiSubnetFailover-Method--SQLServerDataSource-.md)|  
|öffentliches void setPacketSize\(int\)|[setPacketSize](../content/setPacketSize-Method--SQLServerDataSource-.md)|  
|öffentliches void setPassword\(String\)|[setPassword](../content/setPassword-Method--SQLServerDataSource-.md)|  
|öffentliches void setPortNumber\(int\)|[setPortNumber](../content/setPortNumber-Method--SQLServerDataSource-.md)|  
|öffentliches void setResponseBuffering\(String\)|[setResponseBuffering](../content/setResponseBuffering-Method--SQLServerDataSource-.md)|  
|öffentliches void setSelectMethod\(String\)|[setSelectMethod](../content/setSelectMethod-Method--SQLServerDataSource-.md)|  
|öffentliches void setSendStringParametersAsUnicode\(boolean\)|[setSendStringParametersAsUnicode](../content/setSendStringParametersAsUnicode-Method--SQLServerDataSource-.md)|  
|öffentliches void setSendTimeAsDatetime\(boolean\)|[setSendTimeAsDatetime](../content/setSendTimeAsDatetime-Method--SQLServerDataSource-.md)|  
|öffentliches void setServerName\(String\)|[setServerName](../content/setServerName-Method--SQLServerDataSource-.md)|  
|öffentliches void setTrustServerCertificate\(boolean\)|[setTrustServerCertificate](../content/setTrustServerCertificate-Method--SQLServerDataSource-.md)|  
|öffentliches void setTrustStore\(String\)|[setTrustStore](../content/setTrustStore-Method--SQLServerDataSource-.md)|  
|öffentliches void setTrustStorePassword\(String\)|[setTrustStorePassword](../content/setTrustStorePassword-Method--SQLServerDataSource-.md)|  
|öffentliches void setURL\(String url\)|[setURL](../content/setURL-Method--SQLServerDataSource-.md)|  
|öffentliches void setUser\(String\)|[setUser](../content/setUser-Method--SQLServerDataSource-.md)|  
|öffentliches void setWorkstationID\(String\)|[setWorkstationID](../content/setWorkstationID-Method--SQLServerDataSource-.md)|  
|öffentliches void setXopenStates\(boolean\)|[setXopenStates](../content/setXopenStates-Method--SQLServerDataSource-.md)|  
  
## Siehe auch  
 [API-Referenz für den JDBC-Treiber](../content/JDBC-Driver-API-Reference.md)  
  
  