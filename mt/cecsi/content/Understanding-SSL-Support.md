---
title: "Grundlegendes zur SSL-Unterst&#252;tzung"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 073f3b9e-8edd-4815-88ea-de0655d0325e
caps.latest.revision: 28
caps.handback.revision: 27
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
# Grundlegendes zur SSL-Unterst&#252;tzung
  Wenn die Anwendung beim Herstellen einer Verbindung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Verschlüsselung anfordert und die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Instanz für die Unterstützung von SSL\-Verschlüsselung konfiguriert ist, initialisiert [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] den SSL\-Handshake. Mithilfe des Handshakes können der Server und der Client die Verschlüsselungs\- und Kryptografiealgorithmen aushandeln, mit denen Daten geschützt werden sollen. Nachdem der SSL\-Handshake abgeschlossen wurde, können der Client und der Server die verschlüsselten Daten sicher senden. Während des SSL\-Handshakes sendet der Server sein Zertifikat für öffentliche Schlüssel an den Client. Der Aussteller eines Zertifikats für öffentliche Schlüssel wird als Zertifizierungsstelle bezeichnet. Der Client ist dafür verantwortlich zu überprüfen, ob der Client der Zertifizierungsstelle vertraut.  
  
 Wenn die Anwendung keine Verschlüsselung anfordert, wird von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] keine Unterstützung der SSL\-Verschlüsselung von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] erzwungen. Wenn die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Instanz nicht für das Erzwingen der SSL\-Verschlüsselung konfiguriert ist, wird eine Verbindung ohne jegliche Verschlüsselung hergestellt. Falls die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Instanz für das Erzwingen der SSL\-Verschlüsselung konfiguriert ist, aktiviert der Treiber automatisch die SSL\-Verschlüsselung, wenn er auf einer ordnungsgemäß konfigurierten Java Virtual Machine \(JVM\) ausgeführt wird. Andernfalls wird die Verbindung getrennt, und der Treiber löst einen Fehler aus.  
  
> [!NOTE]  
>  Stellen Sie sicher, dass der an **serverName** übergebene Name für eine erfolgreiche SSL\-Verbindung exakt dem CN \(Common Name, allgemeiner Name\) oder dem DNS\-Namen im SAN \(Subject Alternate Name, Subjektalternativname\) im Serverzertifikat entspricht.  
  
> [!NOTE]  
>  Weitere Informationen zum Konfigurieren von SSL für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] finden Sie im Thema zum Verschlüsseln von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Verbindungen in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation.  
  
## Hinweise  
 Damit die SSL\-Verschlüsselung von Anwendungen verwendet werden kann, wurden mit der Version 1.2 von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] die folgenden Verbindungseigenschaften eingeführt: **encrypt**, **trustServerCertificate**, **trustStore**, **trustStorePassword** und **hostNameInCertificate**. Weitere Informationen finden Sie unter [Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md).  
  
 In der folgenden Tabelle wird das Verhalten der [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-Version in möglichen SSL\-Verbindungsszenarios zusammengefasst. In jedem Szenario wird ein anderer Satz von SSL\-Verbindungseigenschaften verwendet. Die Tabelle schließt Folgendes ein:  
  
-   **blank**: "Die Eigenschaft ist in der Verbindungszeichenfolge nicht enthalten."  
  
-   **value**: "Die Eigenschaft ist in der Verbindungszeichenfolge vorhanden, und ihr Wert ist gültig."  
  
-   **any**: "Es ist nicht ausschlaggebend, ob die Eigenschaft in der Verbindungszeichenfolge vorhanden oder ihr Wert gültig ist."  
  
> [!NOTE]  
>  Das gleiche Verhalten trifft auf die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Benutzerauthentifizierung und die integrierte Windows\-Authentifizierung zu.  
  
|encrypt|trustServerCertificate|hostNameInCertificate|trustStore|trustStorePassword|Verhalten|  
|-------------|----------------------------|---------------------------|----------------|------------------------|---------------|  
|false oder blank|any|any|any|any|[!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] erzwingt keine Unterstützung der SSL\-Verschlüsselung durch [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]. Wenn der Server ein selbst signiertes Zertifikat aufweist, initiiert der Treiber den SSL\-Zertifikataustausch. Das SSL\-Zertifikat wird nicht überprüft, und nur die Anmeldeinformationen \(im Anmeldepaket\) werden verschlüsselt.<br /><br /> Wenn der Server erfordert, dass der Client SSL\-Verschlüsselung unterstützt, initiiert der Treiber den SSL\-Zertifikataustausch. Das SSL\-Zertifikat wird nicht überprüft, die gesamte Kommunikation wird jedoch verschlüsselt.|  
|true|true|any|any|any|[!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] fordert die Verwendung der SSL\-Verschlüsselung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] an.<br /><br /> Wenn der Server erfordert, dass der Client SSL\-Verschlüsselung unterstützt oder der Server die Verschlüsselung unterstützt, initiiert der Treiber den SSL\-Zertifikataustausch. Wenn die **trustServerCertificate**\-Eigenschaft auf "true" festgelegt ist, überprüft der Treiber das SSL\-Zertifikat nicht.<br /><br /> Wenn der Server nicht für die Unterstützung der Verschlüsselung konfiguriert ist, löst der Treiber einen Fehler aus und trennt die Verbindung.|  
|true|false oder blank|blank|blank|blank|[!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] fordert die Verwendung der SSL\-Verschlüsselung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] an.<br /><br /> Wenn der Server erfordert, dass der Client SSL\-Verschlüsselung unterstützt oder der Server die Verschlüsselung unterstützt, initiiert der Treiber den SSL\-Zertifikataustausch.<br /><br /> Der Treiber verwendet die in der Verbindungs\-URL angegebene **serverName**\-Eigenschaft, um das SSL\-Zertifikat des Servers zu überprüfen. Außerdem werden die Suchregeln der Trust\-Manager\-Factory verwendet, um den zu verwendenden Zertifikatspeicher zu ermitteln.<br /><br /> Wenn der Server nicht für die Unterstützung der Verschlüsselung konfiguriert ist, löst der Treiber einen Fehler aus und trennt die Verbindung.|  
|true|false oder blank|value|blank|blank|[!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] fordert die Verwendung der SSL\-Verschlüsselung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] an.<br /><br /> Wenn der Server erfordert, dass der Client SSL\-Verschlüsselung unterstützt oder der Server die Verschlüsselung unterstützt, initiiert der Treiber den SSL\-Zertifikataustausch.<br /><br /> Der Treiber überprüft den Subject\-Wert des SSL\-Zertifikats mithilfe des für die **hostNameInCertificate**\-Eigenschaft angegebenen Werts.<br /><br /> Wenn der Server nicht für die Unterstützung der Verschlüsselung konfiguriert ist, löst der Treiber einen Fehler aus und trennt die Verbindung.|  
|true|false oder blank|blank|value|value|[!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] fordert die Verwendung der SSL\-Verschlüsselung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] an.<br /><br /> Wenn der Server erfordert, dass der Client SSL\-Verschlüsselung unterstützt oder der Server die Verschlüsselung unterstützt, initiiert der Treiber den SSL\-Zertifikataustausch.<br /><br /> Der Treiber verwendet den **trustStore**\-Eigenschaftswert zum Ermitteln der Zertifikatdatei **trustStore** und den **trustStorePassword**\-Eigenschaftswert zum Überprüfen der Integrität der Datei **trustStore**.<br /><br /> Wenn der Server nicht für die Unterstützung der Verschlüsselung konfiguriert ist, löst der Treiber einen Fehler aus und trennt die Verbindung.|  
|true|false oder blank|blank|blank|value|[!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] fordert die Verwendung der SSL\-Verschlüsselung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] an.<br /><br /> Wenn der Server erfordert, dass der Client SSL\-Verschlüsselung unterstützt oder der Server die Verschlüsselung unterstützt, initiiert der Treiber den SSL\-Zertifikataustausch.<br /><br /> Der Treiber verwendet den **trustStorePassword**\-Eigenschaftswert zum Überprüfen der Integrität der Standarddatei **trustStore**.<br /><br /> Wenn der Server nicht für die Unterstützung der Verschlüsselung konfiguriert ist, löst der Treiber einen Fehler aus und trennt die Verbindung.|  
|true|false oder blank|blank|value|blank|[!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] fordert die Verwendung der SSL\-Verschlüsselung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] an.<br /><br /> Wenn der Server erfordert, dass der Client SSL\-Verschlüsselung unterstützt oder der Server die Verschlüsselung unterstützt, initiiert der Treiber den SSL\-Zertifikataustausch.<br /><br /> Der Treiber verwendet den **trustStore**\-Eigenschaftswert, um den Speicherort der Datei **trustStore** zu ermitteln.<br /><br /> Wenn der Server nicht für die Unterstützung der Verschlüsselung konfiguriert ist, löst der Treiber einen Fehler aus und trennt die Verbindung.|  
|true|false oder blank|value|blank|value|[!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] fordert die Verwendung der SSL\-Verschlüsselung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] an.<br /><br /> Wenn der Server erfordert, dass der Client SSL\-Verschlüsselung unterstützt oder der Server die Verschlüsselung unterstützt, initiiert der Treiber den SSL\-Zertifikataustausch.<br /><br /> Der Treiber verwendet den **trustStorePassword**\-Eigenschaftswert zum Überprüfen der Integrität der Standarddatei **trustStore**. Außerdem verwendet der Treiber den **hostNameInCertificate**\-Eigenschaftswert, um das SSL\-Zertifikat zu überprüfen.<br /><br /> Wenn der Server nicht für die Unterstützung der Verschlüsselung konfiguriert ist, löst der Treiber einen Fehler aus und trennt die Verbindung.|  
|true|false oder blank|value|value|blank|[!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] fordert die Verwendung der SSL\-Verschlüsselung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] an.<br /><br /> Wenn der Server erfordert, dass der Client SSL\-Verschlüsselung unterstützt oder der Server die Verschlüsselung unterstützt, initiiert der Treiber den SSL\-Zertifikataustausch.<br /><br /> Der Treiber verwendet den **trustStore**\-Eigenschaftswert, um den Speicherort der Datei **trustStore** zu ermitteln. Außerdem verwendet der Treiber den **hostNameInCertificate**\-Eigenschaftswert, um das SSL\-Zertifikat zu überprüfen.<br /><br /> Wenn der Server nicht für die Unterstützung der Verschlüsselung konfiguriert ist, löst der Treiber einen Fehler aus und trennt die Verbindung.|  
|true|false oder blank|value|value|value|[!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] fordert die Verwendung der SSL\-Verschlüsselung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] an.<br /><br /> Wenn der Server erfordert, dass der Client SSL\-Verschlüsselung unterstützt oder der Server die Verschlüsselung unterstützt, initiiert der Treiber den SSL\-Zertifikataustausch.<br /><br /> Der Treiber verwendet den **trustStore**\-Eigenschaftswert zum Ermitteln der Zertifikatdatei **trustStore** und den **trustStorePassword**\-Eigenschaftswert zum Überprüfen der Integrität der Datei **trustStore**. Außerdem verwendet der Treiber den **hostNameInCertificate**\-Eigenschaftswert, um das SSL\-Zertifikat zu überprüfen.<br /><br /> Wenn der Server nicht für die Unterstützung der Verschlüsselung konfiguriert ist, löst der Treiber einen Fehler aus und trennt die Verbindung.|  
  
 Wenn die encrypt\-Eigenschaft auf **true** festgelegt ist, verwendet [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] den JSSE\-Standardsicherheitsanbieter der JVM, um die SSL\-Verschlüsselung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] auszuhandeln. Der Standardsicherheitsanbieter unterstützt möglicherweise nicht alle erforderlichen Funktionen zum erfolgreichen Aushandeln der SSL\-Verschlüsselung. So ist es beispielsweise möglich, dass die im SSL\-Zertifikat für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verwendete Größe des öffentlichen RSA\-Schlüssels vom Standardsicherheitsanbieter nicht unterstützt wird. In diesem Fall löst der Standardsicherheitsanbieter möglicherweise einen Fehler aus, wodurch der JDBC\-Treiber die Verbindung trennt. Führen Sie zum Beheben dieses Problems eine der folgenden Aktionen aus:  
  
-   Konfigurieren Sie [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] mit einem Serverzertifikat mit einem kleineren öffentlichen RSA\-Schlüssel.  
  
-   Konfigurieren Sie die JVM in der Sicherheitseigenschaftendatei "\<java\-home\>\/lib\/security\/java.security" für die Verwendung eines anderen JSSE\-Sicherheitsanbieters.  
  
-   Verwenden Sie eine andere JVM  
  
## Überprüfen des SSL\-Serverzertifikats  
 Während des SSL\-Handshakes sendet der Server sein Zertifikat für öffentliche Schlüssel an den Client. Der JDBC\-Treiber oder Client muss überprüfen, ob das Serverzertifikat von einer Zertifizierungsstelle herausgegeben wurde, der der Client vertraut. Der Treiber erfordert, dass das Serverzertifikat die folgenden Bedingungen erfüllt:  
  
-   Das Zertifikat wurde von einer vertrauenswürdigen Zertifizierungsstelle ausgegeben.  
  
-   Das Zertifikat muss für die Serverauthentifizierung vorgesehen sein.  
  
-   Das Zertifikat ist nicht abgelaufen.  
  
-   Der CN \(Common Name\) im Subjekt oder einem DNS\-Namen im SAN \(Subject Alternate Name, Subjektalternativname\) des Zertifikats entspricht genau dem **serverName**\-Wert, der in der Verbindungszeichenfolge angegeben ist, oder – falls angegeben – dem **hostNameInCertificate**\-Eigenschaftenwert.  
  
-   Ein DNS\-Name kann Platzhalterzeichen enthalten. [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] unterstützt jedoch keine Suchvorgänge mit Platzhalterzeichen. Das heißt, "abc.com" entspricht nicht "\*.com", während "\*.com" jedoch "\*.com" entspricht.  
  
## Siehe auch  
 [Verwenden der SSL-Verschlüsselung](../content/Using-SSL-Encryption.md)   
 [Sichern von JDBC-Treiberanwendungen](../content/Securing-JDBC-Driver-Applications.md)  
  
  