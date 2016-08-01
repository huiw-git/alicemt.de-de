---
title: "Erstellen einer Multiserverumgebung"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: edc2b60d-15da-40a1-8ba3-f1d473366ee6
caps.latest.revision: 5
caps.handback.revision: 4
manager: jhubbard
translation.priority.mt: 
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
# Erstellen einer Multiserverumgebung
Die Multiserververwaltung erfordert, dass Sie einen Masterserver (MSX) und einen oder mehrere Zielserver (TSX) einrichten. Aufträge, die auf allen Zielservern verarbeitet werden, müssen zuerst auf dem Masterserver definiert werden, und dann zu den Zielservern heruntergeladen werden.  
  
Die vollständige SSL-Verschlüsselung (Secure Sockets Layer) und die Zertifikatüberprüfung sind für Verbindungen zwischen Masterservern und Zielservern standardmäßig aktiviert. Weitere Informationen finden Sie unter [Festlegen von Verschlüsselungsoptionen auf Zielservern](../content/Set-Encryption-Options-on-Target-Servers.md).  
  
Wenn Sie eine große Anzahl von Zielservern haben, vermeiden Sie, den Masterserver auf einem Produktionsserver zu definieren, der bedeutende Leistungsanforderungen bezüglich anderer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Funktionalität hat, da der Zielserverdatenverkehr die Leistung auf dem Produktionsserver verlangsamen kann. Wenn Sie auch Ereignisse an einen dedizierten Masterserver weiterleiten, können Sie die Administration auf einem Server zentralisieren. Weitere Informationen finden Sie unter [Ereignisse verwalten](../content/Manage-Events.md).  
  
> [!NOTE]  
> Verarbeiten von Multiserveraufträgen verwenden die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Dienstkonto muss ein Mitglied der **Msdb** Datenbankrolle **TargetServersRole** auf dem Masterserver. Der Masterserver-Assistent fügt dieser Rolle im Rahmen des Eintragungsprozesses automatisch das Dienstkonto hinzu.  
  
## Überlegungen zu Multiserverumgebungen  
Finden Sie in der folgenden Tabelle für unterstützte MSX\/TSX-Konfigurationen.  
  
||**TSX \= 7.0**|**TSX \= 8.0 < SP3**|**TSX \= 8.0 SP3 oder höher**|**TSX \= 9.0**|**TSX\= 10.0**|**TSX \= 10.5**|**TSX \= 11.0**|  
|-|------------------|------------------------|--------------------------------|------------------|------------------|-------------------|-------------------|  
|**MSX \= 7.0**|ja|ja|Nein|Nein|Nein|Nein|Nein|  
|**MSX \= 8.0 < SP3**|ja|ja|Nein|Nein|Nein|Nein|Nein|  
|**MSX \= 8.0 SP3 oder höher**|Nein|Nein|ja|ja|ja|ja|ja|  
|**MSX \= 9.0**|Nein|Nein|Nein|ja|ja|ja|ja|  
|**MSX \= 10.0**|Nein|Nein|Nein|Nein|ja|ja|ja|  
|**MSX \= 10.5**|Nein|Nein|Nein|Nein|Nein|ja|ja|  
|**MSX \= 11.0**|Nein|Nein|Nein|Nein|Nein|Nein|ja|  
  
Beachten Sie die folgenden Punkte, wenn Sie eine Multiserverumgebung erstellen:  
  
-   Jeder Zielserver berichtet nur einem Masterserver. Sie müssen einen Zielserver aus einem Masterserver austragen, bevor Sie ihn bei einem anderen Masterserver eintragen können.  
  
-   Wenn Sie den Namen eines Zielservers ändern, müssen sie vor dem Ändern des Namens und die erneute austragen\-nach der Änderung eintragen.  
  
-   Wenn Sie eine Multiserverkonfiguration auflösen möchten, müssen Sie alle Zielserver aus dem Masterserver austragen.  
  
-   SQL Server Integration Services unterstützt nur Zielserver, die über dieselbe Version wie der Masterserver oder eine höhere Version verfügen.  
  
## Verwandte Aufgaben  
In den folgenden Themen werden allgemeine Aufgaben zum Erstellen einer Multiserverumgebung beschrieben.  
  
|Beschreibung|Thema|  
|---------------|---------|  
|Beschreibt, wie ein Masterserver erstellt wird.|[Einrichten eines Masterservers](../content/Make-a-Master-Server.md)|  
|Beschreibt, wie ein Zielserver erstellt wird.|[Erstellen eines Zielservers](../content/Make-a-Target-Server.md)|  
|Beschreibt, wie ein Zielserver bei einem Masterserver eingetragen wird.|[Eintragen eines Zielservers bei einem Masterserver](../content/Enlist-a-Target-Server-to-a-Master-Server.md)|  
|Beschreibt, wie der Austritt eines Zielservers aus einem Masterserver vollzogen wird.|[Vollziehen des Austritts eines Zielservers aus einem Masterserver](../content/Defect-a-Target-Server-from-a-Master-Server.md)|  
|Beschreibt, wie der Austritt mehrerer Zielserver aus einem Masterserver vollzogen wird.|[Vollziehen des Austritts mehrerer Zielserver aus einem Masterserver](../content/Defect-Multiple-Target-Servers-from-a-Master-Server.md)|  
|Beschreibt, wie der Status eines Zielservers überprüft wird.|[sp_help_targetserver (Transact-SQL)](assetId:///f841d3bd-901a-4980-ad0b-1c6eeba3f717)<br /><br />[sp_help_targetservergroup (Transact-SQL)](assetId:///ec3a4a68-b591-431c-9518-053ede522d0c)|  
  
## Siehe auch  
[Problembehandlung von proxybasierten Multiserveraufträgen](../content/Troubleshoot-Multiserver-Jobs-That-Use-Proxies.md)  
  
