---
title: "Verbindung mit Server herstellen (Seite Anmeldung im Datenbankmodul)"
ms.custom: 
  - SQL2016_New_Updated
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e08cfbc3-bed5-4401-a13b-1c66d902fe32
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
# Verbindung mit Server herstellen (Seite Anmeldung im Datenbankmodul)
Verwenden Sie diese Registerkarte, um anzuzeigen, oder geben Sie Optionen für die Verbindung mit [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)].  
  
> [!NOTE]  
> Zum Herstellen einer Verbindung mit der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Authentifizierung muss [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] im [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]- und Windows-Authentifizierungsmodus konfiguriert werden. Weitere Informationen dazu, wie Sie den Authentifizierungsmodus zu bestimmen und Ändern des Authentifizierungsmodus finden Sie unter [Gewusst wie: Ändern des Serverauthentifizierungsmodus](assetId:///79babcf8-19fd-4495-b8eb-453dc575cac0).  
  
## Optionen  
**Servertyp**  
Wenn Sie einen Server über den Objekt-Explorer registrieren, wählen Sie den Typ des Servers aus, mit dem eine Verbindung hergestellt wird: [!INCLUDE[ssDE](../content/includes/ssDE_md.md)], Analysis Services, Reporting Services oder Integration Services. Im verbleibenden Bereich des Dialogfelds werden nur die Optionen angezeigt, die auf den ausgewählten Servertyp zutreffen. Wenn Sie einen Server über registrierte Server registrieren der **Servertyp** Feld gelesen wird\-und die in der Komponente registrierte Server angezeigten Servertyp übereinstimmt. Zum Registrieren eines anderen Servertyps wählen Sie auf der Symbolleiste "Registrierte Server" die Option [!INCLUDE[ssDE](../content/includes/ssDE_md.md)], "Analysis Services", "Reporting Services" oder "Integration Services" aus. Anschließend können Sie mit der Registrierung eines neuen Servers beginnen.  
  
Beim Verbinden mit einer Instanz von der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Datenbankmodul über [!INCLUDE[ssSDSfull](../content/includes/ssSDSfull_md.md)], verwenden Sie [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Authentifizierung, und geben Sie eine Datenbank in der **mit Server verbinden** Dialogfelds die **Verbindungseigenschaften** Registerkarte. Wählen Sie aus der **Verbindung verschlüsseln** Kontrollkästchen.  
  
In der Standardeinstellung [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] wird eine Verbindung mit **master**. Wenn Sie eine Benutzerdatenbank angeben, wird im Objekt-Explorer nur diese Datenbank mit den zugehörigen Objekten angezeigt. Wenn Sie mit verbinden **master**, werden alle Datenbanken angezeigt. Weitere Informationen finden Sie unter der [Übersicht für Windows Azure SQL-Datenbank](http://go.microsoft.com/fwlink/?LinkId=163948).  
  
**Servername**  
Wählen Sie die Serverinstanz aus, mit der eine Verbindung hergestellt werden soll. Standardmäßig wird die Serverinstanz angezeigt, mit der zuletzt eine Verbindung bestanden hat.  
  
**Authentifizierung**  
Beim Herstellen einer Verbindung mit einer Instanz von [!INCLUDE[ssDEnoversion](../content/includes/ssDEnoversion_md.md)] sind zwei Authentifizierungsmodi verfügbar:  
  
Beim Verbinden mit einer Instanz von der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Datenbankmodul über [!INCLUDE[ssSDS](../content/includes/ssSDS_md.md)], verwenden Sie [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Authentifizierung, und geben Sie eine Datenbank in der **mit Server verbinden** Dialogfelds die **Verbindungseigenschaften** Registerkarte. Wählen Sie aus der **Verbindung verschlüsseln** Kontrollkästchen.  
  
In der Standardeinstellung [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] wird eine Verbindung mit **master**. Wenn Sie eine Benutzerdatenbank angeben, wird im Objekt-Explorer nur diese Datenbank mit den zugehörigen Objekten angezeigt. Wenn Sie mit verbinden **master**, werden alle Datenbanken angezeigt. Weitere Informationen finden Sie unter der [Übersicht für Windows Azure SQL-Datenbank](http://go.microsoft.com/fwlink/?LinkId=163948).  
  
**Windows-Authentifizierung**  
[!INCLUDE[msCoName](../content/includes/msCoName_md.md)] Der Windows Authentifizierungsmodus ermöglicht Benutzern die Verbindung über ein Windows-Benutzerkonto.  
  
**SQL Server-Authentifizierung (SQL server authentication)**  
Wenn ein Benutzer eine Verbindung herstellt mit einem angegebenen Benutzernamen und Kennwort von einer nicht\-Vertrauenswürdige Verbindung, [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] führt die Authentifizierung selbst durch Überprüfen, wenn eine [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Anmeldekonto eingerichtet wurde und wenn das angegebene Kennwort dem entspricht zuvor aufgezeichneten. Wenn kein Anmeldekonto in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] eingerichtet wurde, schlägt die Authentifizierung fehl, und der Benutzer erhält eine Fehlermeldung.  
  
> [!IMPORTANT]  
> Verwenden Sie nach Möglichkeit die Windows-Authentifizierung.  
  
**Active Directory-Kennwort-Authentifizierung**  
Azure Active Directory-Authentifizierung ist ein Mechanismus für das Herstellen einer Verbindung mit [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssSDSfull](../content/includes/ssSDSfull_md.md)] mithilfe von Identitäten in Azure Active Directory (Azure AD).  Verwenden Sie diese Methode für die Verbindung mit [!INCLUDE[ssSDS](../content/includes/ssSDS_md.md)] Sie angemeldet sind, in Windows unter Verwendung von Anmeldeinformationen einer Domäne, die nicht mit Azure verbunden ist, oder mithilfe von Azure AD-Authentifizierung mithilfe von Azure AD auf die ursprüngliche oder die Domäne des Clients basieren. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit SQL-Datenbank unter Verwendung der Azure Active Directory-Authentifizierung](https://azure.microsoft.com/documentation/articles/sql-database-aad-authentication/).  
  
**Active Directory-integrierte Authentifizierung**  
Azure Active Directory-Authentifizierung ist ein Mechanismus für das Herstellen einer Verbindung mit [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssSDSfull](../content/includes/ssSDSfull_md.md)] mithilfe von Identitäten in Azure Active Directory (Azure AD). Verwenden Sie diese Methode für die Verbindung mit [!INCLUDE[ssSDS](../content/includes/ssSDS_md.md)] wenn Sie Windows mit Ihren Azure Active Directory-Anmeldeinformationen aus einer verbundenen Domäne angemeldet sind. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit SQL-Datenbank unter Verwendung der Azure Active Directory-Authentifizierung](https://azure.microsoft.com/documentation/articles/sql-database-aad-authentication/).  
  
**Benutzername**  
Der Windows-Benutzername für die Verbindung mit. Diese Option ist nur verfügbar, wenn Sie die Verbindung mit **Active Directory-Kennwort-Authentifizierung**. Er wird gelesen\-nur, wenn Sie die Auswahl **Windows-Authentifizierung**.  
  
**Anmeldename**  
Geben Sie den Anmeldenamen für die Verbindung ein. Diese Option ist nur verfügbar, wenn Sie zum Verbinden die Authentifizierung von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ausgewählt haben.  
  
**Kennwort**  
Geben Sie das Kennwort für die Anmeldung ein. Sie können diese Option nur bearbeiten, wenn Sie zum Verbinden die Authentifizierung von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ausgewählt haben.  
  
**Kennwort speichern**  
Aktivieren Sie dieses Kontrollkästchen, damit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] das eingegebene Kennwort speichert. Diese Option wird nur angezeigt, wenn Sie zum Verbinden die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Authentifizierung ausgewählt haben.  
  
**Connect**  
Klicken Sie hier, um eine Verbindung mit dem oben ausgewählten Server herzustellen.  
  
**Optionen**  
Klicken Sie hier, um die Anzeige des Dialogfelds zu ändern und die zusätzlichen Serververbindungsoptionen, z. B. Speichern des Kennworts, auszublenden.  
  
