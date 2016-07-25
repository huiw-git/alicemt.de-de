---
title: "Konfigurieren des Clients f&#252;r SSL-Verschl&#252;sselung"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ae34cd1f-3569-4759-80c7-7c9b33b3e9eb
caps.latest.revision: 17
caps.handback.revision: 16
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
# Konfigurieren des Clients f&#252;r SSL-Verschl&#252;sselung
  Der [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] oder Client muss überprüfen, ob es sich bei dem Server um den richtigen Server handelt und das Serverzertifikat von einer Zertifizierungsstelle herausgegeben wurde, der der Client vertraut. Zum Überprüfen des Serverzertifikats müssen die Informationen zur Vertrauenswürdigkeit zur Verbindungszeit angegeben werden. Außerdem muss der Aussteller des Serverzertifikats eine Zertifizierungsstelle sein, der der Client vertraut.  
  
 In diesem Thema wird zuerst beschrieben, wie die Vertrauenswürdigkeitsinformationen auf dem Clientcomputer angegeben werden. Anschließend wird das Importieren eines Serverzertifikats in den Vertrauensspeicher des Clientcomputers erläutert, wenn die Instanz des Secure Sockets Layer \(SSL\)\-Zertifikats von SQL Server von einer privaten Zertifizierungsstelle veröffentlicht wird.  
  
 Weitere Informationen zum Überprüfen des Serverzertifikats finden Sie im Abschnitt zum Überprüfen des SSL\-Serverzertifikats unter [Grundlegendes zur SSL-Unterstützung](../content/Understanding-SSL-Support.md).  
  
## Konfigurieren des Clientvertrauensspeichers  
 Damit das Serverzertifikat überprüft werden kann, müssen die Vertrauensinformationen zur Verbindungszeit explizit mithilfe der **trustStore**\-Verbindungseigenschaft und der **trustStorePassword**\-Verbindungseigenschaft oder implizit mithilfe des Standardvertrauensspeichers der zugrunde liegenden Java Virtual Machine \(JVM\) übermittelt werden. Weitere Informationen zum Festlegen der **trustStore**\-Eigenschaft und der **trustStorePassword**\-Eigenschaft in einer Verbindungszeichenfolge finden Sie unter [Herstellen von Verbindungen mit SSL-Verschlüsselung](../content/Connecting-with-SSL-Encryption.md).  
  
 Wenn die **trustStore**\-Eigenschaft nicht angegeben oder auf NULL festgelegt ist, verwendet [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] den Sicherheitsanbieter der zugrunde liegenden JVM, d. h. Java Secure Socket Extension \(SunJSSE\). Der SunJSSE\-Anbieter stellt einen Standard\-TrustManager bereit. Hiermit werden die von SQL Server zurückgegebenen X.509\-Zertifikate anhand der in einem Vertrauensspeicher bereitgestellten Vertrauensinformationen überprüft.  
  
 Der TrustManager versucht, den Standard\-trustStore in der folgenden Suchreihenfolge zu suchen:  
  
-   Wenn die Systemeigenschaft "javax.net.ssl.trustStore" definiert ist, versucht TrustManager, die Datei **trustStore** anhand des von der Systemeigenschaft angegebenen Dateinamens zu suchen.  
  
-   Wenn die Systemeigenschaft "javax.net.ssl.trustStore" nicht angegeben wurde und die Datei "\<java\-home\>\/lib\/security\/jssecacerts" vorhanden ist, wird diese Datei verwendet.  
  
-   Wenn die Datei "\<java\-home\>\/lib\/security\/cacerts" vorhanden ist, wird diese Datei verwendet.  
  
 Weitere Informationen finden Sie in der Dokumentation zur SUNX509 TrustManager\-Schnittstelle auf der Sun Microsystems\-Website.  
  
 Durch die Java Runtime\-Umgebung können Sie die trustStore\-Systemeigenschaft und die trustStorePassword\-Systemeigenschaft wie folgt festlegen:  
  
```  
java -Djavax.net.ssl.trustStore=C:\MyCertificates\storeName  
java -Djavax.net.ssl.trustStorePassword=storePassword  
```  
  
 In diesem Fall verwenden alle Anwendungen, die auf dieser JVM ausgeführt werden, diese Einstellungen als Standard. Zum Überschreiben der Standardeinstellungen in Ihrer Anwendung sollten Sie die **trustStore**\-Verbindungseigenschaft und die **trustStorePassword**\-Verbindungseigenschaft in der Verbindungszeichenfolge oder in der entsprechenden Festlegungsmethode der [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Klasse festlegen.  
  
 Außerdem können Sie die Standardvertrauensspeicherdateien wie "\<java\-home\>\/lib\/security\/jssecacerts" und "\<java\-home\>\/lib\/security\/cacerts" konfigurieren und verwalten. Verwenden Sie hierzu das JAVA\-Hilfsprogramm "keytool", das mit der JRE \(Java Runtime Environment\) installiert wird. Weitere Informationen zum Hilfsprogramm "keytool" finden Sie in der Dokumentation zu keytool auf der Sun Microsystems\-Website.  
  
### Importieren des Serverzertifikats in den Vertrauensspeicher  
 Während des SSL\-Handshakes sendet der Server sein Zertifikat für öffentliche Schlüssel an den Client. Der Aussteller eines Zertifikats für öffentliche Schlüssel wird als Zertifizierungsstelle bezeichnet. Der Client muss sicherstellen, dass der Client der Zertifizierungsstelle vertraut. Dies wird erreicht, indem der öffentliche Schlüssel von vertrauenswürdigen Zertifizierungsstellen im Voraus bekannt ist. Normalerweise wird die JVM mit einem vordefinierten Satz vertrauenswürdiger Zertifizierungsstellen geliefert.  
  
 Wenn die Instanz des Secure Sockets Layer \(SSL\)\-Zertifikats von SQL Server von einer privaten Zertifizierungsstelle veröffentlicht wird, müssen Sie das Zertifikat der Zertifizierungsstelle der Liste der vertrauenswürdigen Zertifikate im Vertrauensspeicher des Clientcomputers hinzufügen.  
  
 Verwenden Sie hierzu das JAVA\-Hilfsprogramm "keytool", das mit der JRE \(Java Runtime Environment\) installiert wird. Mit der folgenden Eingabeaufforderung wird die Verwendung des Hilfsprogramms "keytool" zum Importieren eines Zertifikats aus einer Datei veranschaulicht:  
  
```  
keytool -import -v -trustcacerts -alias myServer -file caCert.cer -keystore truststore.ks  
```  
  
 Im Beispiel wird die Datei "caCert.cer" als Zertifikatsdatei verwendet. Sie müssen diese Zertifikatsdatei vom Server abrufen. In den folgenden Schritten wird erläutert, wie das Serverzertifikat in eine Datei exportiert wird:  
  
1.  Klicken Sie auf **Start**, klicken Sie auf **Ausführen**, und geben Sie **MMC** ein. \(MMC ist die Abkürzung für Microsoft Management Console.\)  
  
2.  Öffnen Sie in MMC die Zertifikate.  
  
3.  Erweitern Sie **Eigene Zertifikate** und dann **Zertifikate**.  
  
4.  Klicken Sie mit der rechten Maustaste auf das Serverzertifikat, und wählen Sie dann unter **Alle Aufgaben** die Option **Exportieren** aus.  
  
5.  Klicken Sie auf **Weiter**, um das Dialogfeld **Willkommen** des Zertifikatexport\-Assistenten zu überspringen.  
  
6.  Stellen Sie sicher, dass "Nein, privaten Schlüssel nicht exportieren" ausgewählt ist, und klicken Sie dann auf **Weiter**.  
  
7.  Stellen Sie sicher, dass **DER\-codiert\-binär X.509 \(.CER\)** oder **Base\-64\-codiert X.509 \(.CER\)** ausgewählt ist, und klicken Sie dann auf **Weiter**.  
  
8.  Geben Sie einen Namen für die Exportdatei ein.  
  
9. Klicken Sie auf **Weiter**, und klicken Sie dann auf **Fertig stellen**, um das Zertifikat zu exportieren.  
  
## Siehe auch  
 [Verwenden der SSL-Verschlüsselung](../content/Using-SSL-Encryption.md)   
 [Sichern von JDBC-Treiberanwendungen](../content/Securing-JDBC-Driver-Applications.md)  
  
  