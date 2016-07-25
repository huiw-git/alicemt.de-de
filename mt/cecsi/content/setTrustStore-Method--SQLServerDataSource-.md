---
title: "setTrustStore-Methode (SQLServerDataSource)"
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
  - setTrustStore Method (SQLServerDataSource)
apilocation: 
  - setTrustStore Method (SQLServerDataSource)
apitype: Assembly
ms.assetid: bab5485d-4547-426c-adbe-44e2b5702d1d
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
# setTrustStore-Methode (SQLServerDataSource)
  Legt den Pfad \(einschließlich Dateiname\) zur trustStore\-Zertifikatsdatei fest.  
  
## Syntax  
  
```  
  
public void setTrustStore(java.lang.String trustStore)  
```  
  
#### Parameter  
 *trustStore*  
  
 Ein Wert vom Typ **String** mit dem Pfad \(einschließlich des Dateinamens\) der trustStore\-Zertifikatsdatei.  
  
## Hinweise  
 Ist die trustStore\-Eigenschaft nicht angegeben oder auf NULL festgelegt, wird der zu verwendende Zertifikatspeicher von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] mithilfe der Suchregeln der Trust\-Manager\-Factory ermittelt. Die Vertrauenswürdigkeitsinformationen werden von der standardmäßigen SunX509\-TrustManagerFactory an folgenden Speicherorten und in der folgenden Reihenfolge gesucht:  
  
-   1. Eine von der Java Virtual Machine \(JVM\)\-Systemeigenschaft "javax.net.ssl.trustStore" angegebene Datei  
  
-   2. Datei "\<java\-home\>\/lib\/security\/jssecacerts"  
  
-   3. Datei "\<java\-home\>\/lib\/security\/cacerts"  
  
 Weitere Informationen finden Sie in der Dokumentation zur SunX509 TrustManager\-Schnittstelle auf der Website von Sun Microsystems.  
  
 Ist die trustStore\-Eigenschaft auf eine Zeichenfolge oder auf eine leere Zeichenfolge \(""\) festgelegt, wird die trustStore\-Datei anhand dieses Werts gesucht, um das SSL\-Zertifikat des Servers zu überprüfen.  
  
 Die trustStorePassword\-Eigenschaft kann zusammen mit der trustStore\-Eigenschaft angegeben werden, und deren Wert wird zum Öffnen der trustStore\-Datei verwendet. Weitere Informationen finden Sie unter [setTrustStorePassword](../content/setTrustStorePassword-Method--SQLServerDataSource-.md).  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  