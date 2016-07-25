---
title: "H&#228;ufig gestellte Fragen (FAQ)"
ms.custom: na
ms.date: 06/09/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 65bfd6d2-c83d-4528-a5e1-a85b125a4f4a
caps.latest.revision: 6
caps.handback.revision: 2
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
# H&#228;ufig gestellte Fragen (FAQ)
Im Folgenden finden Sie Antworten auf Fragen zum ODBC\-Treiber für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] unter Linux.  
  
## Häufig gestellte Fragen  
Wie funktionieren die vorhandenen ODBC\-Anwendungen unter Linux mit dem Treiber?  
Sie sollten in der Lage sein, die ODBC\-Anwendungen, die Sie unter Linux mit anderen Treibern kompiliert und ausgeführt haben, zu kompilieren und auszuführen.  
  
Welche Funktionen von [!INCLUDE[ssSQL11](../content/includes/ssSQL11_md.md)] werden von dieser Version des Treibers unterstützt?  
Der ODBC\-Treiber unter Linux unterstützt alle Server\-Funktionen in [!INCLUDE[ssSQL11](../content/includes/ssSQL11_md.md)] außer LocalDB. Weitere Informationen zu [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-unterstützten Funktionen finden Sie unter [Programmierrichtlinien](../content/Programming-Guidelines.md).  
  
Unterstützt der Treiber die Kerberos\-Authentifizierung?  
Ja, weitere Informationen hierzu finden Sie unter [Nutzung der Integrierten Authentifizierung](../content/Using-Integrated-Authentication.md).  
  
Welche Unicode\-Codierung sollte eine Anwendung verwenden?  
UTF\-8 für SQL\_CHAR\-Daten und UTF\-16 für SQL\_WCHAR\-Daten.  
  
Gibt es ODBC\-Beispiele, die ich herunterladen und mit dem Treiber laufen lassen kann, um damit zu experimentieren oder sie auszuwerten?  
Ein Beispiel hierzu finden Sie unter [Vorhandene MSDN C\+\+ ODBC\-Beispiele für die ODBC\-Treiber unter Linux](http://blogs.msdn.com/b/sqlblog/archive/2012/01/26/use-existing-msdn-c-odbc-samples-for-microsoft-linux-odbc-driver.aspx).  
  
Ist der ODBC\-Treiber unter Linux Open Source?  
Nein, der ODBC\-Treiber unter Linux ist kein Open Source\-Produkt.  
  
Bedeutet der ODBC\-Treiber unter Linux, dass eine zukünftige Version von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] unter Linux laufen wird?  
Es gibt keine Pläne zur Unterstützung von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] unter Linux.  
  
Warum müssen Benutzer den UnixODBC\-Treiber\-Manager erstellen?  
Das UnixODBC\-Treiber\-Manager\-Paket, das im Lieferumfang der meisten Linux\-Distributionen enthalten ist, ist nicht kompatibel mit dieser Version des [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] ODBC\-Treibers für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]. Informationen zum Installieren von Version 2.3.0 oder 2.3.1 des UnixODBC\-Treiber\-Managers finden Sie unter [Installieren des Treiber-Managers](../content/Installing-the-Driver-Manager.md).  
  
Was sind die Unterschiede zwischen dem [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ODBC\-Treiber 1.0 for Linux und dem [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] ODBC\-Treiber 13 \(Preview\) oder 11 for [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]?  Ist es das gleiche Produkt?  
Der [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] ODBC\-Treiber 11 for [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ist der neue Name für den Treiber für Linux und Windows. Bei Verwendung des [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ODBC\-Treibers 1.0 for Linux, sollten Sie ein Upgrade auf die Version [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] ODBC\-Treiber 13 Version \(Preview\) oder 11 for [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] durchführen.  
  
