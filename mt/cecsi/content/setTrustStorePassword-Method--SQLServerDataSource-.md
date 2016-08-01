---
title: "setTrustStorePassword-Methode (SQLServerDataSource)"
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
  - setTrustStorePassword Method (SQLServerDataSource)
apilocation: 
  - setTrustStorePassword Method (SQLServerDataSource)
apitype: Assembly
ms.assetid: fa87cbde-71cc-4f21-bc07-f8ba2b6a0a3f
caps.latest.revision: 16
caps.handback.revision: 15
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
# setTrustStorePassword-Methode (SQLServerDataSource)
    
## setTrustStorePassword\-Methode \(SQLServerDataSource\)  
 Legt das Kennwort fest, das zum Überprüfen der Integrität der trustStore\-Daten verwendet wird.  
  
## Syntax  
  
```  
  
public void setTrustStorePassword(java.lang.String trustStorePassword)  
```  
  
#### Parameter  
 *trustStorePassword*  
  
 Ein **String** mit dem Kennwort, das zum Überprüfen der Integrität der trustStore\-Daten verwendet wird.  
  
## Hinweise  
 Die trustStorePassword\-Eigenschaft kann zusammen mit der trustStore\-Eigenschaft angegeben werden, und deren Wert wird zum Prüfen der Integrität der trustStore\-Datei verwendet.  
  
 Wenn die trustStore\-Eigenschaft festgelegt ist, die trustStorePassword\-Eigenschaft jedoch nicht festgelegt wurde, wird die Integrität von "trustStore" nicht überprüft.  
  
 Wenn die trustStore\-Eigenschaft und die trustStorePassword\-Eigenschaft nicht angegeben wurden, verwendet der Treiber die Java Virtual Machine \(JVM\)\-Systemeigenschaften "javax.net.ssl.trustStore" und "javax.net.ssl.trustStorePassword". Wenn die Systemeigenschaft "javax.net.ssl.trustStorePassword" nicht angegeben wird, wird die Integrität von **trustStore** nicht überprüft.  
  
 Wenn die trustStore\-Eigenschaft nicht festgelegt ist, die trustStorePassword\-Eigenschaft jedoch festgelegt ist, verwendet der JDBC\-Treiber die von "javax.net.ssl.trustStore" angegebene Datei als Vertrauensspeicher, und die Integrität des Vertrauensspeichers wird mithilfe des angegebenen **trustStorePassword** überprüft. Dies kann erforderlich sein, wenn in der Clientanwendung das Kennwort nicht in der JVM\-Systemeigenschaft gespeichert werden soll.  
  
 Weitere Informationen finden Sie unter [Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md).  
  
 Ab JDBC Driver 3.0 muss SQLServerDataSource.setTrustStorePassword vor dem Herstellen der Verbindung aufgerufen werden, wenn Sie SQLServerDataSource.setTrustStorePassword vor dem Binden der Datenquelleneigenschaften festlegen. Weitere Informationen finden Sie unter [SQLServerDataSource.getReference](../content/getReference-Method--SQLServerDataSource-.md).  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  