---
title: "Verbindung mit Server herstellen (Datenbankmodul)"
ms.custom: 
  - SQL2016_New_Updated
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ee9017b4-8a19-4360-9003-9e6484082d41
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
# Verbindung mit Server herstellen (Datenbankmodul)
Verwenden Sie dieses Dialogfeld, um anzuzeigen, oder geben Sie Optionen für die Verbindung mit [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)]. In den meisten Fällen können Sie durch Eingabe des Computernamens des Datenbankservers in verbinden die **Servername** und klicken Sie dann auf **Verbinden**. Wenn Sie eine Verbindung [!INCLUDE[ssExpress](../content/includes/ssExpress_md.md)], verwenden Sie den Computernamen gefolgt von **\\Sqlexpress**.  
  
Viele Faktoren können Auswirkungen auf die Fähigkeit zum Herstellen der Verbindung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] haben.  
  
## Optionen  
**Servertyp**  
Wenn Sie einen Server über den Objekt-Explorer registrieren, wählen Sie den Typ des Servers aus, mit dem die Verbindung hergestellt werden soll: [!INCLUDE[ssDE](../content/includes/ssDE_md.md)], [!INCLUDE[ssASnoversion](../content/includes/ssASnoversion_md.md)], [!INCLUDE[ssRSnoversion](../content/includes/ssRSnoversion_md.md)] oder [!INCLUDE[ssISnoversion](../content/includes/ssISnoversion_md.md)]. Im verbleibenden Bereich des Dialogfelds werden nur die Optionen angezeigt, die auf den ausgewählten Servertyp zutreffen. Wenn Sie einen Server über registrierte Server registrieren der **Servertyp** Feld gelesen wird\-und die in der Komponente registrierte Server angezeigten Servertyp übereinstimmt. Zum Registrieren eines anderen Servertyps wählen Sie auf der Symbolleiste Registrierte Server [!INCLUDE[ssDE](../content/includes/ssDE_md.md)], [!INCLUDE[ssASnoversion](../content/includes/ssASnoversion_md.md)], [!INCLUDE[ssRSnoversion](../content/includes/ssRSnoversion_md.md)], [!INCLUDE[ssEW](../content/includes/ssEW_md.md)] oder [!INCLUDE[ssISnoversion](../content/includes/ssISnoversion_md.md)] aus, bevor Sie mit der Registrierung eines neuen Servers beginnen.  
  
**Servername**  
Wählen Sie die Serverinstanz aus, mit der eine Verbindung hergestellt werden soll. Standardmäßig wird die Serverinstanz angezeigt, mit der zuletzt eine Verbindung bestanden hat.  
  
> [!NOTE]  
> Verbindung mit einer aktiven Instanz von [!INCLUDE[ssExpress](../content/includes/ssExpress_md.md)] eine Verbindung mithilfe von named Pipes-Protokoll, die Angabe des Pipenamens, z. B. Np:\\\\.\\Pipe\\3C3DF6B1\-2262\-47\\Tsql\\finden Sie weitere Informationen Abfragen der [!INCLUDE[ssExpress](../content/includes/ssExpress_md.md)] Dokumentation.  
  
**Authentifizierung**  
Drei Authentifizierungsmodi sind verfügbar, wenn eine Verbindung zu einer Instanz von Herstellen der [!INCLUDE[ssDE](../content/includes/ssDE_md.md)].  
  
**Windows-Authentifizierung**  
[!INCLUDE[msCoName](../content/includes/msCoName_md.md)] Der Windows Authentifizierungsmodus ermöglicht Benutzern die Verbindung über ein Windows-Benutzerkonto.  
  
**SQL Server-Authentifizierung (SQL server authentication)**  
Wenn ein Benutzer eine Verbindung herstellt mit einem angegebenen Benutzernamen und Kennwort von einer nicht\-Vertrauenswürdige Verbindung, [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] führt die Authentifizierung selbst durch Überprüfen, wenn eine [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Anmeldekonto eingerichtet wurde und wenn das angegebene Kennwort dem entspricht zuvor aufgezeichneten. Wenn kein Anmeldekonto in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] eingerichtet wurde, schlägt die Authentifizierung fehl, und der Benutzer erhält eine Fehlermeldung.  
  
> [!IMPORTANT]  
> Verwenden Sie nach Möglichkeit die Windows-Authentifizierung oder die Active Directory-Kennwort-Authentifizierung.  
  
**Active Directory-Kennwort-Authentifizierung**  
Azure Active Directory-Authentifizierung ist ein Mechanismus für das Herstellen einer Verbindung mit [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssSDSfull](../content/includes/ssSDSfull_md.md)] mithilfe von Identitäten in Azure Active Directory (Azure AD).  Verwenden Sie diese Methode für die Verbindung mit [!INCLUDE[ssSDS](../content/includes/ssSDS_md.md)] Sie angemeldet sind, in Windows unter Verwendung von Anmeldeinformationen einer Domäne, die nicht mit Azure verbunden ist, oder mithilfe von Azure AD-Authentifizierung mithilfe von Azure AD auf die ursprüngliche oder die Domäne des Clients basieren. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit SQL-Datenbank unter Verwendung der Azure Active Directory-Authentifizierung](https://azure.microsoft.com/documentation/articles/sql-database-aad-authentication/).  
  
**Active Directory-integrierte Authentifizierung**  
Azure Active Directory-Authentifizierung ist ein Mechanismus für das Herstellen einer Verbindung mit [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssSDSfull](../content/includes/ssSDSfull_md.md)] mithilfe von Identitäten in Azure Active Directory (Azure AD). Verwenden Sie diese Methode für die Verbindung mit [!INCLUDE[ssSDS](../content/includes/ssSDS_md.md)] wenn Sie Windows mit Ihren Azure Active Directory-Anmeldeinformationen aus einer verbundenen Domäne angemeldet sind. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit SQL-Datenbank unter Verwendung der Azure Active Directory-Authentifizierung](https://azure.microsoft.com/documentation/articles/sql-database-aad-authentication/).  
  
**Benutzername**  
Der Windows-Benutzername für die Verbindung mit. Diese Option ist nur verfügbar, wenn Sie die Verbindung mit **Active Directory-Kennwort-Authentifizierung**. Er wird gelesen\-nur, wenn Sie die Auswahl **Windows-Authentifizierung**.  
  
**Anmeldename**  
Geben Sie den Anmeldenamen für die Verbindung ein. Diese Option ist nur verfügbar, wenn Sie die Verbindung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Authentifizierung oder oder Active Directory-Kennwort-Authentifizierung.  
  
**Kennwort**  
Geben Sie das Kennwort für die Anmeldung ein. Diese Option ist nur bearbeitet werden, wenn Sie ausgewählt haben, die Verbindung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Authentifizierung oder oder Active Directory-Kennwort-Authentifizierung.  
  
**Connect**  
Klicken Sie hier, um eine Verbindung mit dem oben ausgewählten Server herzustellen.  
  
**Optionen**  
Klicken Sie auf diese Schaltfläche, um zusätzliche Optionen für die Serververbindung anzuzeigen, z. B. zum Registrieren eines Servers oder zum Speichern des Kennworts.  
  
