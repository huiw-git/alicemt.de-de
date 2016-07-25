---
title: "PHP-Standarddatentypen"
ms.custom: na
ms.date: 06/16/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b66c301d-3d20-45b8-a112-225d8f01c0bd
caps.latest.revision: 40
caps.handback.revision: 39
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
# PHP-Standarddatentypen
Wenn vom Benutzer kein PHP-Datentyp angegeben wurde, werden die Daten beim Abrufen vom Server von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] in einen PHP-Standarddatentyp konvertiert.  
  
Wenn Daten mit dem Treiber PDO\_SQLSRV zurückgegeben werden, wird als Datentyp entweder „int“ oder „string“ verwendet.  
  
Im weiteren Verlauf dieses Themas werden die Standarddatentypen erläutert, die den SQLSRV-Treiber verwenden.  
  
Die folgende Tabelle enthält den SQL Server-Datentyp \(den Datentyp, der vom Server abgerufen wird\), den PHP-Standarddatentyp \(den Datentyp, in den Daten konvertiert werden\) und die Standardcodierung für Datenströme und Zeichenfolgen. Weitere Informationen dazu, wie Sie Datentypen beim Abrufen von Daten vom Server festlegen, finden Sie unter [How to: Specify PHP Data Types](../Topic/How%20to:%20Specify%20PHP%20Data%20Types.md).  
  
|SQL Server-Typ|PHP-Standardtyp|Standardcodierung|  
|-------------------|--------------------|--------------------|  
|bigint|String|8\-Bit-Zeichen<sup>1</sup>|  
|binary|Datenstrom<sup>2</sup>|Binär<sup>3</sup>|  
|bit|Integer|8\-Bit-Zeichen<sup>1</sup>|  
|char|String|8\-Bit-Zeichen<sup>1</sup>|  
|Datum<sup>8</sup>|Datetime|Nicht verfügbar|  
|datetime<sup>8</sup>|Datetime|Nicht verfügbar|  
|datetime2<sup>8</sup>|Datetime|Nicht verfügbar|  
|datetimeoffset<sup>8</sup>|Datetime|Nicht verfügbar|  
|decimal|String|8\-Bit-Zeichen<sup>1</sup>|  
|float|Float|8\-Bit-Zeichen<sup>1</sup>|  
|geography|Datenstrom|Binär<sup>3</sup>|  
|Geometrie|Datenstrom|Binär<sup>3</sup>|  
|Bild<sup>4</sup>|Datenstrom<sup>2</sup>|Binär<sup>3</sup>|  
|int|Integer|8\-Bit-Zeichen<sup>1</sup>|  
|money|String|8\-Bit-Zeichen<sup>1</sup>|  
|nchar|String|8\-Bit-Zeichen<sup>1</sup>|  
|numeric|String|8\-Bit-Zeichen<sup>1</sup>|  
|nvarchar|String|8\-Bit-Zeichen<sup>1</sup>|  
|nvarchar\(MAX\)|Datenstrom<sup>2</sup>|8\-Bit-Zeichen<sup>1</sup>|  
|ntext<sup>5</sup>|Datenstrom<sup>2</sup>|8\-Bit-Zeichen<sup>1</sup>|  
|real|Float|8\-Bit-Zeichen<sup>1</sup>|  
|smalldatetime|Datetime|8\-Bit-Zeichen<sup>1</sup>|  
|smallint|Integer|8\-Bit-Zeichen<sup>1</sup>|  
|smallmoney|String|8\-Bit-Zeichen<sup>1</sup>|  
|sql\_variant|String|8\-Bit-Zeichen<sup>1</sup>|  
|text<sup>6</sup>|Datenstrom<sup>2</sup>|8\-Bit-Zeichen<sup>1</sup>|  
|time<sup>8</sup>|Datetime|Nicht verfügbar|  
|timestamp|String|8\-Bit-Zeichen<sup>1</sup>|  
|tinyint|Integer|8\-Bit-Zeichen<sup>1</sup>|  
|UDT|Datenstrom<sup>2</sup>|Binär<sup>3</sup>|  
|uniqueidentifier|Zeichenfolge<sup>7</sup>|8\-Bit-Zeichen<sup>1</sup>|  
|varbinary|Datenstrom<sup>2</sup>|Binär<sup>3</sup>|  
|varbinary\(MAX\)|Datenstrom<sup>2</sup>|Binär<sup>3</sup>|  
|varchar|String|8\-Bit-Zeichen<sup>1</sup>|  
|varchar\(MAX\)|Datenstrom<sup>2</sup>|8\-Bit-Zeichen<sup>1</sup>|  
|variant|Nicht unterstützt|Nicht unterstützt|  
|xml|Datenstrom<sup>2</sup>|8\-Bit-Zeichen<sup>1</sup>|  
  
1.  Daten werden in\-8-Bit-Zeichen gemäß der Codepage des im System eingestellten Windows-Gebietsschemas zurückgegeben. Alle Multi\-Byte-Zeichen oder Zeichen, die nicht in dieser Codepage abgebildet sind, werden durch ein aus einem einzelnen Byte bestehendes Fragezeichen \(?\) dargestellt.  
  
2.  Wenn [sqlsrv_fetch_array](../content/sqlsrv_fetch_array.md) oder [sqlsrv_fetch_object](../content/sqlsrv_fetch_object.md) verwendet wird, um Daten abzurufen, die den PHP-Standardtyp Stream besitzen, werden die Daten als Zeichenfolge ausgegeben und genauso wie der Stream codiert. Wird z. B. einer der binären SQL Server-Datentypen über **sqlsrv\_fetch\_array** abgerufen, so wird als Standard-Rückgabetyp ein binärer String verwendet.  
  
3.  Die Daten werden als uncodierter und nicht übersetzter Strom aus unbearbeiteten Bytes vom Server zurückgegeben.  
  
4.  Dies ist ein veralteter Typ, der dem varbinary\(max\)-Typ zugeordnet ist.  
  
5.  Dies ist ein veralteter Typ, der dem nvarchar\(max\)-Typ zugeordnet ist.  
  
6.  Dies ist ein veralteter Typ, der dem varchar\(max\)-Typ zugeordnet ist.  
  
7.  Als „UNIQUEIDENTIFIER“ werden GUIDs bezeichnet, die den folgenden regulären Ausdruck aufweisen.  
  
    \[0\-9a\-fA\-F\]{8}\-\[0\-9a\-fA\-F\]{4}\-\[0\-9a\-fA\-f\]{4}\-\[0\-9a\-fA\-f\]{4}\-\[0\-9a\-fA\-F\]{12}  
  
8.  Daten des Typs „Datum“ und „Uhrzeit“ können als Zeichenfolgen abgerufen werden. Weitere Informationen finden Sie unter [So wird's gemacht: Datums- und Uhrzeittypen mittels des SQLSRV-Treibers als Zeichenfolgen abrufen](../Topic/How%20to:%20Retrieve%20Date%20and%20Time%20Type%20as%20Strings%20Using%20the%20SQLSRV%20Driver.md).  
  
## Weitere neue Datentypen und Funktionen in SQL Server 2008  
Datentypen, die in SQL Server 2008 neu sind und die außerhalb von Spalten \(z. B. Tabellenwertparameter\) vorhanden sind, werden in [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] nicht unterstützt. Die folgende Tabelle fasst die PHP-Unterstützung für die neuen Funktionen von SQL Server 2008 zusammen.  
  
|Funktion|PHP-Unterstützung|  
|-----------|---------------|  
|Tabellenwertparameter|Nein|  
|Spalten mit geringer Dichte|Teilweise|  
|NULL\-Bit-Komprimierung|ja|  
|Große benutzerdefinierte CLR-Typen \(UDTs\)|ja|  
|Dienstprinzipalname|Nein|  
|MERGE|ja|  
|FILESTREAM|Teilweise|  
  
Teilweise Unterstützung besagt, dass Sie den Spaltentyp nicht programmgesteuert abfragen können.  
  
## Siehe auch  
[Konstanten &#40;Microsoft-Treiber für PHP für SQL Server&#41;](../content/Constants--Microsoft-Drivers-for-PHP-for-SQL-Server-.md)  
[Konvertieren von Datentypen](../content/Converting-Data-Types.md)  
[PHP-Typen](http://go.microsoft.com/fwlink/?LinkId=109071)  
[Datentypen \(Transact\-SQL\)](http://go.microsoft.com/fwlink/?LinkId=109068)  
[sqlsrv_field_metadata](../content/sqlsrv_field_metadata.md)  
  
