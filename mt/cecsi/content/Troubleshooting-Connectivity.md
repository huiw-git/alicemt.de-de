---
title: "Behandlung von Verbindungsproblemen"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bfba0b49-2e1f-411d-a625-d25fad9ea12d
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
# Behandlung von Verbindungsproblemen
  [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] setzt für die Kommunikation mit der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank voraus, dass TCP\/IP installiert und aktiv ist. Sie können mit dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Konfigurations\-Manager überprüfen, welche Netzwerkbibliotheksprotokolle installiert sind.  
  
 Für Datenbankverbindungsfehler gibt es eine Vielzahl von Gründen, Sie können u. a. folgende Änderungen vornehmen:  
  
-   TCP\/IP ist für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] nicht aktiviert, oder es wurde ein falscher Server oder eine falsche Portnummer angegeben. Überprüfen Sie, ob [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] an dem angegebenen Server und Port mit TCP\/IP lauscht. In diesem Fall wird eine ähnliche Ausnahme wie die folgende gemeldet: "Fehler bei der Anmeldung. Es konnte keine TCP\/IP\-Verbindung zum Host hergestellt werden." die auf einen der folgenden Fehler hinweist:  
  
    -   [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ist installiert, aber TCP\/IP wurde nicht mit der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Netzwerkkonfiguration für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] bzw. dem [!INCLUDE[ssVersion2000](../content/includes/ssVersion2000_md.md)]\-Konfigurations\-Manager für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] und höher als Netzwerkprotokoll für [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] installiert.  
  
    -   TCP\/IP ist als [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Protokoll installiert, überwacht aber nicht den in der JDBC\-Verbindungs\-URL angegebenen Port. Der Standardport ist 1433. [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] kann aber bei der Produktinstallation für das Lauschen an einem beliebigen Port konfiguriert werden. Vergewissern Sie sich, dass [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] an Port 1433 lauscht. Sollte der Port geändert worden sein, vergewissern Sie sich, dass der in der JDBC\-Verbindungs\-URL angegebene Port dem geänderten Port entspricht. Weitere Informationen zur JDBC\-Verbindungs\-URL finden Sie unter [Erstellen der Verbindungs-URL](../content/Building-the-Connection-URL.md).  
  
    -   Die Adresse des in der JDBC\-Verbindungs\-URL angegebenen Computers verweist nicht auf einen Server, auf dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] installiert und gestartet wurde.  
  
    -   Die TCP\/IP\-Netzwerkverbindung zwischen Client und dem Server mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] funktioniert nicht. Sie können die TCP\/IP\-Verbindung zu [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] mit telnet überprüfen. Geben Sie dazu an der Eingabeaufforderung beispielsweise `telnet 192.168.0.0 1433` ein, wobei es sich bei 192.168.0.0 um die Adresse des Computers mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] und bei 1433 um den Port handelt, an dem gelauscht wird. Wenn Sie eine Meldung erhalten, die darauf hinweist, dass keine Telnet\-Verbindung möglich ist, lauscht TCP\/IP nicht an dem entsprechenden Port für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Verbindungen. Überprüfen Sie mit der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Netzwerkkonfiguration für [!INCLUDE[ssVersion2000](../content/includes/ssVersion2000_md.md)] bzw. dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Konfigurations\-Manager für [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] und höher, ob [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] für den TCP\/IP\-Port 1433 konfiguriert ist.  
  
    -   Der vom Server verwendete Port wurde in der Firewall nicht geöffnet. Dazu gehört der Port, der vom Server verwendet wird, oder optional der Port, der einer benannten Instanz des Servers zugeordnet ist.  
  
-   Der angegebene Datenbankname ist falsch. Vergewissern Sie sich, dass Sie sich bei einer vorhandenen [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank anmelden.  
  
-   Der Benutzername oder das Kennwort ist falsch. Vergewissern Sie sich, dass die richtigen Werte verwendet werden.  
  
-   Wenn Sie die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Authentifizierung verwenden, setzt der JDBC\-Treiber voraus, dass [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] mit der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Authentifizierung installiert ist. Dabei handelt es sich nicht um die Standardeinstellung. Vergewissern Sie sich beim Installieren oder Konfigurieren der Instanz von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)], dass diese Option enthalten ist.  
  
## Siehe auch  
 [Diagnostizieren von Problemen mit dem JDBC-Treiber](../content/Diagnosing-Problems-with-the-JDBC-Driver.md)   
 [Verbinden von SQL Server mit dem JDBC-Treiber](../content/Connecting-to-SQL-Server-with-the-JDBC-Driver.md)  
  
  