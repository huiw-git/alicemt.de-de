---
title: "getEncrypt-Methode (SQLServerDataSource)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - getEncrypt Method (SQLServerDataSource)
apilocation: 
  - getEncrypt Method (SQLServerDataSource)
apitype: Assembly
ms.assetid: 1cdb12dd-6e6f-4bbd-8f5f-9e630f3ee2c9
caps.latest.revision: 19
caps.handback.revision: 18
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
# getEncrypt-Methode (SQLServerDataSource)
  Gibt einen Wert vom Typ **Boolean** zurück, mit dem angegeben wird, ob die encrypt\-Eigenschaft aktiviert ist.  
  
## Syntax  
  
```  
  
public boolean getEncypt()  
```  
  
## Rückgabewert  
 **true**, wenn die Verschlüsselung aktiviert ist. Andernfalls wird **false** verwendet.  
  
## Hinweise  
 Ist die encrypt\-Eigenschaft auf **true** festgelegt, wird von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] sichergestellt, dass [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] für alle zwischen Client und Server versendeten Daten die Secure Sockets Layer \(SSL\)\-Verschlüsselung verwendet, sofern auf dem Server ein Zertifikat installiert ist.  
  
 Ist die encrypt\-Eigenschaft nicht angegeben oder auf **false** festgelegt, wird vom Treiber die Unterstützung der SSL\-Verschlüsselung durch [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] nicht erzwungen. Wenn die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Instanz nicht für das Erzwingen der SSL\-Verschlüsselung konfiguriert ist, wird eine Verbindung ohne jegliche Verschlüsselung hergestellt. Falls die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Instanz für das Erzwingen der SSL\-Verschlüsselung konfiguriert ist, aktiviert [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] bei Ausführung auf einer ordnungsgemäß konfigurierten Java Virtual Machine \(JVM\) automatisch die SSL\-Verschlüsselung. Andernfalls wird die Verbindung getrennt, und der Treiber löst einen Fehler aus. Ist die Verschlüsselungseigenschaft nicht festgelegt, wird von der [getEncrypt](../content/getEncrypt-Method--SQLServerDataSource-.md)\-Methode der Standardwert **false** zurückgegeben.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  