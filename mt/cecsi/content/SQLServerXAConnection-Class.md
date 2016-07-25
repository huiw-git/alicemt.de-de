---
title: "SQLServerXAConnection-Klasse"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5ecb4bf1-b8d1-47cf-9cb1-7a18acc11ce2
caps.latest.revision: 8
caps.handback.revision: 7
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
# SQLServerXAConnection-Klasse
  Stellt JDBC\-Verbindungen dar, die an verteilten Transaktionen \(XA\-Transaktionen\) beteiligt sein können.  
  
 **Paket:** com.microsoft.sqlserver.jdbc  
  
 **Erweitert:** [SQLServerPooledConnection](../content/SQLServerPooledConnection-Class.md)  
  
 **Implementiert:** javax.sql.XAConnection  
  
## Syntax  
  
```  
  
public class SQLServerXAConnection  
```  
  
## Hinweise  
 Ein SQLServerXAConnection\-Objekt kann in einer verteilten Transaktion mittels eines [SQLServerXAResource](../content/SQLServerXAResource-Class.md)\-Objekts aufgelistet werden. Ein Transaktions\-Manager, der normalerweise Bestandteil eines Servers auf mittlerer Ebene ist, verwaltet ein SQLServerXAConnection\-Objekt über das SQLServerXAResource\-Objekt.  
  
> [!NOTE]  
>  Anwendungsprogrammierer verwenden diese Schnittstelle normalerweise nicht direkt. Sie wird in erster Linie von einem Transaktions\-Manager verwendet, der auf dem Server auf mittlerer Ebene arbeitet.  
  
## Siehe auch  
 [SQLServerXAConnection-Elemente](../content/SQLServerXAConnection-Members.md)   
 [API-Referenz für den JDBC-Treiber](../content/JDBC-Driver-API-Reference.md)  
  
  