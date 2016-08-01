---
title: "Problembehandlung von proxybasierten Multiserverauftr&#228;gen"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fc579bd3-010c-4f72-8b5c-d0cc18a1f280
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
# Problembehandlung von proxybasierten Multiserverauftr&#228;gen
Verteilte Aufträge mit Schritten, die einem Proxy zugeordnet sind, werden unter dem Kontext des Proxykontos auf dem Zielserver ausgeführt. Wenn Auftragsschritte, die Konten ein Fehler auf, wenn auf dem Masterserver heruntergeladen Proxy verwenden eine Überprüfung der **Fehler\_Nachricht** -Spalte in der **Sysdownloadlist** -Tabelle in der **Msdb** Datenbank für die folgenden Fehlermeldungen:  
  
-   "Für den Auftragsschritt ist ein Proxykonto erforderlich, das Proxyabgleichen ist auf dem Zielserver aber deaktiviert."  
  
    Um diesen Fehler zu beheben, legen die **\\HKEY\_lokalen\_Computer\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\MSSQL.***< n*>**\\SQLServerAgent\\AllowDownloadedJobsToMatchProxyName** Registrierungsunterschlüssel zu **1 (True)**. Standardmäßig ist dieser Unterschlüssel auf festgelegt **0** (**false**). Der Wert des **MSSQL.**<*n*> ist der Instanzname, z. B. **MSSQL. 1** oder **MSSQL.3**.  
  
-   "Proxy nicht gefunden."  
  
    Zum Beheben dieses Fehlers stellen Sie sicher, dass auf dem Zielserver ein Proxykonto vorhanden ist, das den gleichen Namen wie das Proxykonto des Masterservers hat, unter dem der Auftragsschritt ausgeführt wird.  
  
> [!CAUTION]  
> [!INCLUDE[ssNoteRegistry](../content/includes/ssNoteRegistry_md.md)]  
  
## Siehe auch  
[Erstellen einer Multiserverumgebung](../content/Create-a-Multiserver-Environment.md)  
  
