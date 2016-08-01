---
title: "Internationale Funktionen des JDBC-Treibers"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bbb74a1d-9278-401f-9530-7b5f45aa79de
caps.latest.revision: 40
caps.handback.revision: 38
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
# Internationale Funktionen des JDBC-Treibers
  Der [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] bietet folgende Internationalisierungsfunktionen:  
  
-   Unterstützung einer vollständigen Lokalisierung in den gleichen Sprachen wie [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]  
  
-   Unterstützung für die Javasprachkonvertierungen für vertrauliche Gebietsschema [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Daten  
  
-   Betriebssystemunabhängige Unterstützung internationaler Sprachen  
  
-   Unterstützung für internationale Domänennamen \(beginnend mit Microsoft JDBC\-Treiber 6.0 für SQL Server\)  
  
## Verarbeitung von Zeichendaten  
 Zeichendaten in Java werden standardmäßig als Unicode\-Daten verarbeitet; das Java**String**\-Objekt String stellt Unicode\-Zeichendaten dar. Die einzige Ausnahme dieser Regel im JDBC\-Treiber bilden die Abruf\- und Festlegungsmethoden für ASCII\-Datenströme. Dabei handelt es sich um Sonderfälle, da Bytedatenströme mit der impliziten Voraussetzung einer einzelnen bekannten Codepage \(ASCII\) verwendet werden.  
  
 Darüber hinaus umfasst der JDBC\-Treiber die **sendStringParametersAsUnicode**\-Verbindungszeichenfolgeeigenschaft. Mit dieser Eigenschaft kann angegeben werden, dass die vorbereiteten Parameter für Zeichendaten anstatt in Unicode in ASCII oder als Multibyte\-Zeichensatz \(MBCS\) gesendet werden. Weitere Informationen zum Angeben der **sendStringParametersAsUnicode** Verbindungszeichenfolge finden Sie unter [Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md).  
  
### Konvertierung eingehender Daten  
 Unicode\-Textdaten vom Server brauchen nicht konvertiert zu werden. Sie werden direkt als Unicode\-Daten übergeben. Nicht\-Unicode\-Daten vom Server werden von der Codepage für die Daten auf Datenbank\- oder Spaltenebene in Unicode konvertiert. Der JDBC\-Treiber verwendet die JVM\-Konvertierungsroutinen \(Java Virtual Machine\) für diese Konvertierungen. Diese Konvertierungen werden in allen Abrufmethoden für typisierte Zeichenfolge\- und Zeichendatenströme ausgeführt.  
  
 Wenn die JVM nicht die richtige Codepage für die Daten aus der Datenbank unterstützt, löst der JDBC\-Treiber die Ausnahme „Codepage XXX wird von der Java\-Umgebung nicht unterstützt.“ aus. Zum Beheben dieses Problems sollten Sie die vollständige Unterstützung für internationale Zeichensätze installieren, die für diese JVM erforderlich ist. Ein Beispiel finden Sie auf der Sun Microsystems\-Website in der Dokumentation zu unterstützten Codierungen.  
  
### Konvertierung ausgehender Daten  
 Zeichendaten vom Treiber zum Server können als ASCII oder Unicode übertragen werden. Beispielsweise senden die neuen JDBC 4.0\-Methoden für nationale Zeichensätze wie setNString, setNCharacterStream und setNClob der [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\-Klasse und der [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Klasse ihre Parameterwerte immer im Unicode\-Format an den Server.  
  
 Die API\-Methoden für nicht nationale Zeichensätze wie setString, setCharacterStream und setClob der [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\-Klasse und der [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Klasse senden ihre Parameterwerte hingegen nur dann im Unicode\-Format an den Server, wenn die **sendStringParametersAsUnicode**\-Eigenschaft auf „true“ \(der Standardwert\) festgelegt ist.  
  
## Nicht\-Unicode\-Parameter  
 Um bei Verwendung der Typen von Nicht\-Unicode\-Parametern **CHAR**, **VARCHAR** und **LONGVARCHAR** eine optimale Leistung zu erhalten, legen Sie die **sendStringParametersAsUnicode**\-Verbindungszeichenfolgeneigenschaft auf „false“ fest und verwenden die Methoden für nicht nationale Zeichensätze.  
  
## Formatierungsprobleme  
 Bei Datums\-, Uhrzeit\- und Währungsangaben erfolgt die gesamte Formatierung mit lokalisierten Daten mit dem Locale\-Objekt und den verschiedenen Formatierungsmethoden für **Date**, **Calendar** und **Number**\-Datentypen auf Java\-Ebene. In den seltenen Fällen, in denen der JDBC\-Treiber gebietsschemasensitive Daten in einem lokalisierten Format übergeben muss, wird die entsprechende Formatierungsmethode mit dem JVM\-Standardgebietsschema verwendet.  
  
## Unterstützung der Sortierung  
 JDBC Driver 3.0 unterstützt alle Sortierungen, die von [!INCLUDE[ssVersion2000](../content/includes/ssVersion2000_md.md)], [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] und den neuen Sortierungen oder neuen Versionen der Windows\-Sortierungsnamen, die in [!INCLUDE[ssKatmai](../content/includes/ssKatmai_md.md)] eingeführt wurden, unterstützt werden.  
  
 Weitere Informationen zu Sortierungen finden Sie unter [Sortierung und Unicode\-Unterstützung](http://go.microsoft.com/fwlink/?LinkId=131366) und [Name der Windows\-Sortierreihenfolge \(Transact\-SQL\)](http://go.microsoft.com/fwlink/?LinkId=131367) in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation.  
  
## Verwendung internationaler Domänennamen \(IDN\)  
 Der JDBC\-Treiber 6.0 \(Vorschau\) für SQL Server unterstützt die Verwendung internationaler Domänennamen \(IDNs\) und kann bei Bedarf während einer Verbindung einen Unicode\-ServerName in ASCII\-kompatible Codierung \(Punycode\) konvertieren.  Wenn die IDNs im Domain Name System \(DNS\) als ASCII\-Zeichenfolgen im Punycode\-Format \(angegeben durch RFC 3490\) gespeichert sind, aktivieren Sie die Konvertierung der Unicode\-ServerName, indem Sie die ServerNameAsACE\-Eigenschaft auf „true“ setzen.  Wenn der DNS\-Dienst für die Verwendung von Unicode\-Zeichen konfiguriert ist, setzen Sie die ServerNameAsACE\-Eigenschaft auf „false“ \(Standard\).  Mit älteren Versionen des JDBC\-Treibers lässt sich der ServerName in Punycode umwandeln, indem die [Java’s IDN.toASCII](http://docs.oracle.com/javase/8/docs/api/java/net/IDN.html)\-Methode vor dem Festlegen dieser Verbindungseigenschaft angewendet wird.  
  
> [!NOTE]  
>  Der Großteil der für Windows\-Plattformen geschriebenen Konfliktlösersoftware basiert auf den Internet\-DSN\-Standards und verwendet aus diesem Grund mit hoher Wahrscheinlichkeit das Punycode\-Format für IDN. Ein Windows\-basierter DNS\-Server in einem privaten Netzwerk kann hingegen so konfiguriert werden, dass die Verwendung von UTF\-8\-Zeichen auf Serverbasis möglich ist.  Weitere Informationen finden Sie unter [Unterstützung von Unicode\-Zeichen](https://technet.microsoft.com/en-us/library/cc738403(v=ws.10).aspx).  
  
## Siehe auch  
 [Übersicht über den JDBC-Treiber](../content/Overview-of-the-JDBC-Driver.md)  
  
  