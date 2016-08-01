---
title: "Verwenden der SSL-Verschl&#252;sselung"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8e566243-2f93-4b21-8065-3c8336649309
caps.latest.revision: 32
caps.handback.revision: 31
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
# Verwenden der SSL-Verschl&#252;sselung
  Mit der SSL \(Secure Sockets Layer\)\-Verschlüsselung können verschlüsselte Daten in einem Netzwerk zwischen einer Instanz von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] und einer Clientanwendung übertragen werden.  
  
 Secure Sockets Layer \(SSL\) ist ein Protokoll zum Einrichten eines sicheren Kommunikationskanals, um das Abfangen von kritischen oder vertraulichen Informationen im Netzwerk und bei anderen Internetkommunikationen zu verhindern. Durch SSL können der Client und der Server die Identität des anderen authentifizieren. Nach dem Authentifizieren der Teilnehmer stellt SSL verschlüsselte Verbindungen zwischen ihnen bereit, damit die Nachrichten sicher übertragen werden können.  
  
 [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] stellt eine Infrastruktur bereit, mit der die Verschlüsselung für eine bestimmte Verbindung auf Grundlage der benutzerdefinierten Verbindungseigenschaften und der Server\- und Clienteinstellungen aktiviert und deaktiviert werden kann. Der Benutzer kann den Speicherort des Zertifikatspeichers und das Kennwort sowie einen Hostnamen zum Überprüfen des Zertifikats angeben und festlegen, wann der Verbindungskanal verschlüsselt werden soll.  
  
 Das Aktivieren der SSL\-Verschlüsselung erhöht die Sicherheit von Daten, die netzwerkübergreifend zwischen Instanzen von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] und Anwendungen übertragen werden. Durch das Aktivieren der Verschlüsselung kommt es jedoch zu Leistungseinbußen.  
  
 In den Themen in diesem Abschnitt werden die Unterstützung der SSL\-Verschlüsselung in der [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-Version und neue Verbindungseigenschaften sowie das Konfigurieren des Vertrauensspeichers auf Clientseite beschrieben.  
  
> [!NOTE]  
>  Für das Überprüfen eines SSL\-Zertifikats wird die **hostNameInCertificate**\-Verbindungseigenschaft empfohlen.  
  
## In diesem Abschnitt  
  
|Thema|Beschreibung|  
|-----------|------------------|  
|[Grundlegendes zur SSL-Unterstützung](../content/Understanding-SSL-Support.md)|Beschreibt die Unterstützung der SSL\-Verschlüsselung in [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)].|  
|[Herstellen von Verbindungen mit SSL-Verschlüsselung](../content/Connecting-with-SSL-Encryption.md)|Beschreibt das Herstellen einer Verbindung mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank mithilfe der neuen SSL\-spezifischen Verbindungseigenschaften.|  
|[Konfigurieren des Clients für SSL-Verschlüsselung](../content/Configuring-the-Client-for-SSL-Encryption.md)|Beschreibt das Konfigurieren des Standardvertrauensspeichers auf Clientseite und das Importieren eines privaten Zertifikats im Vertrauensspeicher des Clientcomputers.|  
  
## Siehe auch  
 [Sichern von JDBC-Treiberanwendungen](../content/Securing-JDBC-Driver-Applications.md)  
  
  