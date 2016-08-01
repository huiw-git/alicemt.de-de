---
title: "Verbindung mit Server herstellen (Reporting Services)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ef81b658-8eb5-4636-ac81-eead10cc7b9f
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
# Verbindung mit Server herstellen (Reporting Services)
Verwenden Sie dieses Dialogfeld, um anzuzeigen, oder geben Sie Optionen für die Verbindung mit [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssRSnoversion](../content/includes/ssRSnoversion_md.md)].  
  
## Optionen  
**Servertyp**  
Beim Registrieren eines Servers bei **Objekt-Explorer**, wählen Sie den Typ des Servers für die Verbindung: [!INCLUDE[ssDE](../content/includes/ssDE_md.md)], Analysis Services, Reporting Services und Integration Services. Im verbleibenden Bereich des Dialogfelds werden nur die Optionen angezeigt, die auf den ausgewählten Servertyp zutreffen. Beim Registrieren eines Servers bei **registrierte Server**,  **Servertyp** Feld gelesen wird\-nur und entspricht den Typ des Servers angezeigt, der **registrierte Server** Komponente. Zum Registrieren eines anderen Servertyps wählen Sie [!INCLUDE[ssDE](../content/includes/ssDE_md.md)], Analysis Services, Reporting Services und Integration Services aus der **registrierte Server** Symbolleiste einen neuen Server registrieren.  
  
**Servername**  
Welche Werte Sie eingeben müssen, hängt von dem Servermodus der Berichtsserverinstanz ab, mit der Sie eine Verbindung herstellen.  
  
Wenn es sich um einen Berichtsserver handelt, der im einheitlichen Modus ausgeführt wird, geben Sie die Berichtsserverinstanz an, mit der eine Verbindung hergestellt werden soll. Wenn Sie die Standardinstanz verwenden, ist der Servername in der Regel der Name des Computers. Wenn Sie eine benannte Instanz installiert haben, fügen Sie den Namen der Instanz an den Servernamen in folgendem Format: <servername>\\<InstanceName>. Reporting Services verwendet den umgekehrten Schrägstrich zur Trennung des Instanznamens.  
  
Für einen Berichtsserver, der im integrierten SharePoint-Modus ausgeführt wird, müssen Sie eine SharePoint-Site angeben. Sie können eine beliebige Site aus einer Sitesammlung angeben, die mit [!INCLUDE[ssRSnoversion](../content/includes/ssRSnoversion_md.md)] integriert ist. Die URL, die Sie bereitstellen, muss das HTTP oder HTTPS-Präfix enthalten. Um in Management Studio eine Verbindung mit der SharePoint-Site herstellen zu können, müssen Sie über Zugriffsberechtigungen für die SharePoint-Site verfügen. Die Ihnen zugewiesene Berechtigungsstufe bestimmt, welche Elemente Sie anzeigen und verwalten können. Weitere Informationen finden Sie unter [Gewusst wie: registrieren und Verbindung mit einem Berichtsserver](assetId:///c875ff87-ee7d-443a-a702-bdb4b6c27c6e).  
  
**Authentifizierung**  
[!INCLUDE[ssRSnoversion](../content/includes/ssRSnoversion_md.md)] kann so konfiguriert werden angenommen Windows-authentifizierungsanforderungen oder Formularauthentifizierungsanforderungen, die durch eine benutzerdefinierte Erweiterung behandelt werden, die Sie bereitstellen. Wählen Sie beim Herstellen einer Verbindung mit [!INCLUDE[ssRSnoversion](../content/includes/ssRSnoversion_md.md)] einen der folgenden Authentifizierungsmodi aus:  
  
**Windows-Authentifizierungsmodus (Windows-Authentifizierung)**  
Stellt die Verbindung zur Berichtsserverinstanz mithilfe der Anmeldeinformationen von [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] Windows her.  
  
**Standardauthentifizierung**  
Verbinden mit **Standardauthentifizierung** Wenn Reporting Services-Installation für die Verwendung der Standardauthentifizierung konfiguriert ist.  
  
**Formularauthentifizierung**  
Verbinden mit **Formularauthentifizierung** Wenn Reporting Services-Installation für die Verwendung der Formularauthentifizierung konfiguriert ist.  
  
**Benutzername**  
Geben Sie den Benutzernamen ein, der für die Verbindung verwendet werden soll. Diese Option ist nur verfügbar, wenn Sie **Standardauthentifizierung** oder **Formularauthentifizierung**ausgewählt haben.  
  
**Kennwort**  
Geben Sie das Kennwort für den Benutzernamen ein. Diese Option kann nur bearbeitet werden, wenn Sie **Standardauthentifizierung** oder **Formularauthentifizierung**ausgewählt haben.  
  
**Connect**  
Klicken Sie hier, um eine Verbindung mit dem oben ausgewählten Server herzustellen.  
  
**Optionen**  
Klicken Sie auf diese Schaltfläche, um zusätzliche Optionen für die Serververbindung anzuzeigen, z. B. zum Registrieren eines Servers oder zum Speichern des Kennworts.  
  
## Siehe auch  
[Konfigurieren der Verbindung eines Berichtsservers](assetId:///9759a9fb-35e9-4215-969b-a9f1fea18487)  
[Vorgehensweise: Registrieren eines Berichtsservers und Herstellen einer Verbindung mit dem Berichtsserver](assetId:///c875ff87-ee7d-443a-a702-bdb4b6c27c6e)  
[Konfigurieren der Authentifizierung in Reporting Services](assetId:///753c2542-0e97-4d8f-a5dd-4b07a5cd10ab)  
  
