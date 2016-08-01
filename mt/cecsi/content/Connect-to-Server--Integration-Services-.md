---
title: "Verbindung mit Server herstellen (Integration Services)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5be897bd-f36c-4c6a-a91a-13d0d016f8b6
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
# Verbindung mit Server herstellen (Integration Services)
Verwenden Sie dieses Dialogfeld, um anzuzeigen, oder geben Sie Optionen für die Verbindung mit [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssISnoversion](../content/includes/ssISnoversion_md.md)].  
  
## Optionen  
**Servertyp**  
Wenn Sie einen Server über den Objekt-Explorer registrieren, wählen Sie den Typ des Servers aus, mit dem eine Verbindung hergestellt wird: [!INCLUDE[ssDE](../content/includes/ssDE_md.md)], Analysis Services, Reporting Services oder Integration Services. Im verbleibenden Bereich des Dialogfelds werden nur die Optionen angezeigt, die auf den ausgewählten Servertyp zutreffen. Das Feld Servertyp wird gelesen, wenn Sie einen Server über registrierte Server registrieren,\-und die in der Komponente registrierte Server angezeigten Servertyp übereinstimmt. Zum Registrieren eines anderen Servertyps wählen Sie auf der Symbolleiste "Registrierte Server" die Option [!INCLUDE[ssDE](../content/includes/ssDE_md.md)], "Analysis Services", "Reporting Services" oder "Integration Services" aus. Anschließend können Sie mit der Registrierung eines neuen Servers beginnen.  
  
**Servername**  
Wählen Sie den Server für die Verbindungsherstellung aus. Standardmäßig wird die Serverinstanz angezeigt, mit der zuletzt eine Verbindung bestanden hat.  
  
> [!NOTE]  
> Verwenden Sie keine *<servername>*\\*<instancename>*, da [!INCLUDE[ssIS](../content/includes/ssIS_md.md)] unterstützt nicht mehrere Instanzen auf einem Computer.  
  
**Authentifizierung**  
Für [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] steht nur die [!INCLUDE[ssIS](../content/includes/ssIS_md.md)] Windows-Authentifizierung zur Verfügung. Der Windows Authentifizierungsmodus ermöglicht Benutzern die Verbindung über ein Windows-Benutzerkonto.  
  
**Benutzername**  
Diese Option ist nicht verfügbar, da für [!INCLUDE[ssIS](../content/includes/ssIS_md.md)] nur die Windows-Authentifizierung zur Verfügung steht.  
  
**Kennwort**  
Diese Option ist nicht verfügbar, da für [!INCLUDE[ssIS](../content/includes/ssIS_md.md)] nur die Windows-Authentifizierung zur Verfügung steht.  
  
**Connect**  
Klicken Sie hier, um eine Verbindung mit dem oben ausgewählten Server herzustellen.  
  
**Optionen**  
Klicken Sie auf diese Schaltfläche, um zusätzliche Optionen für die Serververbindung anzuzeigen, z. B. zum Registrieren eines Servers oder zum Speichern des Kennworts.  
  
