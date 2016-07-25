---
title: "Ablaufverfolgung f&#252;r Treibervorg&#228;nge"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 723aeae7-6504-4585-ba8b-3525115bea8b
caps.latest.revision: 42
caps.handback.revision: 41
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
# Ablaufverfolgung f&#252;r Treibervorg&#228;nge
  [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] unterstützt Ablaufverfolgung \(oder Protokollierung\), um die Lösung von Problemen mit dem JDBC\-Treiber in der Anwendung zu ermöglichen. Für die Ablaufverfolgung verwendet der JDBC\-Treiber die Protokollierungs\-APIs in "java.util.logging", die eine Reihe von Klassen zum Erstellen von Logger\- und LogRecord\-Objekten bereitstellen.  
  
> [!NOTE]  
>  Für die im JDBC\-Treiber enthaltene systemeigene Komponente \("sqljdbc\_xa.dll"\) wird die Ablaufverfolgung durch das BID\-Framework \(Built\-In Diagnostics\) ermöglicht. Informationen zu BID finden Sie unter [Data Access Tracing in SQL Server 2005](http://go.microsoft.com/fwlink/?LinkId=70042).  
  
 Beim Entwickeln Ihrer Anwendung können Sie Logger\-Objekte aufrufen, die ihrerseits LogRecord\-Objekte erstellen, die dann zur Verarbeitung an Handler\-Objekte übergeben werden.Logger und Handler arbeiten beide mit Protokollgraden und optional Protokollfiltern, um zu regeln, welche LogRecords verarbeitet werden. Nach Abschluss der Protokolliervorgänge können die Handler\-Objekte die Protokollinformationen ggf. mit Formatter\-Objekten veröffentlichen.  
  
 Standardmäßig erfolgt die Ausgabe des java.util.logging\-Frameworks in eine Datei. Diese Ausgabeprotokolldatei muss Schreibberechtigungen für den Kontext aufweisen, unter dem der JDBC\-Treiber ausgeführt wird.  
  
> [!NOTE]  
>  Weitere Informationen zur Verwendung der verschiedenen Protokollierungsobjekte für die Programmablaufverfolgung finden Sie unter Java Logging APIs auf der Sun Microsystems\-Website.  
  
 Die folgenden Abschnitte beschreiben die Protokolliergrade sowie die protokollierbaren Kategorien und enthalten Informationen darüber, wie die Ablaufverfolgung in der Anwendung aktiviert werden kann.  
  
## Protokolliergrade  
 Jeder erstellten Protokollmeldung ist ein Protokolliergrad zugeordnet. Der Protokolliergrad bestimmt die Wichtigkeit der Protokollmeldung, die durch die **Level**\-Klasse in „java.util.logging“ definiert wird. Durch Aktivieren der Protokollierung für einen bestimmten Grad wird auch das Protokollieren für alle höheren Grade aktiviert. In diesem Abschnitt werden die Protokolliergrade für öffentliche und interne Protokollierungskategorien beschrieben. Weitere Informationen zu den Protokollierungskategorien finden Sie in diesem Thema im Abschnitt "Protokollierungskategorien".  
  
 Die verfügbaren Protokolliergrade für öffentliche Protokollierungskategorien werden in der folgenden Tabelle beschrieben:  
  
|Name|Beschreibung|  
|----------|------------------|  
|SEVERE|Der höchste Protokolliergrad, der schwerwiegende Fehler kennzeichnet. Im JDBC\-Treiber wird dieser Grad für Fehler und Ausnahmen verwendet.|  
|WARNING|Kennzeichnet ein mögliches Problem.|  
|INFO|Stellt informative Meldungen bereit.|  
|CONFIG|Stellt Konfigurationsmeldungen bereit. Beachten Sie, dass der JDBC\-Treiber derzeit keine Konfigurationsmeldungen bereitstellt.|  
|FINE|Stellt grundlegende Ablaufverfolgungsinformationen einschließlich aller von den öffentlichen Methoden ausgelösten Ausnahmen bereit.|  
|FINER|Stellt ausführliche Ablaufverfolgungsinformationen einschließlich aller Ein\- und Ausstiegspunkte von öffentlichen Methoden mit den zugeordneten Parameterdatentypen und allen öffentlichen Eigenschaften für öffentliche Klassen bereit. Außerdem Eingabeparameter, Ausgabeparameter und Methodenrückgabewerte mit Ausnahme der Rückgabewerttypen CLOB, BLOB, NCLOB, Reader und \<stream\>.|  
|FINEST|Stellt sehr ausführliche Ablaufverfolgungsinformationen bereit. Dieser Grad ist der niedrigste Protokolliergrad.|  
|OFF|Schaltet die Protokollierung aus.|  
|ALL|Aktiviert die Protokollierung aller Meldungen.|  
  
 Die verfügbaren Protokolliergrade für interne Protokollierungskategorien werden in der folgenden Tabelle beschrieben:  
  
|Name|Beschreibung|  
|----------|------------------|  
|SEVERE|Der höchste Protokolliergrad, der schwerwiegende Fehler kennzeichnet. Im JDBC\-Treiber wird dieser Grad für Fehler und Ausnahmen verwendet.|  
|WARNING|Kennzeichnet ein mögliches Problem.|  
|INFO|Stellt informative Meldungen bereit.|  
|FINE|Stellt Ablaufverfolgungsinformationen einschließlich grundlegender Informationen zum Erstellen und Löschen von Objekten. Außerdem alle von den öffentlichen Methoden ausgelösten Ausnahmen.|  
|FINER|Stellt ausführliche Ablaufverfolgungsinformationen einschließlich aller Ein\- und Ausstiegspunkte von öffentlichen Methoden mit den zugeordneten Parameterdatentypen und allen öffentlichen Eigenschaften für öffentliche Klassen bereit. Außerdem Eingabeparameter, Ausgabeparameter und Methodenrückgabewerte mit Ausnahme der Rückgabewerttypen CLOB, BLOB, NCLOB, Reader und \<stream\>.<br /><br /> In Version 1.2 von JDBC Driver waren die folgenden Protokollierungskategorien vorhanden, die auch den Protokolliergrad FINE aufweisen: [SQLServerConnection](../content/SQLServerConnection-Class.md), [SQLServerStatement](../content/SQLServerStatement-Class.md), XA und [SQLServerDataSource](../content/SQLServerDataSource-Class.md). Diese wurden ab Version 2.0 auf den Grad FINER hochgestuft.|  
|FINEST|Stellt sehr ausführliche Ablaufverfolgungsinformationen bereit. Dieser Grad ist der niedrigste Protokolliergrad.<br /><br /> In Version 1.2 von JDBC Driver waren die folgenden Protokollierungskategorien vorhanden, die auch den Protokolliergrad FINEST aufweisen: TDS.DATA und TDS.TOKEN. Diese behalten ab Version 2.0 den Protokolliergrad FINEST bei.|  
|OFF|Schaltet die Protokollierung aus.|  
|ALL|Aktiviert die Protokollierung aller Meldungen.|  
  
## Protokollierungskategorien  
 Wenn Sie ein Logger\-Objekt erstellen, müssen Sie an das Objekt die benannte Entität oder Kategorie übergeben, über die Protokollinformationen ermittelt werden sollen. Der JDBC\-Treiber unterstützt die folgenden öffentlichen Protokollierungskategorien, die alle im com.microsoft.sqlserver.jdbc\-Treiberpaket definiert sind.  
  
|Name|Beschreibung|  
|----------|------------------|  
|Verbindung|Protokolliert Meldungen in der [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Klasse. Die Anwendungen können den Protokolliergrad auf FINER festlegen.|  
|Statement|Protokolliert Meldungen in der [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Klasse. Die Anwendungen können den Protokolliergrad auf FINER festlegen.|  
|DataSource|Protokolliert Meldungen in der [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Klasse. Die Anwendungen können den Protokolliergrad auf FINE festlegen.|  
|ResultSet|Protokolliert Meldungen in der [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Klasse. Die Anwendungen können den Protokolliergrad auf FINER festlegen.|  
|Treiber|Protokolliert Meldungen in der [SQLServerDriver](../content/SQLServerDriver-Class.md)\-Klasse. Die Anwendungen können den Protokolliergrad auf FINER festlegen.|  
  
 Ab Version 2.0 von Microsoft JDBC Driver stellt der Treiber auch das com.microsoft.sqlserver.jdbc.internals\-Paket bereit, das die Protokollierungsunterstützung für die folgenden internen Protokollierungskategorien enthält.  
  
|Name|Beschreibung|  
|----------|------------------|  
|AuthenticationJNI|Protokolliert Meldungen zu Problemen mit der integrierten Windows\-Authentifizierung \(wenn die **authenticationScheme**\-Verbindungseigenschaft implizit oder explizit auf **NativeAuthentication** festgelegt ist\).<br /><br /> Die Anwendungen können den Protokolliergrad auf FINER und FINE festlegen.|  
|SQLServerConnection|Protokolliert Meldungen in der [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Klasse. Die Anwendungen können den Protokolliergrad auf FINE und FINER festlegen.|  
|SQLServerDataSource|Protokolliert Meldungen in den [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-, [SQLServerConnectionPoolDataSource](../content/SQLServerConnectionPoolDataSource-Class.md)\- und [SQLServerPooledConnection](../content/SQLServerPooledConnection-Class.md)\-Klassen.<br /><br /> Die Anwendungen können den Protokolliergrad auf FINER festlegen.|  
|InputStream|Protokolliert Meldungen zu den folgenden Datentypen: java.io.InputStream, java.io.Reader und Datentypen mit einem max\-Spezifizierer wie die Datentypen varchar, nvarchar und varbinary.<br /><br /> Die Anwendungen können den Protokolliergrad auf FINER festlegen.|  
|SQLServerException|Protokolliert Meldungen in der [SQLServerException](../content/SQLServerException-Class.md)\-Klasse. Die Anwendungen können den Protokolliergrad auf FINE festlegen.|  
|SQLServerResultSet|Protokolliert Meldungen in der [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Klasse. Die Anwendungen können den Protokolliergrad auf FINE, FINER und FINEST festlegen.|  
|SQLServerStatement|Protokolliert Meldungen in der [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Klasse. Die Anwendungen können den Protokolliergrad auf FINE, FINER und FINEST festlegen.|  
|XA|Protokolliert Meldungen für alle XA\-Transaktionen in der [SQLServerXADataSource](../content/SQLServerXADataSource-Class.md)\-Klasse. Die Anwendungen können den Protokolliergrad auf FINE und FINER festlegen.|  
|KerbAuthentication|Protokolliert Meldungen zur Kerberos\-Authentifizierung Typ 4 \(wenn die **authenticationScheme**\-Verbindungseigenschaft auf **JavaKerberos** festgelegt ist\). Für die Anwendung kann der Protokolliergrad auf FINE oder FINER festgelegt werden.|  
|TDS.DATA|Protokolliert Meldungen, die Konversationen auf TDS\-Protokollebene zwischen Treiber und SQL Server enthalten. Die ausführlichen Inhalte jedes gesendeten und empfangenen TDS\-Pakets werden in ASCII und hexadezimal protokolliert. Die Anmeldeinformationen \(Benutzernamen und Kennwörter\) werden nicht protokolliert. Alle sonstigen Daten werden protokolliert.<br /><br /> Diese Kategorie erstellt sehr ausführliche Meldungen. Sie kann nur aktiviert werden, indem der Protokolliergrad auf FINEST festgelegt wird.|  
|TDS.Channel|Diese Kategorie verfolgt Aktionen der TCP\-Kommunikationskanäle mit SQL Server. Die protokollierten Meldungen umfassen das Öffnen und Schließen von Sockets sowie Lese\- und Schreibvorgänge. Außerdem werden Meldungen zum Herstellen einer SSL \(Secure Sockets Layer\)\-Verbindung mit SQL Server verfolgt.<br /><br /> Diese Kategorie kann nur aktiviert werden, indem der Protokolliergrad auf FINE, FINER oder FINEST festgelegt wird.|  
|TDS.Writer|Diese Kategorie verfolgt Schreibvorgänge für den TDS\-Kanal. Beachten Sie, dass nur die Länge der Schreibvorgänge verfolgt wird, nicht deren Inhalt. Diese Kategorie verfolgt außerdem Probleme, wenn zum Abbrechen der Ausführung einer Anweisung ein Achtungssignal gesendet wird.<br /><br /> Diese Kategorie kann nur aktiviert werden, indem der Protokolliergrad auf FINEST festgelegt wird.|  
|TDS.Reader|Diese Kategorie verfolgt bestimmte Lesevorgänge für den TDS\-Kanal mit dem Grad FINEST. Die Nachverfolgung mit dem Grad FINEST ist möglicherweise sehr ausführlich. Mit den Graden WARNING und SEVERE wird in dieser Kategorie verfolgt, wenn der Treiber ein ungültiges TDS\-Protokoll von SQL Server empfängt, bevor der Treiber die Verbindung trennt.<br /><br /> Diese Kategorie kann nur aktiviert werden, indem der Protokolliergrad auf FINER und FINEST festgelegt wird.|  
|TDS.Command|Diese Kategorie verfolgt Zustandsübergänge auf niedriger Ebene und sonstige Informationen zur Ausführung von TDS\-Befehlen wie der Ausführung von [!INCLUDE[tsql](../content/includes/tsql_md.md)]\-Anweisungen, Abrufvorgängen von ResultSet\-Cursorn, Commits usw.<br /><br /> Diese Kategorie kann nur aktiviert werden, indem der Protokolliergrad auf FINEST festgelegt wird.|  
|TDS.TOKEN|Diese Kategorie protokolliert nur die Token im TDS\-Paket und ist weniger ausführlich als die TDS.DATA\-Kategorie. Sie kann nur aktiviert werden, indem der Protokolliergrad auf FINEST festgelegt wird.<br /><br /> Mit dem Grad FINEST verfolgt diese Kategorie TDS\-Token bei der Verarbeitung in der Antwort. Mit dem Grad SEVERE verfolgt diese Kategorie das Auftreten ungültiger TDS\-Token.|  
|SQLServerDatabaseMetaData|Protokolliert Meldungen in der [SQLServerDatabaseMetaData](../content/SQLServerDatabaseMetaData-Class.md)\-Klasse. Die Anwendungen können den Protokolliergrad auf FINE festlegen.|  
|SQLServerResultSetMetaData|Protokolliert Meldungen in der [SQLServerResultSetMetaData](../content/SQLServerResultSetMetaData-Class.md)\-Klasse. Die Anwendungen können den Protokolliergrad auf FINE festlegen.|  
|SQLServerParameterMetaData|Protokolliert Meldungen in der [SQLServerParameterMetaData](../content/SQLServerParameterMetaData-Class.md)\-Klasse. Die Anwendungen können den Protokolliergrad auf FINE festlegen.|  
|SQLServerBlob|Protokolliert Meldungen in der [SQLServerBlob](../content/SQLServerBlob-Class.md)\-Klasse. Die Anwendungen können den Protokolliergrad auf FINE festlegen.|  
|SQLServerClob|Protokolliert Meldungen in der [SQLServerClob](../content/SQLServerClob-Class.md)\-Klasse. Die Anwendungen können den Protokolliergrad auf FINE festlegen.|  
|SQLServerSQLXML|Protokolliert Meldungen in der internen SQLServerSQLXML\-Klasse. Die Anwendungen können den Protokolliergrad auf FINE festlegen.|  
|SQLServerDriver|Protokolliert Meldungen in der [SQLServerDriver](../content/SQLServerDriver-Class.md)\-Klasse. Die Anwendungen können den Protokolliergrad auf FINE festlegen.|  
|SQLServerNClob|Protokolliert Meldungen in der [SQLServerNClob](../content/SQLServerNClob-Class.md)\-Klasse. Die Anwendungen können den Protokolliergrad auf FINE festlegen.|  
  
## Programmgesteuerte Aktivierung der Ablaufverfolgung  
 Die Ablaufverfolgung kann programmgesteuert aktiviert werden, indem ein Logger\-Objekt erstellt und die zu protokollierende Kategorie angegeben wird. Der folgende Code veranschaulicht beispielsweise, wie die Protokollierung für SQL\-Anweisungen aktiviert wird:  
  
```  
Logger logger = Logger.getLogger("com.microsoft.sqlserver.jdbc.Statement");  
logger.setLevel(Level.FINER);  
```  
  
 Die Protokollierung können Sie im Code folgendermaßen deaktivieren:  
  
```  
logger.setLevel(Level.OFF);  
```  
  
 Mit dem folgenden Code können Sie alle verfügbaren Kategorien protokollieren:  
  
```  
Logger logger = Logger.getLogger("com.microsoft.sqlserver.jdbc");  
logger.setLevel(Level.FINE);  
```  
  
 Mit dem folgenden Code können Sie die Protokollierung einer bestimmten Kategorie deaktivieren:  
  
```  
Logger logger = Logger.getLogger("com.microsoft.sqlserver.jdbc.Statement");  
logger.setLevel(Level.OFF);  
```  
  
## Aktivieren der Ablaufverfolgung mit der Datei "Logging.Properties"  
 Sie können die Ablaufverfolgung auch mit der Datei `logging.properties` aktivieren, die sich im Verzeichnis `lib` der JRE\-Installation \(Java Runtime Environment\) befindet. In dieser Datei können Sie die Standardwerte für die Protokollierungund Handler festlegen, die bei Aktivierung der Ablaufverfolgung verwendet werden sollen.  
  
 Das folgende Beispiel veranschaulicht die Einstellungen, die in `logging.properties`\-Dateien vorgenommen werden können:  
  
```  
# Specify the handler, the handlers will be installed during VM startup.  
handlers= java.util.logging.FileHandler  
  
# Default global logging level.  
.level= OFF  
  
# default file output is in user's home directory.  
java.util.logging.FileHandler.pattern = %h/java%u.log  
java.util.logging.FileHandler.limit = 5000000  
java.util.logging.FileHandler.count = 20  
java.util.logging.FileHandler.formatter = java.util.logging.SimpleFormatter  
java.util.logging.FileHandler.level = FINEST  
  
# Facility specific properties.  
com.microsoft.sqlserver.jdbc.level=FINEST  
  
```  
  
> [!NOTE]  
>  Mit dem  `logging.properties` \-Objekt, das Bestandteil von "java.util.logging" ist, können Sie die Eigenschaften in der DateiLogManagerfestlegen.  
  
## Siehe auch  
 [Diagnostizieren von Problemen mit dem JDBC-Treiber](../content/Diagnosing-Problems-with-the-JDBC-Driver.md)  
  
  