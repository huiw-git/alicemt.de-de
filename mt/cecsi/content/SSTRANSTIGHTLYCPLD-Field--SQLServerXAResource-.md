---
title: "SSTRANSTIGHTLYCPLD-Feld (SQLServerXAResource)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SSTRANSTIGHTLYCPLD Field (SQLServerXAResource)
apilocation: 
  - SSTRANSTIGHTLYCPLD Field (SQLServerXAResource)
apitype: Assembly
ms.assetid: 379857c3-9de1-4964-8782-32df317cbfbb
caps.latest.revision: 15
caps.handback.revision: 14
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
# SSTRANSTIGHTLYCPLD-Feld (SQLServerXAResource)
    
## SSTRANSTIGHTLYCPLD\-Feld \(SQLServerXAResource\)  
 Hierdurch werden eng verkoppelte XA\-Transaktionen ermöglicht, die unterschiedliche XA\-Verzweigungstransaktions\-IDs \(XIDs\) aber dieselbe globale Transaktions\-ID \(GTRID\) aufweisen.  
  
## Syntax  
  
```  
  
public static final int SSTRANSTIGHTLYCPLD  
```  
  
### Feldwert  
 Ein Wert vom Typ **int**  \(32768\).  
  
## Hinweise  
 Jede Transaktion wird anhand einer XA\-Verzweigungstransaktions\-ID \(XID\) und einer globalen Transaktions\-ID \(GTRID\) identifiziert. Damit von den Anwendungen eng verkoppelte XA\-Transaktionen mit unterschiedlichen XIDs aber den gleichen GTRIDs verwendet werden können, muss [SSTRANSTIGHTLYCPLD](../content/SSTRANSTIGHTLYCPLD-Field--SQLServerXAResource-.md) für den flags\-Parameter der XAResource.start\-Methode festgelegt werden. Weitere Informationen zum Verwenden dieses Flags finden Sie unter [Grundlegendes zu XA-Transaktionen](../content/Understanding-XA-Transactions.md).  
  
## Siehe auch  
 [SQLServerXAResource-Felder](../content/SQLServerXAResource-Fields.md)   
 [SQLServerXAResource-Elemente](../content/SQLServerXAResource-Members.md)   
 [SQLServerXAResource-Klasse](../content/SQLServerXAResource-Class.md)  
  
  