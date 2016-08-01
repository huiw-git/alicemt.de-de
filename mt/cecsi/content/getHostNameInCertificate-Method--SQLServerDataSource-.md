---
title: "getHostNameInCertificate-Methode (SQLServerDataSource)"
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
  - getHostNameInCertificate Method (SQLServerDataSource)
apilocation: 
  - getHostNameInCertificate Method (SQLServerDataSource)
apitype: Assembly
ms.assetid: 45ea04e2-9ea5-4171-9136-d09f8a95e128
caps.latest.revision: 11
caps.handback.revision: 10
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
# getHostNameInCertificate-Methode (SQLServerDataSource)
    
## getHostNameInCertificate\-Methode \(SQLServerDataSource\)  
 Gibt den Hostnamen zurück, der bei der Überprüfung des Secure Sockets Layer \(SSL\)\-Zertifikats von SQL Server verwendet wird.  
  
## Syntax  
  
```  
  
public java.lang.String getHostNameInCertificate()  
```  
  
## Rückgabewert  
 Ein **String** , der den Hostnamen oder – sofern kein Wert festgelegt ist – NULL enthält.  
  
## Hinweise  
 Der Hostname dient zum Überprüfen des SQL Server\-SSL\-Zertifikatwerts, wenn die Kommunikationsschicht mithilfe von SSL verschlüsselt wird.  
  
 Ist der Hostname nicht festgelegt, wird von der [getHostNameInCertificate](../content/getHostNameInCertificate-Method--SQLServerDataSource-.md)\-Methode der Standardwert \(NULL\) zurückgegeben.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  