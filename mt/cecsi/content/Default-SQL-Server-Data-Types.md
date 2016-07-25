---
title: "SQL Server-Standarddatentypen"
ms.custom: na
ms.date: 06/16/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 65c7c211-96d3-4e65-a1de-1fe8d21348e7
caps.latest.revision: 20
caps.handback.revision: 19
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
  - zh-cn
  - zh-tw
---
# SQL Server-Standarddatentypen
Beim Senden von Daten an den Server konvertiert der [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] Daten aus seinem PHP-Datentyp in einen SQL Server-Datentyp, wenn vom Benutzer kein SQL Server-Datentyp angegeben wurde. Die folgende Tabelle enthält den PHP-Datentyp \(den Datentyp, der an den Server gesendet wird\) und den SQL Server-Standarddatentyp \(den Datentyp, in den die Daten konvertiert werden\). Details zum Angeben von Datentypen beim Senden von Daten an den Server finden Sie unter [Gewusst wie: Angeben von SQL Server-Datentypen, wenn der SQLSRV-Treiber verwendet wird](../Topic/How%20to:%20Specify%20SQL%20Server%20Data%20Types%20When%20Using%20the%20SQLSRV%20Driver.md).  
  
|PHP-Datentyp|SQL-Standardservertyp im SQLSRV-Treiber|SQL-Standardservertyp im PDO\_SQLSRV-Treiber|  
|-----------------|------------------------------------------------|-----------------------------------------------------|  
|NULL|varchar\(1\)|nicht unterstützt|  
|Boolean|bit|bit|  
|Integer|int|int|  
|Float|float\(24\)|nicht unterstützt|  
|Zeichenfolge \(Länge kleiner als 8000 Bytes\)|varchar\(<string length>\)|varchar\(<string length>\)|  
|Zeichenfolge \(Länge größer als 8000 Bytes\)|varchar\(max\)|varchar\(max\)|  
|Ressource|Wird nicht unterstützt.|Nicht unterstützt.|  
|Stream \(Codierung: nicht binär\)|varchar\(max\)|varchar\(max\)|  
|Stream \(Codierung: binär\)|varbinary|varbinary|  
|Array|Wird nicht unterstützt.|Wird nicht unterstützt.|  
|Objekt|Wird nicht unterstützt.|Nicht unterstützt.|  
|DatumUhrzeit \(1\)|datetime|Nicht unterstützt.|  
  
## Siehe auch  
[Konstanten &#40;Microsoft-Treiber für PHP für SQL Server&#41;](../content/Constants--Microsoft-Drivers-for-PHP-for-SQL-Server-.md)  
[Konvertieren von Datentypen](../content/Converting-Data-Types.md)  
[sqlsrv_field_metadata](../content/sqlsrv_field_metadata.md)  
[PHP-Typen](http://go.microsoft.com/fwlink/?LinkId=109071)  
[Datentypen \(Transact\-SQL\)](http://go.microsoft.com/fwlink/?LinkId=109068)  
  
