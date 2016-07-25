---
title: "Arbeiten mit Anweisungen und Resultsets"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cc917534-f5f8-4844-87c8-597c48b4e06d
caps.latest.revision: 13
caps.handback.revision: 12
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
# Arbeiten mit Anweisungen und Resultsets
  Wenn Sie die [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\- und Statement\-Objekte von ResultSet verwenden, gibt es mehrere Möglichkeiten, um die Leistung und Zuverlässigkeit der Anwendungen zu verbessern.  
  
## Verwenden des geeigneten Statement\-Objekts  
 Wenn Sie eines der Statement\-Objekte des JDBC\-Treibers verwenden, z. B. ein [SQLServerStatement](../content/SQLServerStatement-Class.md)\-, ein [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\- oder ein [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Objekt, müssen Sie das für die Aufgabe geeignete Objekt verwenden.  
  
-   Wenn keine OUT\-Parameter vorhanden sind, müssen Sie das SQLServerCallableStatement\-Objekt nicht verwenden. Sie können stattdessen das SQLServerStatement\-Objekt oder das SQLServerPreparedStatement\-Objekt verwenden.  
  
-   Wenn Sie die Anweisung nicht mehrmals ausführen möchten oder keine IN\- oder OUT\-Parameter verwenden, müssen Sie das SQLServerCallableStatement\-Objekt oder das SQLServerPreparedStatement\-Objekt nicht verwenden. Verwenden Sie stattdessen das SQLServerStatement\-Objekt.  
  
## Verwenden der geeigneten Parallelität für ResultSet\-Objekte  
 Verwenden Sie beim Erstellen von Anweisungen, die Resultsets erzeugen, keine aktualisierbare Parallelität, wenn die Ergebnisse nicht aktualisiert werden sollen. Das Standardmodell mit schreibgeschütztem Vorwärtscursor weist beim Lesen von kleinen Resultsets die höchste Leistung auf.  
  
## Einschränken der Größe von Resultsets  
 Sie sollten die [setMaxRows](../content/setMaxRows-Method--SQLServerStatement-.md)\-Methode \(bzw. die SQL\-Syntax SET ROWCOUNT oder SELECT TOP N\) verwenden, um die Anzahl der von möglicherweise umfangreichen Resultsets zurückgegebenen Zeilen zu beschränken. Bei der Verarbeitung von umfangreichen Resultsets sollten Sie eine adaptive Antwortpufferung verwenden, indem Sie die Verbindungszeichenfolgeneigenschaft "responseBuffering" auf "adaptive" \(den Standardmodus\) festlegen. So kann die Anwendung große Resultsets verarbeiten, ohne serverseitige Cursor verwenden zu müssen, und die Anwendungsspeicherauslastung minimieren. Weitere Informationen finden Sie unter [Verwenden der adaptiven Pufferung](../content/Using-Adaptive-Buffering.md).  
  
## Verwenden der geeigneten Fetchgröße  
 Bei schreibgeschützten Servercursorn muss ein Kompromiss zwischen den Roundtrips zum Server und dem im Treiber verwendeten Speicher gefunden werden. Bei aktualisierbaren Servercursorn beeinflusst außerdem die Abrufgröße die Sensitivität des Resultsets gegenüber Änderungen und die Parallelität des Servers. Updates von Zeilen im Fetchpuffer werden erst dann sichtbar, wenn explizit eine [refreshRow](../content/refreshRow-Method--SQLServerResultSet-.md)\-Methode ausgegeben wird oder der Cursor den Fetchpuffer verlässt. Große Fetchpuffer weisen eine höhere Leistung \(weniger Serverroundtrips\) aber eine geringere Sensitivität gegenüber Änderungen auf und verringern die Parallelität des Servers, wenn CONCUR\_SS\_SCROLL\_LOCKS \(1009\) verwendet wird. Verwenden Sie die Abrufgröße "1", um die Sensitivität gegenüber Änderungen zu maximieren. Beachten Sie jedoch, dass dabei für jede abgerufene Zeile ein Roundtrip zum Server erforderlich ist.  
  
## Verwenden von Datenströmen für umfangreiche IN\-Parameter  
 Verwenden Sie Datenströme oder BLOBs und CLOBs, die inkrementell gefüllt werden, um umfangreiche Spaltenwerte zu aktualisieren oder umfangreiche IN\-Parameter zu senden. Der JDBC\-Treiber sendet diese blockweise in mehreren Roundtrips an den Server, sodass Werte festgelegt und aktualisiert werden können, die größer sind als der verfügbare Speicher.  
  
## Siehe auch  
 [Verbessern von Leistung und Zuverlässigkeit mit dem JDBC-Treiber](../content/Improving-Performance-and-Reliability-with-the-JDBC-Driver.md)  
  
  