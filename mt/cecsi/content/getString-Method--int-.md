---
title: "getString-Methode (int)"
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
  - SQLServerCallableStatement.getString (int)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: f3fce8bf-8d6e-476f-aa6d-992daa79b899
caps.latest.revision: 10
caps.handback.revision: 9
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
# getString-Methode (int)
    
## getString\-Methode \(int\)  
 Ruft den Wert des angegebenen Parameters unter Berücksichtigung des Parameterindexes als **String** \-Objekt in der Programmiersprache Java ab.  
  
## Syntax  
  
```  
  
public java.lang.String getString(int index)  
```  
  
#### Parameter  
 *index*  
  
 Ein Wert vom Typ **int** zum Angeben des Parameterindexes.  
  
## Rückgabewert  
 Ein Wert vom Typ **String** .  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getString\-Methode wird von der getString\-Methode in der java.sql.CallableStatement\-Schnittstelle angegeben.  
  
 Alle Spalten in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] können als Zeichenfolge zurückgegeben werden. Es können also eine Zeichenfolgendarstellung aller zahlen\- und zeichenfolgenbasierten Typen und eine hexadezimale Zeichenfolgendarstellung binärer Spalten wie "binary", "varbinary", "varbinary\(max\)", "image", "timestamp" oder "uniqueidentifier" zurückgegeben werden.  
  
 Den Speicherort berücksichtigende Typen wie "money", "smallmoney", "datetime", "smalldatetime", "float", "real", "decimal" oder "numeric" geben für den zugrundeliegenden Wert des Typs das kanonische toString\(\)\-Format zurück.  
  
 Benutzerdefinierte Typen werden als hexadezimale Zeichenfolgenwerte zurückgegeben.  
  
## Siehe auch  
 [getString-Methode &#40;SQLServerCallableStatement&#41;](../content/getString-Method--SQLServerCallableStatement-.md)   
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [SQLServerCallableStatement-Klasse](../content/SQLServerCallableStatement-Class.md)  
  
  