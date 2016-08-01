---
title: "getBinaryStream-Methode (java.lang.String)"
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
  - SQLServerResultSet.getBinaryStream (java.lang.String)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 149609b5-a6de-4e23-a440-7061775d0899
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
# getBinaryStream-Methode (java.lang.String)
    
## getBinaryStream\-Methode \(java.lang.String\)  
 Ruft den Wert des angegebenen Spaltennamens in der aktuellen Zeile dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts als Binärdatenstrom nicht interpretierter Bytes ab.  
  
## Syntax  
  
```  
  
public java.io.InputStream getBinaryStream(java.lang.String columnName)  
```  
  
#### Parameter  
 *columnName*  
  
 Ein **String** mit dem Spaltennamen.  
  
## Rückgabewert  
 Ein InputStream\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getBinaryStream\-Methode wird von der getBinaryStream\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Diese Methode kann nur mit folgenden [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentypen verwendet werden: binary, varbinary, varbinary\(max\) und image. Bei Verwendung dieser Methode mit anderen Datentypen wird eine Ausnahme ausgelöst.  
  
 Nachdem der Wert von der Methode als Datenstrom empfangen wurde, kann der Wert in Ausschnitten aus dem Strom gelesen werden. Diese Methode ist besonders zum Abrufen umfangreicher LONGVARBINARY\-Werte geeignet.  
  
> [!NOTE]  
>  Alle Daten im zurückgegebenen Datenstrom müssen vor dem Abrufen des Werts aus einer anderen Spalte gelesen werden. Der nächste Aufruf einer Getter\-Methode schließt den Datenstrom implizit. Ein Datenstrom kann ebenfalls Null zurückgeben, wenn die InputStream.available\-Methode aufgerufen wird, egal ob Daten verfügbar sind oder nicht.  
  
## Siehe auch  
 [getBinaryStream-Methode &#40;ISQLServerResultSet&#41;](../content/getBinaryStream-Method--SQLServerResultSet-.md)   
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  