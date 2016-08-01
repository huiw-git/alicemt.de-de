---
title: "Konfigurieren von WMI zum Anzeigen des Serverstatus in SQL Server-Tools"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7e97197b-ed4d-40d1-9a52-9ab1d92401d7
caps.latest.revision: 4
caps.handback.revision: 3
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
# Konfigurieren von WMI zum Anzeigen des Serverstatus in SQL Server-Tools
In diesem Thema wird beschrieben, wie WMI konfiguriert wird, um den Serverstatus in SQL Server-Tools in [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] anzuzeigen. Bei der Verbindungsherstellung mit Servern wird von den Komponenten Registrierte Server und Objekt-Explorer von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] sowie auch vom [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Konfigurations-Manager Windows Management Instrumentation (WMI) zum Abrufen des Status der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Dienste (MSSQLSERVER) und [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Dienste (MSSQLSERVER) verwendet. Zum Anzeigen des Dienststatus muss der Benutzer über Remotezugriffsrechte für das WMI-Objekt verfügen. Zum Konfigurieren dieser Berechtigung muss auf dem Server WMI installiert sein.  
  
## <a name="SSMSProcedure"></a>So konfigurieren Sie die WMI-Berechtigung  
  
1.  Auf der **Start** auf dem Remoteserver, klicken Sie anschließend auf **Ausführen**.  
  
2.  In der **Öffnen** Geben Sie im Feld **wmimgmt.msc**, und klicken Sie dann auf **OK**.  
  
3.  In der **Windows-Verwaltungsinfrastruktur** Programmieren, rechts\-Klicken Sie auf **WMI-Steuerung (lokal)**, und klicken Sie dann auf **Eigenschaften**.  
  
4.  In der **Eigenschaften von WMI-Steuerung (lokal)** Dialogfeld auf die **Sicherheit** Registerkarte, erweitern Sie **Root**, und klicken Sie dann auf **CIMV2**.  
  
5.  Klicken Sie auf **Security** Öffnen der **Sicherheit für Stamm\\CIMV2** Dialogfeld.  
  
6.  Hinzufügen einer Gruppe oder der Benutzer die **Gruppen-oder Benutzernamen** und wählen Sie es.  
  
7.  In der **Berechtigungen für***<group or user>* Wählen Sie im die **Zulassen** Spalte, für die **Remoteaktivierung** über die Berechtigung, für Benutzer, die den Dienststatus Remote erkannt werden soll.  
  
## Siehe auch  
[Starten, Beenden oder Anhalten des SQL Server-Agent-Dienstes](../content/Start--Stop--or-Pause-the-SQL-Server-Agent-Service.md)  
  
