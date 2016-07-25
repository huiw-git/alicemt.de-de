---
title: "getTrustServerCertificate-Methode (SQLServerDataSource)"
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
  - getTrustServerCertificate Method (SQLServerDataSource)
apilocation: 
  - getTrustServerCertificate Method (SQLServerDataSource)
apitype: Assembly
ms.assetid: e4f443cc-b5d7-4859-81df-836a8642ed07
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
# getTrustServerCertificate-Methode (SQLServerDataSource)
  Gibt einen Wert vom Typ **Boolean** zurück, mit dem angegeben wird, ob die trustServerCertificate\-Eigenschaft aktiviert ist.  
  
## Syntax  
  
```  
  
public boolean getTrustServerCertificate()  
```  
  
## Rückgabewert  
 **true**, wenn "trustServerCertificate" aktiviert ist. Andernfalls wird **false** verwendet.  
  
## Hinweise  
 Ist die trustServerCertificate\-Eigenschaft auf **true** festgelegt, wird dem SSL\-Zertifikat von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] automatisch vertraut, wenn die Kommunikationsschicht mit SSL \(Secure Sockets Layer\) verschlüsselt ist. Mit anderen Worten, das [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-SSL\-Zertifikat wird von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] nicht überprüft. Der Standardwert ist **false**.  
  
 Ist die trustServerCertificate\-Eigenschaft auf **false** festgelegt, wird das SSL\-Zertifikat des Servers von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] überprüft.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  