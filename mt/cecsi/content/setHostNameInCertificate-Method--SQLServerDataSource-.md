---
title: "setHostNameInCertificate-Methode (SQLServerDataSource)"
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
  - setHostNameInCertificate Method (SQLServerDataSource)
apilocation: 
  - setHostNameInCertificate Method (SQLServerDataSource)
apitype: Assembly
ms.assetid: 2bcf4f2e-a103-4374-abc4-ffad4ce8e3c0
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
# setHostNameInCertificate-Methode (SQLServerDataSource)
  Legt den Hostnamen fest, der bei der Überprüfung des Secure Sockets Layer \(SSL\)\-Zertifikats von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verwendet werden soll.  
  
## Syntax  
  
```  
  
public void setHostNameInCertificate(java.lang.String hostNameInCertificate)  
```  
  
#### Parameter  
 *hostNameInCertificate*  
  
 Ein **String** mit dem Hostnamen.  
  
## Hinweise  
 Der hostNameInCertificate\-Wert dient zum Überprüfen des SSL\-Zertifikats von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)], wenn die Kommunikationsschicht mithilfe von SSL verschlüsselt wird. Der Standardwert ist NULL.  
  
 Ist die hostNameInCertificate\-Eigenschaft auf NULL festgelegt oder nicht angegeben, wird das SSL\-Zertifikat von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] durch [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] anhand der serverName\-Eigenschaft überprüft. Ist die hostNameInCertificate\-Eigenschaft auf eine Zeichenfolge oder auf eine leere Zeichenfolge festgelegt, wird das SSL\-Zertifikat des Servers anhand dieses Werts überprüft.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  