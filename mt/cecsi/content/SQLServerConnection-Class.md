---
title: "SQLServerConnection-Klasse"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 937292a6-1525-423e-a2b2-a18fd34c2893
caps.latest.revision: 17
caps.handback.revision: 16
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
# SQLServerConnection-Klasse
  Stellt eine JDBC\-Verbindung mit einer [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank dar.  
  
 **Paket:** com.microsoft.sqlserver.jdbc  
  
 **Implementiert:** [ISQLServerConnection](../content/ISQLServerConnection-Interface.md), java.io.Serializable  
  
## Syntax  
  
```  
  
public class SQLServerConnection  
```  
  
## Hinweise  
 SQLServerConnection unterstützt JDBC\-Verbindungspooling und kann entweder eine physische JDBC\-Verbindung oder eine logische JDBC\-Verbindung sein.SQLServerConnection verwaltet die Transaktionssteuerung für alle Anweisungen, die aus ihr erstellt wurden, und kann an verteilten XA\-Transaktionen teilnehmen, die über einen XAResource\-Adapter verwaltet werden.  
  
 SQLServerConnection verwaltet einen Pool vorbereiteter Anweisungshandles. Vorbereitete Anweisungen werden einmal vorbereitet und werden normalerweise mehrere Male mit unterschiedlichen Parameterdatenwerten ausgeführt. Vorbereitete Anweisungen werden ebenfalls über logische \(als Poolverbindung verwendete\) Verbindungsgrenzen hinweg beibehalten.  
  
> [!NOTE]  
>  SQLServerConnection ist nicht threadsicher. Mehrere aus einer einzelnen Verbindung erstellte Anweisungen können simultan in parallelen Threads verarbeitet werden.  
  
 Diese Klasse unterstützt das Entpacken in die Klasse SQLServerConnection, die Schnittstelle  java.sql.connection und die Schnittstelle  ISQLServerConnection. Weitere Informationen finden Sie unter [Wrapper und Schnittstellen](../content/Wrappers-and-Interfaces.md).  
  
## Siehe auch  
 [SQLServerConnection-Elemente](../content/SQLServerConnection-Members.md)   
 [API-Referenz für den JDBC-Treiber](../content/JDBC-Driver-API-Reference.md)  
  
  