---
title: "Verwenden von Leistungsobjekten"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 830b843a-6b2a-4620-a51b-98358e9fc54b
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
# Verwenden von Leistungsobjekten
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent gehören Leistungsobjekte und Leistungsindikatoren zum Überwachen der Leistung des Diensts. Mithilfe dieser Leistungsobjekte können Sie das Windows-Tool Systemmonitor verwenden, um festzustellen, welche Vorgänge vom [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Dienst im Hintergrund ausgeführt werden. Sie können beispielsweise die Anzahl der aktiven Aufträge feststellen, die vom [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Dienst aktuell ausgeführt werden, um blockierte Aufträge zu identifizieren.  
  
Die Leistungsobjekte und Leistungsindikatoren des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Diensts sind für jede Instanz von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] vorhanden, die auf einem Computer installiert ist. Leistungsobjekte sind nach der Instanz von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] benannt, die jedes Objekt repräsentiert.  
  
Die folgende Tabelle veranschaulicht, wie die Leistungsobjekte des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Diensts benannt werden:  
  
|Instanztyp|Objektname|  
|-----------------|---------------|  
|Standardwert|**SQLAgent:***Objekt*:*Zähler*|  
|Benannt|**SQLAgent$**<br /> **& #42; Instanz\_Name & #42;:***Objekt*:*Zähler*|  
  
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] enthält die folgenden Leistungsobjekte für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent.  
  
|Objektname|Beschreibung|  
|---------------|---------------|  
|[SQLAgent:Aufträge](assetId:///225b5e2d-4a78-4178-b2b6-b419df83c4aa)|Leistungsinformationen zu gestarteten Aufträgen, Erfolgsrate und aktuellem Status|  
|[SQLAgent:Auftragsschritte](assetId:///44f9983c-1753-4fe0-8475-973aa2460b3a)|Statusinformationen zu Auftragsschritten|  
|[SQLAgent:Warnungen](assetId:///e5e37f74-ee88-46d0-ad8f-71fd1b1fa64a)|Informationen zur Anzahl der Warnungen und Benachrichtigungen|  
|[SQLAgent:Statistik](assetId:///ebe92bfa-0721-48aa-9ba6-e7904ad265a1)|Allgemeine Leistungsinformationen|  
  
## Siehe auch  
[Überwachen und Optimieren der Leistung](assetId:///87f23f03-0f19-4b2e-bfae-efa378f7a0d4)  
[Vorgehensweise: Starten des Systemmonitors (Windows)](assetId:///5e51bb79-5737-470b-9c47-fac330c001c5)  
  
