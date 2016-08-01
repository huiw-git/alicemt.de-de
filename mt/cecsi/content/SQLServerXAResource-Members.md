---
title: "SQLServerXAResource-Elemente"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a069bf2c-1b70-4817-b084-a508445de799
caps.latest.revision: 12
caps.handback.revision: 11
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
# SQLServerXAResource-Elemente
    
## SQLServerXAResource\-Elemente  
 In den folgenden Tabellen sind die Elemente aufgeführt, die von der [SQLServerXAResource](../content/SQLServerXAResource-Class.md)\-Klasse verfügbar gemacht werden.  
  
### Konstruktoren  
 Keine  
  
### Felder  
  
|Name|Beschreibung|  
|----------|------------------|  
|[SSTRANSTIGHTLYCPLD](../content/SSTRANSTIGHTLYCPLD-Field--SQLServerXAResource-.md)|Hierdurch werden eng verkoppelte XA\-Transaktionen ermöglicht, die unterschiedliche XA\-Verzweigungstransaktions\-IDs \(XIDs\) aber dieselbe globale Transaktions\-ID \(GTRID\) aufweisen.|  
  
### Geerbte Felder  
  
|Klasse geerbt von:|Methoden|  
|------------------------|--------------|  
|javax.transaction.xa.XAResource|TMENDRSCAN, TMFAIL, TMJOIN, TMNOFLAGS, TMONEPHASE, TMRESUME, TMSTARTRSCAN, TMSUCCESS, TMSUSPEND, XA\_OK, XA\_RDONLY|  
  
### Methoden  
  
|Name|Beschreibung|  
|----------|------------------|  
|[commit](../content/commit-Method--SQLServerXAResource-.md)|Führt einen Commit für die globale Transaktion aus, die durch das angegebene Xid\-Objekt festgelegt wird.|  
|[end](../content/end-Method--SQLServerXAResource-.md)|Beendet die für einen Transaktionszweig durchgeführte Arbeit.|  
|[forget](../content/forget-Method--SQLServerXAResource-.md)|Teilt dem Ressourcen\-Manager mit, dass eine heuristisch abgeschlossene Transaktionsverzweigung ignoriert \(vergessen\) werden kann.|  
|[getTransactionTimeout](../content/getTransactionTimeout-Method--SQLServerXAResource-.md)|Ruft den aktuellen Transaktionstimeoutwert für das [SQLServerXAResource](../content/SQLServerXAResource-Class.md)\-Objekt ab.|  
|[isSameRM](../content/isSameRM-Method--SQLServerXAResource-.md)|Ermittelt, ob die vom Zielobjekt dargestellte Ressourcen\-Manager\-Instanz der vom XAResource\-Objekt dargestellten Ressourcen\-Manager\-Instanz entspricht.|  
|[prepare](../content/prepare-Method--SQLServerXAResource-.md)|Fordert an, dass der Ressourcen\-Manager für eine Transaktions\-Commit\-Aktion der vom vorhandenen Xid\-Objekt angegebenen Transaktion vorbereitet wird.|  
|[recover](../content/recover-Method--SQLServerXAResource-.md)|Ruft eine Liste vorbereiteter Transaktionszweige von einem Ressourcen\-Manager ab.|  
|[rollback](../content/rollback-Method--SQLServerXAResource-.md)|Fordert an, dass der Ressourcen\-Manager für die für den Transaktionszweig durchgeführte Arbeit ein Rollback ausführt.|  
|[setTransactionTimeout](../content/setTransactionTimeout-Method--SQLServerXAResource-.md)|Legt den aktuellen Transaktionstimeoutwert für das [SQLServerXAResource](../content/SQLServerXAResource-Class.md)\-Objekt fest.|  
|[start](../content/start-Method--SQLServerXAResource-.md)|Startet die Arbeit am Xid\-Objekt, das in einem Transaktionszweig angegeben ist.|  
  
### Geerbte Methoden  
  
|Klasse geerbt von:|Methoden|  
|------------------------|--------------|  
|java.lang.Object|clone, equals, finalize, getClass, hashCode, notify, notifyAll, toString, wait|  
  
## Siehe auch  
 [SQLServerXAResource-Klasse](../content/SQLServerXAResource-Class.md)  
  
  