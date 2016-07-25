---
title: "setTrustServerCertificate-Methode (SQLServerDataSource)"
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
  - setTrustServerCertificate Method (SQLServerDataSource)
apilocation: 
  - setTrustServerCertificate Method (SQLServerDataSource)
apitype: Assembly
ms.assetid: 6c37b518-147e-4cd9-9eff-b48a3f5888c6
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
  - sv-se
  - zh-cn
  - zh-tw
---
# setTrustServerCertificate-Methode (SQLServerDataSource)
  Legt einen Wert vom Typ **Boolean** fest, mit dem angegeben wird, ob die trustServerCertificate\-Eigenschaft aktiviert ist.  
  
## Syntax  
  
```  
  
public void setTrustServerCertificate(boolean trustServerCertificate)  
```  
  
#### Parameter  
 *trustServerCertificate*  
  
 **true**, wenn dem Secure Sockets Layer \(SSL\)\-Zertifikat des Servers automatisch vertraut werden soll, sofern die Kommunikationsschicht mit SSL verschlüsselt ist. Andernfalls wird **false** verwendet.  
  
## Hinweise  
 Ist die trustServerCertificate\-Eigenschaft auf **true** festgelegt, wird dem SSL\-Zertifikat von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] automatisch vertraut, wenn die Kommunikationsschicht mit SSL verschlüsselt ist. Mit anderen Worten, das [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-SSL\-Zertifikat wird von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] nicht überprüft. Der Standardwert ist **false**.  
  
 Ist die trustServerCertificate\-Eigenschaft auf **false** festgelegt, wird das SSL\-Zertifikat des Servers von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] überprüft.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  