---
title: "Einf&#252;hrung in SQL Server Management Studio f&#252;r Business Intelligence"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ffaa77b7-03d0-4d7a-aa42-c5091a4f2ceb
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
# Einf&#252;hrung in SQL Server Management Studio f&#252;r Business Intelligence
Verwenden Sie [!INCLUDE[ssASnoversion](../content/includes/ssASnoversion_md.md)] für den Zugriff auf und die Verwaltung von [!INCLUDE[ssISnoversion](../content/includes/ssISnoversion_md.md)], [!INCLUDE[ssRSnoversion](../content/includes/ssRSnoversion_md.md)] und [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)]. Obwohl alle drei Business Intelligence-Technologien auf [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] basieren, weichen die mit den jeweiligen Technologien verbundenen Verwaltungsaufgaben leicht voneinander ab.  
  
> [!NOTE]  
> Verwenden Sie zum Erstellen und Ändern von Projektmappen in [!INCLUDE[ssASnoversion](../content/includes/ssASnoversion_md.md)], [!INCLUDE[ssRSnoversion](../content/includes/ssRSnoversion_md.md)] und [!INCLUDE[ssISnoversion](../content/includes/ssISnoversion_md.md)] [!INCLUDE[ssBIDevStudioFull](../content/includes/ssBIDevStudioFull_md.md)] und nicht [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)]. [!INCLUDE[ssBIDevStudioFull](../content/includes/ssBIDevStudioFull_md.md)] ist eine Entwicklungsumgebung, die auf [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[vsprvs](../content/includes/vsprvs_md.md)].  
  
## Verwalten von Analysis Services-Lösungen mit SQL Server Management Studio  
[!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] ermöglicht das Verwalten von [!INCLUDE[ssASnoversion](../content/includes/ssASnoversion_md.md)] Objekte, z. B. wieder ausführen\-USV und Verarbeitung von Objekten.  
  
[!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)] Stellt ein [!INCLUDE[ssASnoversion](../content/includes/ssASnoversion_md.md)] Skript-Projekt, in dem Sie entwickeln, und speichern in MDX (Multidimensional Expressions), Data Mining Extensions (DMX) und XML for Analysis (XMLA) geschriebene Skripts. Verwenden Sie [!INCLUDE[ssASnoversion](../content/includes/ssASnoversion_md.md)] Skriptprojekte, um das Ausführen von Verwaltungsaufgaben oder Re\-erstellen Objekte, z. B. Datenbanken oder Cubes auf [!INCLUDE[ssASnoversion](../content/includes/ssASnoversion_md.md)] Instanzen. Sie können beispielsweise ein XMLA-Skript in einem [!INCLUDE[ssASnoversion](../content/includes/ssASnoversion_md.md)]-Skriptprojekt entwickeln, das neue Objekte direkt auf einer vorhandenen [!INCLUDE[ssASnoversion](../content/includes/ssASnoversion_md.md)]-Instanz erstellt. Die [!INCLUDE[ssASnoversion](../content/includes/ssASnoversion_md.md)]-Skriptprojekte können als Teil einer Lösung gespeichert werden und mit dem Quellcodeverwaltungssystem integriert werden.  
  
Weitere Informationen zur Verwendung von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)], finden Sie unter [entwickeln und implementieren mithilfe von SQL Server Management Studio](assetId:///c4f5a06b-e2e4-4660-a3a8-6fd356742c02).  
  
## Verwalten von Integration Services-Lösungen mit SQL Server Management Studio  
[!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] ermöglicht Ihnen die Verwendung der [!INCLUDE[ssISnoversion](../content/includes/ssISnoversion_md.md)] Dienst zu verwalten und ausgeführte Pakete überwachen können. Zudem können Sie [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)] zur Organisation von Paketen in Ordnern, zum Ausführen von Paketen, zum Im- und Exportieren von Paketen, zum Migrieren von DTS-Paketen (Data Transformation Services) sowie zum Aktualisieren von [!INCLUDE[ssISnoversion](../content/includes/ssISnoversion_md.md)]-Paketen verwenden.  
  
## Verwalten von Reporting Services-Projekten mit SQL Server Management Studio  
Verwenden Sie SQL Server Management Studio zum Aktivieren von Reporting Services-Funktionen und zum Verwalten von Server und Datenbanken sowie von Rollen und Aufträgen.  
  
Verwalten Sie freigegebene Zeitpläne mit dem Ordner Freigegebene Zeitpläne, und verwalten Sie Berichtsserver-Datenbanken (ReportServer, ReportServerTempdb). Sie erstellen eine RSExecRole auch in der Master-Systemdatenbank beim Wechsel von einer Berichtsserver-Datenbank zu einer neuen oder anderen SQL Server-Datenbankmodul ([!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]). Weitere Informationen zu diesen Aufgaben finden Sie unter den folgenden Themen:  
  
-   [Management Studio (Themen zur Vorgehensweisen)](assetId:///60685458-9108-47bf-820a-5e7db454d408)  
  
-   [Verwalten einer Berichtsserver-Datenbank](assetId:///97b2e1b5-3869-4766-97b9-9bf206b52262)  
  
-   [Vorgehensweise: Erstellen der Rolle 'RSExecRole'](assetId:///7ac17341-df7e-4401-870e-652caa2859c0)  
  
Zudem verwalten Sie den Server, indem Sie verschiedene Funktionen aktivieren und konfigurieren, Serverstandardwerte festlegen und Rollen und Aufträge verwalten. Weitere Informationen zu diesen Aufgaben finden Sie unter den folgenden Themen:  
  
-   [Vorgehensweise: Festlegen von Berichtsservereigenschaften (Management Studio)](assetId:///1ed0f84b-b12a-4e49-b65c-a11a99f9093f)  
  
-   [Vorgehensweise: Erstellen, Löschen oder Ändern einer Rolle (Management Studio)](assetId:///3d1d56e6-a283-44a7-8417-36cb4d2c74d1)  
  
-   [Aktivieren und Deaktivieren von clientseitigem Druck für Reporting Services](assetId:///0e709c96-7517-4547-8ef6-5632f8118524)  
  
## Siehe auch  
[Entwickeln und implementieren mithilfe von SQL Server Data Tools](assetId:///132ed779-3ec8-4734-9698-802116d1b017)  
[Reporting Services in SQL Server Data Tools](assetId:///0903c7b2-ac59-45f1-b7d0-922ecd9d76f8)  
  
