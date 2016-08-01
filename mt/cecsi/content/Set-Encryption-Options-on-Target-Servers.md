---
title: "Festlegen von Verschl&#252;sselungsoptionen auf Zielservern"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1a9fd539-e166-4ea8-9f21-ac400ca74dee
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
# Festlegen von Verschl&#252;sselungsoptionen auf Zielservern
Wenn Sie für die verschlüsselte SSL-Kommunikation (Secure Sockets Layer) zwischen Masterservern und einigen oder allen Zielservern kein Zertifikat verwenden können, aber den Kanal zwischen diesen verschlüsseln möchten, müssen Sie auf dem Zielserver die erforderliche Sicherheitsstufe konfigurieren.  
  
So konfigurieren Sie die entsprechende Ebene der Sicherheit für eine bestimmte Masterserver erforderlich\/Kommunikationskanal abzielen, legen Sie die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Registrierungsunterschlüssel **\\HKEY\_lokalen\_Computer\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\**<*Instanz\_Namen*>**\\SQLServerAgent\\MsxEncryptChannelOptions(REG\_DWORD)** auf dem Zielserver auf einen der folgenden Werte. Der Wert des <*Instanz\_Namen*> ist **MSSQL.***n*. Z. B. **MSSQL. 1** oder **MSSQL.3**.  
  
|Wert|Beschreibung|  
|---------|---------------|  
|**0**|Deaktiviert die Verschlüsselung zwischen diesem Zielserver und dem Masterserver. Wählen Sie diese Option nur aus, wenn der Kanal zwischen Zielserver und Masterserver auf andere Weise gesichert ist.|  
|**1**|Aktiviert nur die Verschlüsselung zwischen diesem Zielserver und dem Masterserver, eine Zertifikatüberprüfung ist jedoch nicht erforderlich.|  
|**2**|Aktiviert die vollständige SSL-Verschlüsselung und Zertifikatüberprüfung zwischen diesem Zielserver und dem Masterserver. Dies ist die Standardeinstellung. Es wird empfohlen, diesen Wert nicht zu ändern, es sei denn, dafür liegen spezifische Gründe vor.|  
  
Wenn **1** oder **2** angegeben ist, müssen Sie SSL aktiviert sowohl die Master-und Zielservern. Wenn **2** angegeben ist, muss Ihnen ein ordnungsgemäß signiertes Zertifikat vorhanden auch auf dem Masterserver.  
  
> [!CAUTION]  
> [!INCLUDE[ssNoteRegistry](../content/includes/ssNoteRegistry_md.md)]  
  
## Siehe auch  
[Vorgehensweise: Aktivieren von verschlüsselten Verbindungen zum Datenbankmodul (SQL Server-Konfigurations-Manager).](assetId:///e1e55519-97ec-4404-81ef-881da3b42006)  
  
