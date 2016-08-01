---
title: "getSendStringParametersAsUnicode-Methode (SQLServerDataSource)"
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
  - SQLServerDataSource.getSendStringParametersAsUnicode
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 3836d0ab-c3fb-41ff-bb89-10389594ae51
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
# getSendStringParametersAsUnicode-Methode (SQLServerDataSource)
    
## getSendStringParametersAsUnicode\-Methode \(SQLServerDataSource\)  
 Gibt einen Wert vom Typ **boolean** zurück, mit dem angegeben wird, ob das Senden von Zeichenfolgenparametern an den Server im Unicode\-Format aktiviert ist.  
  
## Syntax  
  
```  
  
public boolean getSendStringParametersAsUnicode()  
```  
  
## Rückgabewert  
 **true**, wenn Zeichenfolgenparameter im Unicode\-Format an den Server gesendet werden. Andernfalls wird **false** verwendet.  
  
## Hinweise  
 Ist die sendStringParametersAsUnicode\-Eigenschaft auf **true** \(Standardeinstellung\) festgelegt, werden Zeichenfolgenparameter im Unicode\-Format an den Server gesendet. Ist die sendStringParametersAsUnicode\-Eigenschaft auf **false** festgelegt, werden Zeichenfolgenparameter nicht im Unicode\-Format, sondern im ASCII\-\/MBCS\-Format an den Server gesendet. Ist die sendStringParametersAsUnicode\-Eigenschaft nicht festgelegt, wird von getSendStringParametersAsUnicode der Standardwert **true** zurückgegeben.  
  
 Weitere Informationen zur sendStringParametersAsUnicode\-Verbindungseigenschaft finden Sie unter [Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md).  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  