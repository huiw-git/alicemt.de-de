---
title: "getPrecision-Methode (SQLServerParameterMetaData)"
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
  - SQLServerParameterMetaData.getPrecision
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 8bd79484-bab6-423b-978f-d7ec7132ebeb
caps.latest.revision: 8
caps.handback.revision: 8
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
# getPrecision-Methode (SQLServerParameterMetaData)
    
## getPrecision\-Methode \(SQLServerParameterMetaData\)  
 Ruft die Anzahl von Dezimalstellen des angegebenen Parameters ab.  
  
## Syntax  
  
```  
  
public int getPrecision(int param)  
```  
  
#### Parameter  
 *param*  
  
 Ein Wert vom Typ **int** zum Angeben des Parameterindexes.  
  
## Rückgabewert  
 Ein Wert vom Typ **int** , der die Genauigkeit des angegebenen Parameters angibt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getPrecision\-Methode wird von der getPrecision\-Methode in der java.sql.ParameterMetaData\-Schnittstelle angegeben.  
  
 Für Zahlentypen wird von dieser Methode die Anzahl von Dezimalstellen abgerufen. Für Zeichentypen wird die maximale Länge in Zeichen abgerufen. Für binäre Typen wird die maximale Länge in Bytes abgerufen. Ist die Dezimalstellenanzahl unbekannt, wird von der Methode "0" zurückgegeben.  
  
## Siehe auch  
 [SQLServerParameterMetaData-Methoden](../content/SQLServerParameterMetaData-Methods.md)   
 [SQLServerParameterMetaData-Elemente](../content/SQLServerParameterMetaData-Members.md)   
 [SQLServerParameterMetaData-Klasse](../content/SQLServerParameterMetaData-Class.md)  
  
  