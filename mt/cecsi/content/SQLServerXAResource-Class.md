---
title: "SQLServerXAResource-Klasse"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: df957b79-536f-4db7-b6ac-3d59343559fc
caps.latest.revision: 10
caps.handback.revision: 9
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
# SQLServerXAResource-Klasse
  Stellt eine XAResource für die Verwaltung verteilter XA\-Transaktionen dar.  
  
 **Paket:** com.microsoft.sqlserver.jdbc  
  
 **Erweitert:** java.lang.Object  
  
 **Implementiert:** javax.transaction.xa.XAResource  
  
## Syntax  
  
```  
  
public class SQLServerXAResource  
```  
  
## Hinweise  
 XA\-Transaktionen werden in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] mithilfe von [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] mithilfe des Managers für verteilte Transaktionen \(DTC\) implementiert. Die SQLServerXAResource\-Klasse ruft eine erweiterte DLL\-Datei in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] mit der Bezeichnung "sqljdbc\_xa.dll" auf, die eine Verbindung mit DTC herstellt. Von SQLServerXAResource empfangene XA\-Aufrufe \(XA\_START, XA\_END, XA\_PREPARE usw.\) werden den entsprechenden Aufrufen der DTC\-Funktionen zugeordnet.  
  
## Siehe auch  
 [SQLServerXAResource-Elemente](../content/SQLServerXAResource-Members.md)   
 [API-Referenz für den JDBC-Treiber](../content/JDBC-Driver-API-Reference.md)  
  
  