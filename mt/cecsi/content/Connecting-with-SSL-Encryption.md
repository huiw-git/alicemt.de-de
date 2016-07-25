---
title: "Herstellen von Verbindungen mit SSL-Verschl&#252;sselung"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ec91fa8a-ab7e-4c1e-a05a-d7951ddf33b1
caps.latest.revision: 18
caps.handback.revision: 17
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
# Herstellen von Verbindungen mit SSL-Verschl&#252;sselung
  In diesem Beispiel wird veranschaulicht, wie Verbindungszeichenfolgeneigenschaften verwendet werden, mit denen Anwendungen Secure Sockets Layer \(SSL\)\-Verschlüsselung in einer Java\-Anwendung verwenden können. Weitere Informationen zu den neuen Eigenschaften für Verbindungszeichenfolgen \(beispielsweise **encrypt**, **trustServerCertificate**, **trustStore**, **trustStorePassword** und **hostNameInCertificate**\) finden Sie unter [Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md).  
  
 Wenn die **encrypt**\-Eigenschaft auf **true** festgelegt ist und die **trustServerCertificate**\-Eigenschaft auf **true** festgelegt ist, wird von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] keine Überprüfung des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-SSL\-Zertifikats ausgeführt. Dies ist normalerweise zum Zulassen von Verbindungen in Testumgebungen erforderlich, beispielsweise wenn die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Instanz nur über ein selbst signiertes Zertifikat verfügt.  
  
 Im folgenden Codebeispiel wird das Festlegen der **trustServerCertificate**\-Eigenschaft in einer Verbindungszeichenfolge veranschaulicht:  
  
```  
String connectionUrl =   
    "jdbc:sqlserver://localhost:1433;" +  
     "databaseName=AdventureWorks;integratedSecurity=true;" +  
     "encrypt=true;trustServerCertificate=true";  
```  
  
 Wenn die **encrypt**\-Eigenschaft auf **true** festgelegt ist und die **trustServerCertificate**\-Eigenschaft auf **false** festgelegt ist, wird von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] die Überprüfung des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-SSL\-Zertifikats ausgeführt. Das Überprüfen des Serverzertifikats ist Teil des SSL\-Handshakes und stellt sicher, dass es sich bei dem Server tatsächlich um den Server handelt, mit dem eine Verbindung hergestellt werden soll. Zum Überprüfen des Serverzertifikats müssen die Vertrauensinformationen zur Verbindungszeit explizit mithilfe der **trustStore**\-Verbindungseigenschaft und der **trustStorePassword**\-Verbindungseigenschaft oder implizit mithilfe des Standardvertrauensspeichers der zugrunde liegenden Java Virtual Machine \(JVM\) übermittelt werden.  
  
 Die **trustStore**\-Eigenschaft gibt den Pfad \(einschließlich des Dateinamens\) der **trustStore**\-Zertifikatsdatei an. Diese enthält die Liste der Zertifikate, denen der Client vertraut. Die **trustStorePassword**\-Eigenschaft gibt das Kennwort an, das verwendet wird, um die Integrität der trustStore\-Daten zu überprüfen. Weitere Informationen zum Standardvertrauensspeicher der JVM finden Sie unter [Konfigurieren des Clients für SSL-Verschlüsselung](../content/Configuring-the-Client-for-SSL-Encryption.md).  
  
 Im folgenden Codebeispiel wird das Festlegen der **trustStore**\-Eigenschaft und der **trustStorePassword**\-Eigenschaft in einer Verbindungszeichenfolge veranschaulicht:  
  
```  
String connectionUrl =   
    "jdbc:sqlserver://localhost:1433;" +  
     "databaseName=AdventureWorks;integratedSecurity=true;" +  
     "encrypt=true; trustServerCertificate=false;" +  
     "trustStore=storeName;trustStorePassword=storePassword";  
```  
  
 JDBC Driver stellt die zusätzliche Eigenschaft **hostNameInCertificate** bereit, mit der der Hostname des Servers angegeben wird. Der Wert dieser Eigenschaft muss mit der **subject**\-Eigenschaft des Zertifikats übereinstimmen.  
  
 Im folgenden Codebeispiel wird das Verwenden der **hostNameInCertificate**\-Eigenschaft in einer Verbindungszeichenfolge veranschaulicht:  
  
```  
String connectionUrl =   
    "jdbc:sqlserver://localhost:1433;" +  
     "databaseName=AdventureWorks;integratedSecurity=true;" +  
     "encrypt=true; trustServerCertificate=false;" +  
     "trustStore=storeName;trustStorePassword=storePassword" +  
     "hostNameInCertificate=hostName";  
```  
  
> [!NOTE]  
>  Sie können den Wert von Verbindungseigenschaften auch mithilfe der entsprechenden **setter**\-Methoden festlegen, die von der [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Klasse bereitgestellt werden.  
  
 Wenn die **encrypt**\-Eigenschaft auf **true** und die **trustServerCertificate**\-Eigenschaft auf **false** festgelegt ist und der Servername in der Verbindungszeichenfolge nicht dem Servernamen im [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-SSL\-Zertifikat entspricht, wird der folgende Fehler ausgegeben: Der Treiber konnte keine sichere Verbindung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] über die SSL \(Secure Sockets Layer\)\-Verschlüsselung herstellen. Fehler: "java.security.cert.CertificateException: Fehler bei der Servernamenüberprüfung in einem Zertifikat während der SSL \(Secure Sockets Layer\)\-Initialisierung."  
  
## Siehe auch  
 [Verwenden der SSL-Verschlüsselung](../content/Using-SSL-Encryption.md)   
 [Sichern von JDBC-Treiberanwendungen](../content/Securing-JDBC-Driver-Applications.md)  
  
  