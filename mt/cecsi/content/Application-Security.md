---
title: "Anwendungssicherheit"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 940879b4-aa0f-41ce-a369-6cfc0e78e01d
caps.latest.revision: 23
caps.handback.revision: 22
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
# Anwendungssicherheit
  Wenn Sie [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] verwenden, müssen Sie Vorsichtsmaßnahmen ergreifen, um die Sicherheit der Anwendung sicherzustellen. Die folgenden Abschnitte enthalten Informationen zu den Schritten, die Sie zum Sichern der Anwendung ergreifen können.  
  
## Verwenden von Java\-Richtlinienberechtigungen  
 Wenn Sie [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] verwenden, müssen Sie die für den JDBC\-Treiber erforderlichen Java\-Richtlinienberechtigungen angeben. Die JRE \(Java Runtime Environment\) stellt ein umfassendes Sicherheitsmodell bereit, mit dem zur Laufzeit ermittelt werden kann, ob ein Thread auf eine Ressource zugreifen kann. Dieser Zugriff kann durch Sicherheitsrichtliniendateien gesteuert werden. Die Richtliniendateien werden vom Entwickler und vom Systemadministrator des Containers verwaltet. Die in diesem Thema aufgeführten Berechtigungen wirken sich jedoch auf die Funktionsweise des JDBC\-Treibers aus.  
  
 Eine normale Berechtigung in der Richtliniendatei sieht folgendermaßen aus:  
  
```  
// Example policy file entry.  
grant [signedBy <signer>,] [codeBase <code source>] {  
   permission  <class>  [<name> [, <action list>]];  
};  
```  
  
 Die folgende Codebasis muss auf die Codebasis des JDBC\-Treibers beschränkt werden, damit die minimal erforderlichen Privilegien gewährt werden.  
  
```  
grant codeBase "file:/install_dir/lib/-" {  
  
// Grant access to data source.  
permission java.util.PropertyPermission "java.naming.*", "read,write";  
  
// Specify which hosts can be connected to.  
permission java.net.socketPermission "host:port", "connect";  
  
// Logger permission to take advantage of logging.  
permission java.util.logging.LoggingPermission;  
  
// Grant listen/connect/accept permissions to the driver if   
// connecting to a named instance as the client driver.   
// This connects to a udp service and listens for a response.  
permission java.net.SocketPermission "*", "listen, connect, accept";   
};   
```  
  
> [!NOTE]  
>  Der Code "file:\/install\_dir\/lib\/\-" bezieht sich auf das Installationsverzeichnis des JDBC\-Treibers.  
  
## Schützen der Serverkommunikation  
 Wenn Sie den JDBC\-Treiber für die Kommunikation mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank verwenden, können Sie den Kommunikationskanal mit IPSec \(Internet Protocol Security\) und\/oder SSL \(Secure Sockets Layer\) sichern.  
  
 Die SSL\-Unterstützung kann verwendet werden, um zusätzlich zu IPSEC eine weitere Schutzebene bereitzustellen. Weitere Informationen zum Verwenden von SSL finden Sie unter [Verwenden der SSL-Verschlüsselung](../content/Using-SSL-Encryption.md).  
  
## Siehe auch  
 [Sichern von JDBC-Treiberanwendungen](../content/Securing-JDBC-Driver-Applications.md)  
  
  