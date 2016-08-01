---
title: "API-Referenz f&#252;r den JDBC-Treiber"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e4e1ae9d-18a6-41db-8bd2-9cf0eee4cccb
caps.latest.revision: 46
caps.handback.revision: 37
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
# API-Referenz f&#252;r den JDBC-Treiber
  Die von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] bereitgestellte API kann innerhalb von Java\-Programmiercode zum Herstellen einer Verbindung und Kommunizieren mit einer [!INCLUDE[msCoName](../content/includes/msCoName_md.md)][!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank verwendet werden.  
  
> [!NOTE]  
>  Konzeptionelle Informationen zur Verwendung des JDBC\-Treibers finden Sie unter [Übersicht über den JDBC-Treiber](../content/Overview-of-the-JDBC-Driver.md).  
  
> [!IMPORTANT]  
>  Verwenden Sie Microsoft JDBC Driver 4.2 für SQL Server, um JDBC 4.1\- und 4.2\-Kompatibilität zu unterstützen. Die vorhergehenden Versionen Microsoft JDBC Driver 4.1 und 4.0 unterstützen die in JDBC 4.1 und 4.2 eingeführten neuen Methoden nicht.  
>   
>  API\-Details zur JDBC 4.1\-Kompatibilität werden in diesem Abschnitt nicht erörtert. Siehe [JDBC 4.1-Kompatibilität für den JDBC-Treiber](../content/JDBC-4.1-Compliance-for-the-JDBC-Driver.md).  
>   
>  API\-Details zur JDBC 4.2\-Kompatibilität werden in diesem Abschnitt nicht erörtert. Siehe [JDBC 4.2-Kompatibilität für den JDBC-Treiber](../content/JDBC-4.2-Compliance-for-the-JDBC-Driver.md).  
>   
>  API\-Details zur Massenkopierfunktion, die in Microsoft JDBC Drivers 4.2 für SQL Server zur Verfügung steht, werden in diesem Abschnitt nicht erörtert.  Siehe [Verwenden von Massenkopieren mit dem JDBC Driver](../content/Using-Bulk-Copy-with-the-JDBC-Driver.md).  
>   
>  API\-Details für „Immer verschlüsselt“ , die ab dem Microsoft JDBC Driver 6.0 \(Vorschau\) für SQL Server verfügbar ist, werden in diesem Abschnitt nicht erörtert. Siehe [Verwenden von „Immer verschlüsselt“ mit dem JDBC-Treiber](../content/Using-Always-Encrypted-with-the-JDBC-Driver.md)  
>   
>  Die Microsoft JDBC\-Treiber 6.0 \(Vorschau\) und 4.2 unterstützen die Kompilierung mit JDK 5.0, 6.0, 7.0 und 8.0.  
>   
>  Der Microsoft JDBC\-Treiber 4.1 unterstützt die Kompilierung mit JDK 5.0, 6.0 und 7.0.  
>   
>  Der Microsoft JDBC\-Treiber 4.0 unterstützt die Kompilierung mit JDK 5.0 und 7.0.  
  
## Schnittstellen  
  
|Schnittstellenname|Beschreibung|  
|------------------------|------------------|  
|[ISQLServerCallableStatement-Schnittstelle](../content/ISQLServerCallableStatement-Interface.md)|Mit dieser Klasse kann der gespeicherte Prozedurname angegeben werden, der mit Eingabe\- und Ausgabeparametern aufgerufen wird.|  
|[ISQLServerConnection-Schnittstelle](../content/ISQLServerConnection-Interface.md)|Stellt eine JDBC\-Verbindung mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank dar.|  
|[SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)|Stellt eine Liste mit spezifischen Eigenschaften für das Herstellen einer Verbindung mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank unter Verwendung eines [ISQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekts dar.|  
|[ISQLServerPreparedStatement](../content/ISQLServerPreparedStatement-Interface.md)|Stellt die grundlegende Implementierung der JDBC\-Funktion für vorbereitete Anweisungen dar.|  
|[ISQLServerResultSet](../content/ISQLServerResultSet-Interface.md)|Stellt ein JDBC\-Resultset dar.|  
|[ISQLServerStatement](../content/ISQLServerStatement-Interface.md)|Stellt die grundlegende Implementierung der JDBC\-Anweisungsfunktion dar.|  
  
## Klassen  
  
|Klassenname|Beschreibung|  
|-----------------|------------------|  
|[DateTimeOffset](../content/DateTimeOffset-Class.md)|Stellt ein Objekt vom Typ „microsoft.sql.DateTimeOffset“ dar.|  
|[SQLServerBlob](../content/SQLServerBlob-Class.md)|Stellt ein BLOB \(Binary Large Object\) dar.|  
|[SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)|Stellt ein CLOB \(Character Large Binary Object\) dar.|  
|[SQLServerClob](../content/SQLServerClob-Class.md)|Stellt ein CLOB \(Character Large Binary Object\) dar|  
|[SQLServerConnection](../content/SQLServerConnection-Class.md)|Implementiert ISQLServerConnectopn.|  
|[SQLServerConnectionPoolDataSource](../content/SQLServerConnectionPoolDataSource-Class.md)|Stellt die physischen Datenbankverbindungen für Verbindungspool\-Manager dar.|  
|[SQLServerDatabaseMetaData](../content/SQLServerDatabaseMetaData-Class.md)|Stellt die Metadaten für die Datenbank dar.|  
|[SQLServerDataSource](../content/ISQLServerDataSource-Interface.md)|Stellt eine Liste mit spezifischen Eigenschaften für das Herstellen einer Verbindung mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank unter Verwendung eines [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekts dar.|  
|[SQLServerDataSourceObjectFactory](../content/SQLServerDataSourceObjectFactory-Class.md)|Stellt ein Objektfactory zum Materialisieren von Datenquellen aus der JNDI \(Java Naming and Directory Interface\) dar.|  
|[SQLServerDriver](../content/SQLServerDriver-Class.md)|Stellt den JDBC\-Treiber dar. Diese Klasse enthält Methoden zum Herstellen einer Verbindung mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank sowie zum Abrufen von Informationen zum JDBC\-Treiber.|  
|[SQLServerException](../content/SQLServerException-Class.md)|Stell die fehlerhafte oder unvollständige Ausführung einer SQL\-Anweisung dar.|  
|[SQLServerNClob\-Klasse](../content/SQLServerNClob-Class.md)|Stellt ein CLOB \(Character Large Binary Object\) mit nationalem Zeichensatz dar.|  
|[SQLServerParameterMetaData](../content/SQLServerParameterMetaData-Class.md)|Stellt die Metadaten für die Parameter vorbereiteter Anweisungen dar.|  
|[SQLServerPooledConnection](../content/SQLServerPooledConnection-Class.md)|Stellt eine physische Datenbankverbindung in einem Verbindungspool dar.|  
|[SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)|Implementiert ISQLServerPreparedStatement.|  
|[SQLServerResource](../content/SQLServerResource-Class.md)|Stellt eine Ressource für lokalisierte Fehlerzeichenfolgen dar. Diese Klasse dient nur zur internen Verwendung.|  
|[SQLServerResultSet](../content/SQLServerResultSet-Class.md)|Implementiert ISQLServerResultSet.|  
|[SQLServerResultSetMetaData](../content/SQLServerResultSetMetaData-Class.md)|Stellt die Metadaten der Spalten innerhalb eines Resultsets dar.|  
|[SQLServerSavepoint](../content/SQLServerSavepoint-Class.md)|Stellt den Prüfpunkt dar, bis zu dem ein Transaktionsrollback durchgeführt werden kann.|  
|[SQLServerStatement](../content/SQLServerStatement-Class.md)|Implementiert ISQLServerStatement.|  
|[SQLServerXAConnection](../content/SQLServerXAConnection-Class.md)|Stellt JDBC\-Verbindungen dar, die an verteilten Transaktionen \(XA\-Transaktionen\) beteiligt sein können.|  
|[SQLServerXADataSource](../content/SQLServerXADataSource-Class.md)|Stellt eine intern verwendete Factory für [SQLServerXAConnectio](../content/SQLServerXAConnection-Class.md)n\-Objekte dar.|  
|[SQLServerXAResource](../content/SQLServerXAResource-Class.md)|Stellt eine XAResource für die Verwaltung verteilter XA\-Transaktionen dar.|  
  
## Siehe auch  
 [Übersicht über den JDBC-Treiber](../content/Overview-of-the-JDBC-Driver.md)  
  
  