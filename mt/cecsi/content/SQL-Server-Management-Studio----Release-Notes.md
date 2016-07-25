---
title: "Versionshinweise f&#252;r SQL Server Management Studio"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0b95337b-80bf-4624-8f5d-cdaf6181d3b8
caps.latest.revision: 47
caps.handback.revision: 35
manager: jeffreyg
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
# Versionshinweise f&#252;r SQL Server Management Studio
Willkommen bei unserem Preview-Version von SQL Server Management Studio\!  Diese Version von SQL Server Management Studio (SSMS) ist eine eigenständige\-außerhalb der SQL Server-Version installiert. Unser Ziel besteht darin, diese häufig zu aktualisieren und neue Funktionen, Korrekturen und Hilfestellungen für die neuesten Funktionen des SQL Servers und der Azure SQL-Datenbank bereitzustellen.

Um die neuesten SQL Server Management Studio zu installieren, finden Sie unter [Herunterladen von SQL Server Management Studio & #40; SSMS & #41;](../content/Download-SQL-Server-Management-Studio--SSMS-.md).

Dies sind Probleme und Einschränkungen, die in Verbindung mit der neuesten SQL Server Management Studio Version bestehen:

1.  **SSMS wird eine Warnung ausgegeben, wenn eine SQL Server 2016-Instanz aus einem nicht kompatiblen Build auf dem gleichen Computer installiert ist.**
     Wenn Sie versuchen, die neueste Version von SSMS auf einem Computer mit einer SQL Server 2016 Preview-Instanz zu installieren, erhalten Sie ein Dialogfeld dazu aufgefordert, das Überschreiben mit SQL Server gemeinsam verwendete Komponenten zu bestätigen. Die Version von SQL Server 2016, die für die neueste Version von SSMS kann hier heruntergeladen werden: [SQL Server](http://www.microsoft.com/en-us/evalcenter/evaluate-sql-server-2016).

2. **SSMS wird nicht Wartungspläne für SQL Server 2008 R2 und früheren Versionen von SQL Server gespeichert werden.**
    Wir arbeiten an der Behebung dieses Problems. In der Zwischenzeit können Sie die [Version 2014 SSMS](../content/Previous-SQL-Server-Management-Studio-Releases.md) die Wartungspläne zu speichern.

3.  **SQL Server-Konfigurations-Manager kann nicht gestartet werden, wenn kein SQL auf dem Clientcomputer installiert Server** Wenn Sie nicht auf dem Clientcomputer installierten SQL Server und SQL Server-Konfigurations-Manager zu starten, wird den folgenden Fehler angezeigt:  `Cannot connect to WMI provider. You do not have permission or the server is unreachable. Note that you can only manage SQL Server 2005 and later servers with SQL Server Configuration Manager. Invalid namespace \[0x8004100e]`, 
 
     * Wenn Sie SQL Server-Instanzen 'Registrierte Server'-Liste in SSMS hinzugefügt haben:
        1. Navigieren Sie zu 'Registrierte Server'-Ansicht in SSMS.
        2. Mit der rechten Maustaste in der SQL Server-Instanz, die Sie konfigurieren möchten.
        3. Wählen Sie SQL Server Configuration Manager... aus dem Kontextmenü.  
        
      * Wenn Sie eine SQL Server-Instanz nicht 'Registrierte Server'-Liste in SSMS hinzugefügt haben:
        1. Öffnen Sie einen Promopt Befehl als Administrator aus.
        2. Führen Sie die Mofcomp-Tool, mit dem folgenden Befehl: `mofcomp "%programfiles(x86)%\Microsoft SQL Server\130\Shared\sqlmgmproviderxpsp2up.mof"`
        3. Führen Sie nach dem Ausführen des Tools Mofcomp folgenden Befehle, um die Änderungen wirksam werden den WMI-Dienst neu starten: `net stop "Windows Management Instrumentation"`
        `net start “Windows Management Instrumentation”`


## Feedback

![Needhelp_person_icon](../content/media/needhelp_person_icon.png) [SQL Client Tools-Forum](https://social.msdn.microsoft.com/Forums/en-US/home?forum=sqltools) |  [Melden eines Problems oder an Microsoft Connect](https://connect.microsoft.com/SQLServer/Feedback).

## Siehe auch
[Herunterladen von SQL Server Management Studio & #40. SSMS & #41;](../content/Download-SQL-Server-Management-Studio--SSMS-.md)
[Vorherigen SQL Server Management Studio-Versionen](../content/Previous-SQL-Server-Management-Studio-Releases.md)
[SQL Server Management Studio](../Topic/SQL%20Server%20Management%20Tools%20with%20SSMS.md)

