---
title: "setSendStringParametersAsUnicode-Methode (SQLServerDataSource)"
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
  - SQLServerDataSource.setSendStringParametersAsUnicode
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 49198d63-76cb-4843-8d04-e49b1fbb6916
caps.latest.revision: 17
caps.handback.revision: 16
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
# setSendStringParametersAsUnicode-Methode (SQLServerDataSource)
    
## setSendStringParametersAsUnicode\-Methode \(SQLServerDataSource\)  
 Legt einen Wert vom Typ **boolean** fest, mit dem angegeben wird, ob das Senden von Zeichenfolgenparametern an den Server im Unicode\-Format aktiviert ist.  
  
## Syntax  
  
```  
  
public void setSendStringParametersAsUnicode(boolean sendStringParametersAsUnicode)  
```  
  
#### Parameter  
 *sendStringParametersAsUnicode*  
  
 **true**, wenn Zeichenfolgenparameter im Unicode\-Format an den Server gesendet werden. Andernfalls wird **false** verwendet.  
  
## Hinweise  
 Ist die sendStringParametersAsUnicode\-Eigenschaft auf **true** \(Standardeinstellung\) festgelegt, werden Zeichenfolgenparameter im Unicode\-Format an den Server gesendet. Ist die sendStringParametersAsUnicode\-Eigenschaft auf **false** festgelegt, werden Zeichenfolgenparameter nicht im Unicode\-Format, sondern im ASCII\-\/MBCS\-Format an den Server gesendet. Ist die sendStringParametersAsUnicode\-Eigenschaft nicht festgelegt, wird von [getSendStringParametersAsUnicode](../content/getSendStringParametersAsUnicode-Method--SQLServerDataSource-.md) der Standardwert **true** zurückgegeben.  
  
 Weitere Informationen zur sendStringParametersAsUnicode\-Verbindungseigenschaft finden Sie unter [Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md).  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  