---
title: "Verbindungspooling (Microsoft Drivers for PHP for SQL Server)"
ms.custom: na
ms.date: 06/28/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4d9a83d4-08de-43a1-975c-0a94005edc94
caps.latest.revision: 14
caps.handback.revision: 13
manager: jhubbard
translation.priority.ht: 
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
# Verbindungspooling (Microsoft Drivers for PHP for SQL Server)
Folgende wichtige Punkte sollten Sie für das Verbindungspooling in [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]beachten:  
  
-   [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] verwendet ODBC-Verbindungspooling.  
  
-   Standardmäßig ist die Verbindung aktiviert. Wenn Sie sich mit einem Server verbinden, versucht der Treiber zunächst, eine Poolverbindung zu verwenden bevor er eine neue erstellt. Falls im Pool keine äquivalente Verbindung gefunden wird, wird eine neue Verbindung erstellt und dem Pool hinzugefügt. Basierend auf einem Vergleich der Verbindungszeichenfolgen, ermittelt der Treiber  ob die Verbindungen äquivalent sind.  
  
-   Wenn eine Verbindung aus dem Pool verwendet wird, wird der Verbindungsstatus zurückgesetzt.   
  
-   Das Schließen der Verbindung gibt die Verbindung an den Pool zurück.  
  
Weitere Informationen zum Verbindungspooling finden Sie unter [Treibermanager-Verbindungspooling](http://go.microsoft.com/fwlink/?linkid=119622).  
  
## Verbindungsattribute  
Sie können den Treiber zwingen, eine neue Verbindung zu erstellen \(anstatt nach einer äquivalenten Verbindung im Verbindungspool zu suchen\), indem Sie den Wert des *ConnectionPooling*-Attributs in der Verbindungszeichenfolge auf **false** \(oder 0\) festlegen.  
  
Falls das *ConnectionPooling*-Attribut aus der Verbindungszeichenfolge weggelassen oder auf **true** \(oder 1\) festgelegt wird, erstellt der Treiber nur dann eine neue Verbindung, wenn es keine äquivalente Verbindung im Verbindungspool gibt.  
  
Weitere Informationen zu weiteren Verbindungsattributen finden Sie unter [Connection Options](../content/Connection-Options.md).  
  
## Siehe auch  
[Vorgehensweise: Herstellen einer Verbindung mithilfe der Windows-Authentifizierung](../Topic/How%20to:%20Connect%20Using%20Windows%20Authentication.md)  
[Vorgehensweise: Herstellen einer Verbindung mithilfe der SQL Server-Authentifizierung](../Topic/How%20to:%20Connect%20Using%20SQL%20Server%20Authentication.md)  
  
