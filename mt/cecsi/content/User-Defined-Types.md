---
title: "Benutzerdefinierte Typen"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 19a71b27-b788-43a3-a76d-fe3001a6f016
caps.latest.revision: 9
caps.handback.revision: 8
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
  - sv-se
  - zh-cn
  - zh-tw
---
# Benutzerdefinierte Typen
  Benutzerdefinierte Typen \(UDTs\) wurden in [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] vorgestellt. Mit ihnen können Entwickler das Skalartypsystem durch das Speichern von CLR \(Common Language Runtime\)\-Objekten in einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank erweitern. UDTs können mehrere Elemente enthalten und Verhalten aufweisen, die sich von den herkömmlichen Aliasdatentypen unterscheiden, die aus einem einzigen [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Systemdatentyp bestehen. Vorher waren UDTs auf eine Dateigröße von maximal 8 Kilobyte beschränkt. In [!INCLUDE[ssKatmai](../content/includes/ssKatmai_md.md)] werden jetzt UDTs über 64 Kilobyte unterstützt. Ab Version 3.0 unterstützt JDBC Driver beim Festlegen des UserDefined\-Formats auch UDTs, die größer als 64 KB sind.  
  
 UDTs mit genau oder weniger als 8.000 Byte verhalten sich also genau wie bisher. Größere UDTs werden aber unterstützt und zeigen ihre Größe als "unbegrenzt" an.  
  
## Siehe auch  
 [Grundlegendes zu den Datentypen in JDBC Driver](../content/Understanding-the-JDBC-Driver-Data-Types.md)  
  
  