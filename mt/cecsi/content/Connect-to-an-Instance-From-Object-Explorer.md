---
title: "Verbinden mit einer Instanz mit dem Objekt-Explorer"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9803a8a0-a8f1-4b65-87b8-989b06850194
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
# Verbinden mit einer Instanz mit dem Objekt-Explorer
Um Objekte mittels Objekt-Explorer zu verwalten, müssen Sie zuerst den Objekt-Explorer mit der Instanz verbinden, die die Objekte enthält. Sie können den Objekt-Explorer gleichzeitig mit mehreren Instanzen verbinden.  
  
## Herstellen einer Verbindung zwischen dem Objekt-Explorer und einem Server  
Um den Objekt-Explorer verwenden zu können, müssen Sie zuerst eine Verbindung mit einem Server herstellen. Klicken Sie auf **Verbinden** auf der Symbolleiste des Objekt-Explorer, und wählen Sie den Typ des Servers aus der Dropdownliste\--Liste. Das Dialogfeld **Verbindung mit Server herstellen** wird geöffnet. Um eine Verbindung herzustellen, sind als Mindestangabe der Name des Servers und die richtigen Authentifizierungsinformationen erforderlich.  
  
## Optionale Verbindungseinstellungen für den Objekt-Explorer  
Wenn eine Verbindung mit einem Server herstellen, können Sie angeben, dass zusätzliche Verbindungsinformationen in der **Verbindung mit Server herstellen** im Dialogfeld. Die **Verbindung mit Server herstellen** im Dialogfeld werden die zuletzt verwendeten Einstellungen beibehalten und neue Verbindungen, z. B. neuen Fenstern des Code-Editor werden diese Einstellungen verwenden.  
  
Zum Angeben optionaler Verbindungseinstellungen führen Sie die folgenden Schritte aus:  
  
1.  Klicken Sie auf **Verbinden** auf der Symbolleiste des Objekt-Explorer, und klicken Sie auf den Typ des Servers für die Verbindung. Das Dialogfeld **Verbindung mit Server herstellen** wird angezeigt.  
  
2.  In der **Servername** Geben Sie den Namen Ihrer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Instanz.  
  
3.  Klicken Sie auf **Optionen**. Die **Verbindung mit Server herstellen** im Dialogfeld werden weitere Optionen angezeigt.  
  
4.  Klicken Sie auf die **Verbindungseigenschaften** Registerkarte zusätzlichen Einstellungen konfigurieren. Die verfügbaren Einstellungen variieren abhängig vom Servertyp. Die folgenden Einstellungen sind für [!INCLUDE[ssDE](../content/includes/ssDE_md.md)] verfügbar.  
  
    |Einstellung|Beschreibung|  
    |-----------|---------------|  
    |**Verbindung mit Datenbank herstellen**|Treffen Sie eine Auswahl aus den verfügbaren Datenbanken auf dem Server. In dieser Liste werden nur Datenbanken angezeigt, für die Sie die Berechtigung zum Anzeigen haben.|  
    |**Netzwerkprotokoll**|Wählen Sie aus Shared Memory, TCP\/IP-Adresse oder Named Pipes.|  
    |**Netzwerkpaketgröße**|Konfigurieren Sie in Byte. Die Standardeinstellung ist 4096 Byte.|  
    |**Verbindungstimeout**|Konfigurieren Sie in Sekunden. Die Standardeinstellung ist 15 Sekunden.|  
    |**Ausführungstimeout**|Konfigurieren Sie in Sekunden. Die Standardeinstellung (0) weist darauf hin, dass es für die Ausführung kein Timeout gibt.|  
    |**Verbindung verschlüsseln**|Erzwingt die Verschlüsselung.|  
  
5.  Um den angegebenen Server zur Liste der registrierten Server hinzuzufügen, klicken Sie auf der **registrierte Server** Registerkarte, klicken Sie auf den Speicherort, in dem der neue Server angezeigt werden soll, und schließen Sie die Verbindung.  
  
> [!NOTE]  
> Mithilfe der Seite **Zusätzliche Verbindungsparameter** können Sie der Verbindungszeichenfolge weitere Verbindungsparameter hinzufügen. Weitere Informationen finden Sie unter [Verbindung mit Server & #40; Seite zusätzliche Verbindungsparameter & #41;](../content/Connect-to-Server--Additional-Connection-Parameters-Page-.md).  
  
