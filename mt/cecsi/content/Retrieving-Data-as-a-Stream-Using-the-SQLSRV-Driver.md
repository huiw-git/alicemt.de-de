---
title: "Abrufen von Daten als Stream mit dem SQLSRV-Treiber"
ms.custom: na
ms.date: 06/16/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 17dc9129-04cd-430c-b5b3-82824116425d
caps.latest.revision: 18
caps.handback.revision: 17
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
# Abrufen von Daten als Stream mit dem SQLSRV-Treiber
Das Abrufen von Daten als Stream ist nur im SQLSRV-Treiber von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] und nicht im PDO\_SQLSRV-Treiber verfügbar.  
  
Die [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] nutzen Streams zum Abrufen großer Datenmengen. Die Themen in diesem Abschnitt enthalten ausführliche Informationen zum Abrufen von Daten als Stream.  
  
Die folgenden Schritte fassen zusammen, wie Daten als Stream abgerufen werden können:  
  
1.  Bereiten Sie eine Transact\-SQL-Abfrage mit [sqlsrv_query](../content/sqlsrv_query.md) oder der Kombination aus [sqlsrv_prepare](../content/sqlsrv_prepare.md)\/[sqlsrv_execute](../content/sqlsrv_execute.md) vor, und führen Sie sie aus.  
  
2.  Verwenden Sie [sqlsrv_fetch](../content/sqlsrv_fetch.md) , um in die nächste Zeile im Resultset zu wechseln.  
  
3.  Verwenden Sie [sqlsrv_get_field](../content/sqlsrv_get_field.md) , um ein Feld aus der Zeile abzurufen. Geben Sie durch die Angabe von **SQLSRV\_PHPTYPE\_STREAM\(<encoding>\)** als drittem Parameter im Funktionsaufruf an, dass die Daten als Stream abgerufen werden sollen. Diese Tabelle enthält die Konstanten, mit denen die Codierungen und ihre Beschreibungen angegeben werden:  
  
    |SQLSRV-Konstante|Beschreibung|  
    |-------------------|---------------|  
    |SQLSRV\_ENC\_BINARY|Die Daten werden als uncodierter und nicht übersetzter Strom aus unbearbeiteten Bytes vom Server zurückgegeben.|  
    |SQLSRV\_ENC\_CHAR|Daten werden in\-8-Bit-Zeichen gemäß der Codepage des im System eingestellten Windows-Gebietsschemas zurückgegeben. Alle Multi\-Byte-Zeichen oder Zeichen, die nicht in dieser Codepage abgebildet sind, werden durch ein aus einem einzelnen Byte bestehendes Fragezeichen \(?\) ersetzt.|  
  
> [!NOTE]  
> Einige Datentypen werden standardmäßig als Stream zurückgegeben. Weitere Informationen finden Sie unter [Default PHP Data Types](../content/Default-PHP-Data-Types.md).  
  
## In diesem Abschnitt  
  
|Thema|Beschreibung|  
|---------|---------------|  
|[Datentypen mit Stream-Unterstützung, die den SQLSRV-Treiber nutzen](../content/Data-Types-with-Stream-Support-Using-the-SQLSRV-Driver.md)|Listet die SQL Server-Datentypen auf, die als Streams abgerufen werden können.|  
|[Vorgehensweise: Abrufen von Zeichendaten als Stream mit dem SQLSRV-Treiber](../Topic/How%20to:%20Retrieve%20Character%20Data%20as%20a%20Stream%20Using%20the%20SQLSRV%20Driver.md)|Veranschaulicht, wie Zeichendaten als Stream abgerufen werden können.|  
|[Vorgehensweise: Abrufen von Binärdaten als Stream mithilfe des SQLSRV-Treibers](../Topic/How%20to:%20Retrieve%20Binary%20Data%20as%20a%20Stream%20Using%20the%20SQLSRV%20Driver.md)|Veranschaulicht, wie Binärdaten als Stream abgerufen werden können.|  
  
## Siehe auch  
[Abrufen von Daten](../content/Retrieving-Data.md)  
[Konstanten &#40;Microsoft-Treiber für PHP für SQL Server&#41;](../content/Constants--Microsoft-Drivers-for-PHP-for-SQL-Server-.md)  
  
