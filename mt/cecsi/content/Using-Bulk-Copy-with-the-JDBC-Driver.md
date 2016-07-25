---
title: "Verwenden von Massenkopieren mit dem JDBC Driver"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 21e19635-340d-49bb-b39d-4867102fb5df
caps.latest.revision: 14
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
  - zh-cn
  - zh-tw
---
# Verwenden von Massenkopieren mit dem JDBC Driver
  Microsoft SQL Server enthält ein beliebtes Befehlszeilen\-Hilfsprogramm mit dem Namen **bcp** zum schnellen Massenkopieren großer Dateiumfänge in Tabellen oder Ansichten in SQL Server\-Datenbanken. Die Klasse „SQLServerBulkCopy“ ermöglicht Ihnen das Erstellen von Codelösungen in Java, die eine ähnliche Funktionalität bereitstellen. Es gibt eine Reihe weiterer Verfahren, Daten in eine SQL\-Server\-Tabelle zu laden \(beispielsweise INSERT\-Anweisungen\), doch bietet „SQLServerBulkCopy“ ihnen gegenüber einen erheblichen Leistungsvorteil.  
  
 Die Klasse „SQLServerBulkCopy“ kann nur verwendet werden, um Daten in SQL Server\-Tabellen zu schreiben. Die Datenquelle ist aber nicht auf SQL Server beschränkt; jede beliebige Datenquelle kann verwendet werden, sofern die Daten mit einer Implementierung von „ResultSet“, „RowSet“ oder „ISQLServerBulkRecord“ gelesen werden können.  
  
 Mithilfe der SQLServerBulkCopy\-Klasse können Sie folgende Vorgänge ausführen:  
  
-   Einen einzelnen Massenkopiervorgang  
  
-   Mehrere Massenkopiervorgänge  
  
-   Einen Massenkopiervorgang mit einer Transaktion  
  
> [!NOTE]  
>  Wenn Sie den Microsoft JDBC Driver 4.1 für SQL Server \(der die SQLServerBulkCopy\-Klasse nicht unterstützt\) oder eine frühere Version verwenden, können Sie stattdessen die SQL Server Transact\-SQL\-Anweisung „BULK INSERT“ ausführen.  
  
## Einrichten des Massenkopierbeispiels  
 Die Klasse „SQLServerBulkCopy“ kann nur verwendet werden, um Daten in SQL Server\-Tabellen zu schreiben. Die in diesem Thema gezeigten Codebeispiele verwenden die SQL Server\-Beispieldatenbank „AdventureWorks“. Um eine Änderung der vorhandenen Codebeispiele zu vermeiden, schreiben die Codebeispiele Daten in Tabellen, die zuvor von Ihnen erstellt werden.  
  
 Die Tabellen „BulkCopyDemoMatchingColumns“ und „BulkCopyDemoDifferentColumns“ basieren beide auf der Tabelle „AdventureWorks Production.Products“. In Codebeispielen, die diese Tabellen verwenden, werden Daten aus der Tabelle „Production.Products“ einer dieser Beispieltabellen hinzugefügt. Die Tabelle „BulkCopyDemoDifferentColumns“ wird verwendet, um im Beispiel zu veranschaulichen, wie Spalten aus den Quelldaten der Zieltabelle zugeordnet werden; für die meisten anderen Beispiele wird „BulkCopyDemoMatchingColumns“ verwendet.  
  
 Einige der Codebeispiele zeigen, wie eine Klasse „SQLServerBulkCopy“ zum Schreiben in mehrere Tabellen verwendet werden kann. Für diese Beispiele werden die Tabellen „BulkCopyDemoOrderHeader“ und „BulkCopyDemoOrderDetail“ als Zieltabellen verwendet. Diese Tabellen basieren auf den Tabellen „Sales.SalesOrderHeader“ und „Sales.SalesOrderDetail“ in „AdventureWorks“.  
  
> [!NOTE]  
>  Die Codebeispiele zu „SQLServerBulkCopy“ werden nur zur Verfügung gestellt, um die Syntax für die Verwendung von „SQLServerBulkCopy“ zu veranschaulichen. Wenn sich die Quell\- und Zieltabellen in der gleichen SQL Server\-Instanz befinden, ist die Verwendung einer Transact\-SQL\-Anweisung „INSERT … SELECT“ zum Kopieren der Daten einfacher und schneller.  
  
###  <a name="BKMK_TableSetup"></a> Tabelleneinrichtung  
 Zum Erstellen der Tabellen, die für die ordnungsgemäße Ausführung der Codebeispiele erforderlich sind, müssen Sie die folgenden Transact\-SQL\-Anweisungen in einer SQL Server\-Datenbank ausführen.  
  
```  
USE AdventureWorks IF EXISTS (SELECT * FROM dbo.sysobjects WHERE id = object_id(N'[dbo].[BulkCopyDemoMatchingColumns]') AND OBJECTPROPERTY(id, N'IsUserTable') = 1) DROP TABLE [dbo].[BulkCopyDemoMatchingColumns] CREATE TABLE [dbo].[BulkCopyDemoMatchingColumns]([ProductID] [int]) ON [PRIMARY] IF EXISTS (SELECT * FROM dbo.sysobjects WHERE id = object_id(N'[dbo].[BulkCopyDemoDifferentColumns]') AND OBJECTPROPERTY(id, N'IsUserTable') = 1) DROP TABLE [dbo].[BulkCopyDemoDifferentColumns] CREATE TABLE [dbo].[BulkCopyDemoDifferentColumns]([ProdID] [int]) ON [PRIMARY] IF EXISTS (SELECT * FROM dbo.sysobjects WHERE id = object_id(N'[dbo].[BulkCopyDemoOrderHeader]') AND OBJECTPROPERTY(id, N'IsUserTable') = 1) DROP TABLE [dbo].[BulkCopyDemoOrderHeader] CREATE TABLE [dbo].[BulkCopyDemoOrderHeader]([SalesOrderID] [int]) ON [PRIMARY] IF EXISTS (SELECT * FROM dbo.sysobjects WHERE id = object_id(N'[dbo].[BulkCopyDemoOrderDetail]') AND OBJECTPROPERTY(id, N'IsUserTable') = 1) DROP TABLE [dbo].[BulkCopyDemoOrderDetail] CREATE TABLE [dbo].[BulkCopyDemoOrderDetail]([SalesOrderID] [int]) ON [PRIMARY]  
  
```  
  
## Einzelne Massenkopiervorgänge  
 Die einfachste Herangehensweise an einen SQL Server\-Massenkopiervorgang ist das Durchführen eines einzelnen Vorgangs für eine Datenbank. Standardmäßig wird ein Massenkopiervorgang als isolierter Vorgang ausgeführt: Der Kopiervorgang erfolgt in nicht transaktionaler Weise, ohne Möglichkeit zum Rollback.  
  
> [!NOTE]  
>  Wenn Sie für den Massenkopiervorgang beim Auftreten eines Fehlers einen teilweisen oder vollständigen Rollback ausführen müssen, können Sie entweder eine verwaltete SQLServerBulkCopy\-Transaktion verwenden oder den Massenkopiervorgang innerhalb einer vorhandenen Transaktion ausführen.  
>   
>  Weitere Informationen finden Sie unter [Transaktionen und Massenkopiervorgänge](../content/Using-Bulk-Copy-with-the-JDBC-Driver.md#BKMK_TransactionBulk).  
  
 Dies sind die allgemeinen Schritte zum Durchführen eines Massenkopiervorgangs:  
  
1.  Herstellen einer Verbindung mit dem Quellserver und Abrufen der zu kopierenden Daten. Daten können auch aus anderen Quellen stammen, sofern sie von einem ResultSet\-Objekt oder einer ISQLServerBulkRecord\-Implementierung abgerufen werden können.  
  
2.  Herstellen einer Verbindung mit dem Zielserver \(es sei denn, Sie möchten **SQLServerBulkCopy** die Verbindung für Sie herstellen lassen\).  
  
3.  Erstellen eines SQLServerBulkCopy\-Objekts und Festlegen aller erforderlichen Eigenschaften mithilfe von **setBulkCopyOptions**.  
  
4.  Aufrufen der Methode **setDestinationTableName**, um die Zieltabelle für den Masseneinfügungsvorgang anzugeben.  
  
5.  Aufruf einer der **writeToServer**\-Methoden.  
  
6.  Optional Aktualisieren der Eigenschaften mithilfe von **setBulkCopyOptions** und bei Bedarf erneuter Aufruf von **writeToServer**.  
  
7.  Aufruf von **close** oder Umschließen der Massenkopiervorgänge durch eine try\-with\-resources\-Anweisung.  
  
> [!CAUTION]  
>  Wir empfehlen die Verwendung gleicher Datentypen für Quell\- und Zielspalten. Wenn die Datentypen nicht übereinstimmen, versucht „SQLServerBulkCopy“, jeden Quellwert in den Zieldatentyp zu konvertieren. Konvertierungen wirken sich negativ auf die Leistung aus und können außerdem zu unerwarteten Fehlern führen. Beispielsweise kann ein Datentyp „double“ in den meisten Fällen in den Datentyp „decimal“ konvertiert werden, aber nicht immer.  
  
### Beispiel  
 Die folgende Anwendung zeigt das Laden von Daten mithilfe der Klasse „SQLServerBulkCopy“. In diesem Beispiel wird ein „ResultSet“ verwendet, um Daten aus der Tabelle „Production.Product“ in der SQL Server AdventureWorks\-Datenbank in eine ähnliche Tabelle in der gleichen Datenbank zu kopieren.  
  
> [!IMPORTANT]  
>  Dieses Beispiel wird nur ausgeführt, wenn Sie die Arbeitstabellen zuvor wie in [Tabelleneinrichtung](../content/Using-Bulk-Copy-with-the-JDBC-Driver.md#BKMK_TableSetup) beschrieben erstellt haben. Dieser Code wird nur bereitgestellt, um die Syntax für die Verwendung von „SQLServerBulkCopy“ zu demonstrieren. Wenn sich die Quell\- und Zieltabellen in der gleichen SQL Server\-Instanz befinden, ist die Verwendung einer Transact\-SQL\-Anweisung „INSERT … SELECT“ zum Kopieren der Daten einfacher und schneller.  
  
```  
import java.sql.*; import com.microsoft.sqlserver.jdbc.SQLServerBulkCopy; public class Program { public static void main(String[] args) { String connectionString = GetConnectionString(); try { // Note: if you are not using try-with-resources statements (as here), // you must remember to call close() on any Connection, Statement, // ResultSet, and SQLServerBulkCopy objects that you create. // Open a sourceConnection to the AdventureWorks database. Class.forName("com.microsoft.sqlserver.jdbc.SQLServerDriver"); try (Connection sourceConnection = DriverManager.getConnection(connectionString)) { try (Statement stmt = sourceConnection.createStatement()) { // Perform an initial count on the destination table. long countStart = 0; try (ResultSet rsRowCount = stmt.executeQuery( "SELECT COUNT(*) FROM dbo.BulkCopyDemoMatchingColumns;")) { rsRowCount.next(); countStart = rsRowCount.getInt(1); System.out.println("Starting row count = " + countStart); } // Get data from the source table as a ResultSet. try (ResultSet rsSourceData = stmt.executeQuery( "SELECT ProductID, Name, ProductNumber FROM Production.Product")) { // Open the destination connection. In the real world you would // not use SQLServerBulkCopy to move data from one table to the other // in the same database. This is for demonstration purposes only. try (Connection destinationConnection = DriverManager.getConnection(connectionString)) { // Set up the bulk copy object. // Note that the column positions in the source // table match the column positions in // the destination table so there is no need to // map columns. try (SQLServerBulkCopy bulkCopy = new SQLServerBulkCopy(destinationConnection)) { bulkCopy.setDestinationTableName("dbo.BulkCopyDemoMatchingColumns"); try { // Write from the source to the destination. bulkCopy.writeToServer(rsSourceData); } catch (Exception e) { // Handle any errors that may have occurred. e.printStackTrace(); } } // Perform a final count on the destination // table to see how many rows were added. try (ResultSet rsRowCount = stmt.executeQuery( "SELECT COUNT(*) FROM dbo.BulkCopyDemoMatchingColumns;")) { rsRowCount.next(); long countEnd = rsRowCount.getInt(1); System.out.println("Ending row count = " + countEnd); System.out.println((countEnd - countStart) + " rows were added."); } } } } } } catch (Exception e) { // Handle any errors that may have occurred. e.printStackTrace(); } } // To avoid storing the sourceConnection String in your code, // you can retrieve it from a configuration file. private static String GetConnectionString() { // Create a variable for the connection string. String connectionUrl = "jdbc:sqlserver://localhost:1433;" + "databaseName=AdventureWorks;user=UserName;password=*****"; return connectionUrl; } }  
```  
  
### Ausführen eines Massenkopiervorgangs mithilfe von Transact\-SQL  
 Das folgende Beispiel zeigt die Verwendung der Methode „executeUpdate“ zum Ausführen der Anweisung „BULK INSERT“.  
  
> [!NOTE]  
>  Der Dateipfad für die Datenquelle ist relativ zum Server. Der Serverprozess muss Zugriff auf diesen Pfad besitzen, damit der Massenkopiervorgang erfolgreich ausgeführt werden kann.  
  
```  
try (Connection con = DriverManager.getConnection(connectionString)) { try (Statement stmt = con.createStatement()) { // Perform the BULK INSERT stmt.executeUpdate( "BULK INSERT Northwind.dbo.[Order Details] " + "FROM 'f:\\mydata\\data.tbl' " + "WITH ( FORMATFILE='f:\\mydata\\data.fmt' )"); } }  
```  
  
## Mehrere Massenkopiervorgänge  
 Mithilfe einer einzelnen Instanz einer SQLServerBulkCopy\-Klasse können Sie mehrere Massenkopiervorgänge ausführen. Wenn sich die Parameter für den Vorgang zwischen den Ausführungen ändern \(z. B. der Name der Zieltabelle\), müssen Sie sie vor allen nachfolgenden Aufrufen einer der writeToServer\-Methoden ändern, wie im folgenden Beispiel gezeigt. Sofern sie nicht explizit geändert werden, bleiben alle Eigenschaftswerte die gleichen wie beim letzten Massenkopiervorgang für eine bestimmte Instanz.  
  
> [!NOTE]  
>  Das Ausführen mehrerer Massenkopiervorgänge mithilfe der gleichen Instanz von SQLServerBulkCopy ist normalerweise effizienter als die Verwendung einer separaten Instanz für jeden Vorgang.  
  
 Wenn Sie mehrere Massenkopiervorgänge mithilfe des gleichen SQLServerBulkCopy\-Objekts ausführen, bestehen normalerweise keine Einschränkungen hinsichtlich der Gleichheit oder Verschiedenheit der Quell\- und Zielinformationen für die einzelnen Vorgänge. Sie müssen jedoch sicherstellen, dass die Informationen zur Spaltenzuordnung bei jedem Schreibvorgang auf dem Server ordnungsgemäß festgelegt sind.  
  
> [!IMPORTANT]  
>  Dieses Beispiel wird nur ausgeführt, wenn Sie die Arbeitstabellen zuvor wie in [Tabelleneinrichtung](../content/Using-Bulk-Copy-with-the-JDBC-Driver.md#BKMK_TableSetup) beschrieben erstellt haben. Dieser Code wird nur bereitgestellt, um die Syntax für die Verwendung von „SQLServerBulkCopy“ zu demonstrieren. Wenn sich die Quell\- und Zieltabellen in der gleichen SQL Server\-Instanz befinden, ist die Verwendung einer Transact\-SQL\-Anweisung „INSERT … SELECT“ zum Kopieren der Daten einfacher und schneller.  
  
```  
import java.sql.*; import com.microsoft.sqlserver.jdbc.SQLServerBulkCopy; public class Program { public static void main(String[] args) { String connectionString = GetConnectionString(); try { // Note: if you are not using try-with-resources statements (as here), // you must remember to call close() on any Connection, Statement, // ResultSet, and SQLServerBulkCopy objects that you create. // Open a sourceConnection to the AdventureWorks database. Class.forName("com.microsoft.sqlserver.jdbc.SQLServerDriver"); try (Connection sourceConnection1 = DriverManager.getConnection(connectionString)) { try (Statement stmt = sourceConnection1.createStatement()) { // Empty the destination tables. stmt.executeUpdate("DELETE FROM dbo.BulkCopyDemoOrderHeader;"); stmt.executeUpdate("DELETE FROM dbo.BulkCopyDemoOrderDetail;"); // Perform an initial count on the destination //  table with matching columns. long countStartHeader = 0; try (ResultSet rsRowCountHeader = stmt.executeQuery( "SELECT COUNT(*) FROM dbo.BulkCopyDemoOrderHeader;")) { rsRowCountHeader.next(); countStartHeader = rsRowCountHeader.getInt(1); System.out.println("Starting row count for Header table = " + countStartHeader); } // Perform an initial count on the destination // table with different column positions. long countStartDetail = 0; try (ResultSet rsRowCountDetail = stmt.executeQuery( "SELECT COUNT(*) FROM dbo.BulkCopyDemoOrderDetail;")) { rsRowCountDetail.next(); countStartDetail = rsRowCountDetail.getInt(1); System.out.println("Starting row count for Detail table = " + countStartDetail); } // Get data from the source table as a ResultSet. // The Sales.SalesOrderHeader and Sales.SalesOrderDetail // tables are quite large and could easily cause a timeout // if all data from the tables is added to the destination. // To keep the example simple and quick, a parameter is // used to select only orders for a particular account // as the source for the bulk insert. try (PreparedStatement preparedStmt1 = sourceConnection1.prepareStatement( "SELECT [SalesOrderID], [OrderDate], " + "[AccountNumber] FROM [Sales].[SalesOrderHeader] " + "WHERE [AccountNumber] = ?;")) { preparedStmt1.setString(1, "10-4020-000034"); try (ResultSet rsHeader = preparedStmt1.executeQuery()) { // Get the Detail data in a separate connection. try (Connection sourceConnection2 = DriverManager.getConnection(connectionString)) { try (PreparedStatement preparedStmt2 = sourceConnection2.prepareStatement( "SELECT [Sales].[SalesOrderDetail].[SalesOrderID], " + "[SalesOrderDetailID], [OrderQty], [ProductID], " + "[UnitPrice] FROM [Sales].[SalesOrderDetail] " + "INNER JOIN [Sales].[SalesOrderHeader] " + "ON [Sales].[SalesOrderDetail].[SalesOrderID] " + "= [Sales].[SalesOrderHeader].[SalesOrderID] " + "WHERE [AccountNumber] = ?;")) { preparedStmt2.setString(1, "10-4020-000034"); try (ResultSet rsDetail = preparedStmt2.executeQuery()) { // Create the SQLServerBulkCopySQLServerBulkCopy object. try (SQLServerBulkCopy bulkCopy = new SQLServerBulkCopy(connectionString)) { bulkCopy.setBulkCopyOptions(copyOptions); bulkCopy.setDestinationTableName("dbo.BulkCopyDemoOrderHeader"); // Guarantee that columns are mapped correctly by // defining the column mappings for the order. bulkCopy.addColumnMapping("SalesOrderID", "SalesOrderID"); bulkCopy.addColumnMapping("OrderDate", "OrderDate"); bulkCopy.addColumnMapping("AccountNumber", "AccountNumber"); // Write rsHeader to the destination. try { bulkCopy.writeToServer(rsHeader); } catch (Exception e) { // Handle any errors that may have occurred. e.printStackTrace(); } // Set up the order details destination. bulkCopy.setDestinationTableName("dbo.BulkCopyDemoOrderDetail"); // Clear the existing column mappings bulkCopy.clearColumnMappings(); // Add order detail column mappings. bulkCopy.addColumnMapping("SalesOrderID", "SalesOrderID"); bulkCopy.addColumnMapping( "SalesOrderDetailID", "SalesOrderDetailID"); bulkCopy.addColumnMapping("OrderQty", "OrderQty"); bulkCopy.addColumnMapping("ProductID", "ProductID"); bulkCopy.addColumnMapping("UnitPrice", "UnitPrice"); // Write rsDetail to the destination. try { bulkCopy.writeToServer(rsDetail); } catch (Exception e) { // Handle any errors that may have occurred. e.printStackTrace(); } } } } } } } // Perform a final count on the destination // tables to see how many rows were added. try (ResultSet rsRowCountHeader = stmt.executeQuery( "SELECT COUNT(*) FROM dbo.BulkCopyDemoOrderHeader;")) { rsRowCountHeader.next(); long countEndHeader =  rsRowCountHeader.getInt(1); System.out.println( (countEndHeader - countStartHeader) + " rows were added to the Header table."); } try (ResultSet rsRowCountDetail = stmt.executeQuery( "SELECT COUNT(*) FROM dbo.BulkCopyDemoOrderDetail;")) { rsRowCountDetail.next(); long countEndDetail = rsRowCountDetail.getInt(1); System.out.println( (countEndDetail - countStartDetail) + " rows were added to the Detail table."); } } } } catch (Exception e) { // Handle any errors that may have occurred. e.printStackTrace(); } } // To avoid storing the sourceConnection String in your code, // you can retrieve it from a configuration file. private static String GetConnectionString() { // Create a variable for the connection string. String connectionUrl = "jdbc:sqlserver://localhost:1433;" + "databaseName=AdventureWorks;user=UserName;password=*****"; return connectionUrl; } }  
  
```  
  
##  <a name="BKMK_TransactionBulk"></a> Transaktionen und Massenkopiervorgänge  
 Massenkopiervorgänge können als isolierte Vorgänge oder im Rahmen einer aus mehreren Schritten bestehenden Transaktion ausgeführt werden. Diese zweite Option ermöglicht Ihnen das Ausführen mehrerer Massenkopiervorgänge innerhalb der gleichen Transaktion sowie die Durchführung weiterer Datenbankvorgänge \(wie etwa Einfüge\-, Aktualisierungs\- und Löschvorgänge\), während die Möglichkeit zum Commit oder Rollback der gesamten Transaktion erhalten bleibt.  
  
 Standardmäßig wird ein Massenkopiervorgang als isolierter Vorgang ausgeführt. Der Massenkopiervorgang erfolgt nicht transaktional, ohne Möglichkeit zum Rollback. Wenn Sie für den Massenkopiervorgang beim Auftreten eines Fehlers einen teilweisen oder vollständigen Rollback ausführen müssen, können Sie eine verwaltete SQLServerBulkCopy\-Transaktion verwenden oder den Massenkopiervorgang innerhalb einer vorhandenen Transaktion ausführen.  
  
### Ausführen eines nicht transaktionalen Massenkopiervorgangs  
 Die folgende Anwendung zeigt, was geschieht, wenn bei einem nicht transaktionalen Massenkopiervorgang nach teilweiser Ausführung ein Fehler auftritt.  
  
 In dem Beispiel enthalten Quell\- und Zieltabelle jeweils eine Identitätsspalte mit Namen **ProductID**. Der Code bereitet zunächst die Zieltabelle vor, indem er alle Zeilen löscht und dann eine einzelne Zeile einfügt, deren **ProductID** bekanntermaßen in der Quelltabelle vorhanden ist. Standardmäßig wird für die Spalte „Identity“ in der Zieltabelle für jede hinzugefügte Zeile ein neuer Wert generiert. In diesem Beispiel wird beim Öffnen der Verbindung eine Option festgelegt, die den Massenladevorgang zwingt, stattdessen die Identity\-Werte aus der Quelltabelle zu verwenden.  
  
 Der Massenkopiervorgang wird mit dem Wert „10“ für die Eigenschaft **BatchSize** ausgeführt. Wenn der Vorgang auf die ungültige Zeile trifft, wird eine Ausnahme ausgelöst. In diesem ersten Beispiel ist der Massenkopiervorgang nicht transaktional. Für alle bis zum Auftreten des Fehlers kopierten Batches wird ein Commit ausgeführt; für den Batch, der den doppelten Schlüssel enthält, wird ein Rollback ausgeführt, und der Massenkopiervorgang wird vor dem Verarbeiten weiterer Batches angehalten.  
  
> [!NOTE]  
>  Dieses Beispiel wird nur ausgeführt, wenn Sie die Arbeitstabellen zuvor wie in [Tabelleneinrichtung](../content/Using-Bulk-Copy-with-the-JDBC-Driver.md#BKMK_TableSetup) beschrieben erstellt haben. Dieser Code wird nur bereitgestellt, um die Syntax für die Verwendung von „SQLServerBulkCopy“ zu demonstrieren. Wenn sich die Quell\- und Zieltabellen in der gleichen SQL Server\-Instanz befinden, ist die Verwendung einer Transact\-SQL\-Anweisung „INSERT … SELECT“ zum Kopieren der Daten einfacher und schneller.  
  
```  
import java.sql.*; import com.microsoft.sqlserver.jdbc.SQLServerBulkCopy; import com.microsoft.sqlserver.jdbc.SQLServerBulkCopyOptions; public class Program { public static void main(String[] args) { String connectionString = GetConnectionString(); try { // Note: if you are not using try-with-resources statements (as here), // you must remember to call close() on any Connection, Statement, // ResultSet, and SQLServerBulkCopy objects that you create. // Open a sourceConnection to the AdventureWorks database. Class.forName("com.microsoft.sqlserver.jdbc.SQLServerDriver"); try (Connection sourceConnection = DriverManager.getConnection(connectionString)) { try (Statement stmt = sourceConnection.createStatement()) { //  Delete all from the destination table. stmt.executeUpdate("DELETE FROM dbo.BulkCopyDemoMatchingColumns"); //  Add a single row that will result in duplicate key //  when all rows from source are bulk copied. //  Note that this technique will only be successful in //  illustrating the point if a row with ProductID = 446 //  exists in the AdventureWorks Production.Products table. //  If you have made changes to the data in this table, change //  the SQL statement in the code to add a ProductID that //  does exist in your version of the Production.Products //  table. Choose any ProductID in the middle of the table //  (not first or last row) to best illustrate the result. stmt.executeUpdate("SET IDENTITY_INSERT dbo.BulkCopyDemoMatchingColumns ON;" + "INSERT INTO " + "dbo.BulkCopyDemoMatchingColumns " + "([ProductID], [Name] ,[ProductNumber]) " + "VALUES(446, 'Lock Nut 23','LN-3416');" + "SET IDENTITY_INSERT dbo.BulkCopyDemoMatchingColumns OFF"); // Perform an initial count on the destination table. long countStart = 0; try (ResultSet rsRowCount = stmt.executeQuery( "SELECT COUNT(*) FROM dbo.BulkCopyDemoMatchingColumns;")) { rsRowCount.next(); countStart = rsRowCount.getInt(1); System.out.println("Starting row count = " + countStart); } //  Get data from the source table as a ResultSet. try (ResultSet rsSourceData = stmt.executeQuery( "SELECT ProductID, Name, ProductNumber FROM Production.Product")) { // Set up the bulk copy object using the KeepIdentity option and BatchSize = 10. SQLServerBulkCopyOptions copyOptions = new SQLServerBulkCopyOptions(); copyOptions.setKeepIdentity(true); copyOptions.setBatchSize(10); try (SQLServerBulkCopy bulkCopy = new SQLServerBulkCopy(connectionString)) { bulkCopy.setBulkCopyOptions(copyOptions); bulkCopy.setDestinationTableName("dbo.BulkCopyDemoMatchingColumns"); // Write from the source to the destination. // This should fail with a duplicate key error // after some of the batches have been copied. try { bulkCopy.writeToServer(rsSourceData); } catch (Exception e) { // Handle any errors that may have occurred. e.printStackTrace(); } } } // Perform a final count on the destination // table to see how many rows were added. try (ResultSet rsRowCount = stmt.executeQuery( "SELECT COUNT(*) FROM dbo.BulkCopyDemoMatchingColumns;")) { rsRowCount.next(); long countEnd = rsRowCount.getInt(1); System.out.println("Ending row count = " + countEnd); System.out.println((countEnd - countStart) + " rows were added."); } } } } catch (Exception e) { // Handle any errors that may have occurred. e.printStackTrace(); } } // To avoid storing the sourceConnection String in your code, // you can retrieve it from a configuration file. private static String GetConnectionString() { // Create a variable for the connection String. String connectionUrl = "jdbc:sqlserver://localhost:1433;" + "databaseName=AdventureWorks;user=UserName;password=*****"; return connectionUrl; } }  
```  
  
### Ausführen eines dedizierten Massenkopiervorgangs in einer Transaktion  
 Standardmäßig stellt ein Massenkopiervorgang seine eigene Transaktion dar. Wenn Sie einen dedizierten Massenkopiervorgang ausführen möchten, erstellen Sie eine neue Instanz von „SQLServerBulkCopy“ mit einer Verbindungszeichenfolge. In diesem Szenario erstellt der Massenkopiervorgang die Transaktion, für die er dann einen Commit oder einen Rollback ausführt. Sie können explizit die Option **UseInternalTransaction** in **SQLServerBulkCopyOptions** angeben, um explizit die Ausführung eines Massenkopiervorgangs innerhalb einer eigenen Transaktion zu veranlassen, was dazu führt, dass jeder Batch des Massenkopiervorgangs in einer eigenen Transaktion ausgeführt wird.  
  
> [!NOTE]  
>  Da verschiedene Batches in verschiedenen Transaktionen ausgeführt werden, wird für alle Zeilen im aktuellen Batch beim Auftreten eines Fehlers ein Rollback ausgeführt, die Zeilen aus vorhergehenden Batches verbleiben jedoch in der Datenbank.  
  
 Die folgende Anwendung ähnelt dem vorhergehenden Beispiel, mit einer Ausnahme: In diesem Beispiel verwaltet der Massenkopiervorgang seine eigenen Transaktionen. Für alle bis zum Auftreten des Fehlers kopierten Batches wird ein Commit ausgeführt; für den Batch, der den doppelten Schlüssel enthält, wird ein Rollback ausgeführt, und der Massenkopiervorgang wird vor dem Verarbeiten weiterer Batches angehalten.  
  
> [!NOTE]  
>  Dieses Beispiel wird nur ausgeführt, wenn Sie die Arbeitstabellen zuvor wie in [Tabelleneinrichtung](../content/Using-Bulk-Copy-with-the-JDBC-Driver.md#BKMK_TableSetup) beschrieben erstellt haben. Dieser Code wird nur bereitgestellt, um die Syntax für die Verwendung von „SQLServerBulkCopy“ zu demonstrieren. Wenn sich die Quell\- und Zieltabellen in der gleichen SQL Server\-Instanz befinden, ist die Verwendung einer Transact\-SQL\-Anweisung „INSERT … SELECT“ zum Kopieren der Daten einfacher und schneller.  
  
```  
import java.sql.*; import com.microsoft.sqlserver.jdbc.SQLServerBulkCopy; import com.microsoft.sqlserver.jdbc.SQLServerBulkCopyOptions; public class Program { public static void main(String[] args) { String connectionString = GetConnectionString(); try { // Note: if you are not using try-with-resources statements (as here), // you must remember to call close() on any Connection, Statement, // ResultSet, and SQLServerBulkCopy objects that you create. // Open a sourceConnection to the AdventureWorks database. Class.forName("com.microsoft.sqlserver.jdbc.SQLServerDriver"); try (Connection sourceConnection = DriverManager.getConnection(connectionString)) { try (Statement stmt = sourceConnection.createStatement()) { //  Delete all from the destination table. stmt.executeUpdate("DELETE FROM dbo.BulkCopyDemoMatchingColumns"); //  Add a single row that will result in duplicate key //  when all rows from source are bulk copied. //  Note that this technique will only be successful in //  illustrating the point if a row with ProductID = 446 //  exists in the AdventureWorks Production.Products table. //  If you have made changes to the data in this table, change //  the SQL statement in the code to add a ProductID that //  does exist in your version of the Production.Products //  table. Choose any ProductID in the middle of the table //  (not first or last row) to best illustrate the result. stmt.executeUpdate("SET IDENTITY_INSERT dbo.BulkCopyDemoMatchingColumns ON;" + "INSERT INTO " + "dbo.BulkCopyDemoMatchingColumns " + "([ProductID], [Name] ,[ProductNumber]) " + "VALUES(446, 'Lock Nut 23','LN-3416');" + "SET IDENTITY_INSERT dbo.BulkCopyDemoMatchingColumns OFF"); // Perform an initial count on the destination table. long countStart = 0; try (ResultSet rsRowCount = stmt.executeQuery( "SELECT COUNT(*) FROM dbo.BulkCopyDemoMatchingColumns;")) { rsRowCount.next(); countStart = rsRowCount.getInt(1); System.out.println("Starting row count = " + countStart); } //  Get data from the source table as a ResultSet. try (ResultSet rsSourceData = stmt.executeQuery( "SELECT ProductID, Name, ProductNumber FROM Production.Product")) { // Set up the bulk copy object. // Note that when specifying the UseInternalTransaction // option, you cannot also use an external transaction. // Therefore, you must use the SQLServerBulkCopy construct that // requires a string for the connection, rather than an // existing Connection object. SQLServerBulkCopyOptions copyOptions = new SQLServerBulkCopyOptions(); copyOptions.setKeepIdentity(true); copyOptions.setBatchSize(10); copyOptions.setUseInternalTransaction(true); try (SQLServerBulkCopy bulkCopy = new SQLServerBulkCopy(connectionString)) { bulkCopy.setBulkCopyOptions(copyOptions); bulkCopy.setDestinationTableName("dbo.BulkCopyDemoMatchingColumns"); // Write from the source to the destination. // This should fail with a duplicate key error // after some of the batches have been copied. try { bulkCopy.writeToServer(rsSourceData); } catch (Exception e) { // Handle any errors that may have occurred. e.printStackTrace(); } } } // Perform a final count on the destination // table to see how many rows were added. try (ResultSet rsRowCount = stmt.executeQuery( "SELECT COUNT(*) FROM dbo.BulkCopyDemoMatchingColumns;")) { rsRowCount.next(); long countEnd = rsRowCount.getInt(1); System.out.println("Ending row count = " + countEnd); System.out.println((countEnd - countStart) + " rows were added."); } } } } catch (Exception e) { // Handle any errors that may have occurred. e.printStackTrace(); } } // To avoid storing the sourceConnection String in your code, // you can retrieve it from a configuration file. private static String GetConnectionString() { // Create a variable for the connection string. String connectionUrl = "jdbc:sqlserver://localhost:1433;" + "databaseName=AdventureWorks;user=UserName;password=*****"; return connectionUrl; } }  
```  
  
### Verwenden vorhandener Transaktionen  
 Sie können ein Verbindungsobjekt, für das Transaktionen aktiviert sind, als Parameter in einem SQLServerBulkCopy\-Konstruktor übergeben. In dieser Situation wird der Massenkopiervorgang in einer vorhandenen Transaktion ausgeführt, und es tritt keine Änderung am Transaktionsstatus ein \(d.h. für sie wird weder ein Commit noch ein Abbruch ausgeführt\). Dies macht es möglich, dass Anwendungen den Massenkopiervorgang zusammen mit anderen Datenbankvorgängen in einer Transaktion einschließen. Ob Sie einen Rollback des gesamten Massenkopiervorgangs durchführen müssen, weil ein Fehler auftritt, oder ob die Massenkopie im Rahmen eines größeren Prozesses ausgeführt werden soll, für den ein Rollback durchgeführt werden kann, Sie können den Rollback für das Verbindungsobjekt zu jedem beliebigen Zeitpunkt nach dem Massenkopiervorgang ausführen.  
  
 Die folgende Anwendung ähnelt dem ersten \(nicht transaktionalen\) Beispiel, mit einer Ausnahme: in diesem Beispiel ist der Massenkopiervorgang in einer größeren, externen Transaktion enthalten. Wenn der Fehler aufgrund des Primärschlüsselverstoßes auftritt, wird ein Rollback der gesamten Transaktion ausgeführt, und der Zieltabelle werden keine Zeilen hinzugefügt.  
  
> [!NOTE]  
>  Dieses Beispiel wird nur ausgeführt, wenn Sie die Arbeitstabellen zuvor wie in [Tabelleneinrichtung](../content/Using-Bulk-Copy-with-the-JDBC-Driver.md#BKMK_TableSetup) beschrieben erstellt haben. Dieser Code wird nur bereitgestellt, um die Syntax für die Verwendung von „SQLServerBulkCopy“ zu demonstrieren. Wenn sich die Quell\- und Zieltabellen in der gleichen SQL Server\-Instanz befinden, ist die Verwendung einer Transact\-SQL\-Anweisung „INSERT … SELECT“ zum Kopieren der Daten einfacher und schneller.  
  
```  
import java.sql.*; import com.microsoft.sqlserver.jdbc.SQLServerBulkCopy; import com.microsoft.sqlserver.jdbc.SQLServerBulkCopyOptions; public class Program { public static void main(String[] args) { String connectionString = GetConnectionString(); try { // Note: if you are not using try-with-resources statements (as here), // you must remember to call close() on any Connection, Statement, // ResultSet, and SQLServerBulkCopy objects that you create. // Open a sourceConnection to the AdventureWorks database. Class.forName("com.microsoft.sqlserver.jdbc.SQLServerDriver"); try (Connection sourceConnection = DriverManager.getConnection(connectionString)) { try (Statement stmt = sourceConnection.createStatement()) { //  Delete all from the destination table. stmt.executeUpdate("DELETE FROM dbo.BulkCopyDemoMatchingColumns"); //  Add a single row that will result in duplicate key //  when all rows from source are bulk copied. //  Note that this technique will only be successful in //  illustrating the point if a row with ProductID = 446 //  exists in the AdventureWorks Production.Products table. //  If you have made changes to the data in this table, change //  the SQL statement in the code to add a ProductID that //  does exist in your version of the Production.Products //  table. Choose any ProductID in the middle of the table //  (not first or last row) to best illustrate the result. stmt.executeUpdate("SET IDENTITY_INSERT dbo.BulkCopyDemoMatchingColumns ON;" + "INSERT INTO " + "dbo.BulkCopyDemoMatchingColumns " + "([ProductID], [Name] ,[ProductNumber]) " + "VALUES(446, 'Lock Nut 23','LN-3416');" + "SET IDENTITY_INSERT dbo.BulkCopyDemoMatchingColumns OFF"); // Perform an initial count on the destination table. long countStart = 0; try (ResultSet rsRowCount = stmt.executeQuery( "SELECT COUNT(*) FROM dbo.BulkCopyDemoMatchingColumns;")) { rsRowCount.next(); countStart = rsRowCount.getInt(1); System.out.println("Starting row count = " + countStart); } //  Get data from the source table as a ResultSet. try (ResultSet rsSourceData = stmt.executeQuery( "SELECT ProductID, Name, ProductNumber FROM Production.Product")) { // Set up the bulk copy object inside the transaction. try (Connection destinationConnection = DriverManager.getConnection(connectionString)) { destinationConnection.setAutoCommit(false); SQLServerBulkCopyOptions copyOptions = new SQLServerBulkCopyOptions(); copyOptions.setKeepIdentity(true); copyOptions.setBatchSize(10); try (SQLServerBulkCopy bulkCopy = new SQLServerBulkCopy(destinationConnection)) { bulkCopy.setBulkCopyOptions(copyOptions); bulkCopy.setDestinationTableName("dbo.BulkCopyDemoMatchingColumns"); // Write from the source to the destination. // This should fail with a duplicate key error. try { bulkCopy.writeToServer(rsSourceData); destinationConnection.commit(); } catch (Exception e) { // Handle any errors that may have occurred. e.printStackTrace(); destinationConnection.rollback(); } } } } // Perform a final count on the destination // table to see how many rows were added. try (ResultSet rsRowCount = stmt.executeQuery( "SELECT COUNT(*) FROM dbo.BulkCopyDemoMatchingColumns;")) { rsRowCount.next(); long countEnd = rsRowCount.getInt(1); System.out.println("Ending row count = " + countEnd); System.out.println((countEnd - countStart) + " rows were added."); } } } } catch (Exception e) { // Handle any errors that may have occurred. e.printStackTrace(); } } // To avoid storing the sourceConnection String in your code, // you can retrieve it from a configuration file. private static String GetConnectionString() { // Create a variable for the connection string. String connectionUrl = "jdbc:sqlserver://localhost:1433;" + "databaseName=AdventureWorks;user=UserName;password=*****"; return connectionUrl; } }  
  
```  
  
### Massenkopieren aus einer CSV\-Datei  
 Die folgende Anwendung zeigt das Laden von Daten mithilfe der Klasse „SQLServerBulkCopy“. In diesem Beispiel wird eine CSV\-Datei verwendet, um aus der Tabelle „Production.Product“ in der SQL Server AdventureWorks\-Datenbank exportierte Daten in eine ähnliche Tabelle in der gleichen Datenbank zu kopieren.  
  
> [!IMPORTANT]  
>  Dieses Beispiel wird nur ausgeführt, wenn Sie die Arbeitstabellen zuvor wie in [Tabelleneinrichtung](../content/Using-Bulk-Copy-with-the-JDBC-Driver.md#BKMK_TableSetup) beschrieben erstellt haben. Sie müssen darüber hinaus eine CSV\-Datei mit exportierten Daten aus der Tabelle „Production.Product“ erstellen; dies können Sie mit SSMS \(SQL Server Management Studio\) erledigen.  Wenn Sie nicht über SSMS verfügen, können Sie [Download SQL Server Management Studio](https://msdn.microsoft.com/library/mt238290.aspx) aufsuchen, um es herunterzuladen.  
  
1.  Öffnen Sie **SQL Server Management Studio**, und stellen Sie eine Verbindung mit dem SQL Server\-Computer mit der AdventureWorks\-Datenbank her.  
  
2.  Erweitern Sie die Datenbanken, klicken Sie mit der rechten Maustaste auf die AdventureWorks\-Datenbank, und wählen Sie **Aufgaben** und **Daten exportieren**… aus.  
  
3.  Wählen Sie als Datenquelle die **Datenquelle** aus, die Ihnen die Verbindung mit Ihrem SQL Server ermöglicht \(z. B. SQL Server Native Client 11.0\), überprüfen Sie die Konfiguration, und wählen Sie dann **Weiter** aus.  
  
4.  Wählen Sie als Ziel das **Flatfileziel** aus, und geben Sie einen **Dateinamen** mit einem Zielspeicherort wie etwa „C:\\Test\\TestBulkCSVExample.csv“ ein. Überprüfen Sie, ob das **Format** „Mit Trennzeichen“, der **Textqualifizierer** „Ohne“ ist, und aktivieren Sie **Spaltennamen in der ersten Datenzeile**. Wählen Sie dann **Weiter** aus.  
  
5.  Wählen Sie **Abfrage zum Angeben der zu übertragenden Daten schreiben** und dann **Weiter** aus.  Geben Sie für die **SQL\-Anweisung** SELECT ProductID, Name, ProductNumber FROM Production.Product und **Weiter** ein.  
  
6.  Überprüfen Sie die Konfiguration: Sie können das Zeilentrennzeichen als {CR}{LF} und das Spaltentrennzeichen als Komma {,} belassen.  Wählen Sie **Zuordnungen bearbeiten**… aus, und überprüfen Sie, ob der **Datentyp** für die einzelnen Spalten richtig ist \(z. B. Integer für ProductID und Unicode\-Zeichenfolge für die anderen\).  
  
7.  Überspringen Sie die weiteren Optionen bis zu **Fertig stellen**, und führen Sie den Exportvorgang aus.  
  
```  
  
import java.sql.*; import com.microsoft.sqlserver.jdbc.SQLServerBulkCSVFileRecord; import com.microsoft.sqlserver.jdbc.SQLServerBulkCopy; public class Program { public static void main(String[] args) { String connectionString = GetConnectionString(); SQLServerBulkCSVFileRecord fileRecord = null; try { // Get data from the source file by loading it into a class that implements ISQLServerBulkRecord. // Here we are using the SQLServerBulkCSVFileRecord implementation to import the example CSV file. fileRecord = new SQLServerBulkCSVFileRecord("C:\\Test\\TestBulkCSVExample.csv", true); // Set the metadata for each column to be copied. fileRecord.addColumnMetadata(1, null, java.sql.Types.INTEGER, 0, 0); fileRecord.addColumnMetadata(2, null, java.sql.Types.NVARCHAR, 50, 0); fileRecord.addColumnMetadata(3, null, java.sql.Types.NVARCHAR, 25, 0); // Open a destinationConnection to the AdventureWorks database. Class.forName("com.microsoft.sqlserver.jdbc.SQLServerDriver"); try (Connection destinationConnection = DriverManager.getConnection(connectionString)) { try (Statement stmt = destinationConnection.createStatement()) { // Perform an initial count on the destination table. long countStart = 0; try (ResultSet rsRowCount = stmt.executeQuery( "SELECT COUNT(*) FROM dbo.BulkCopyDemoMatchingColumns;")) { rsRowCount.next(); countStart = rsRowCount.getInt(1); System.out.println("Starting row count = " + countStart); } // Set up the bulk copy object. // Note that the column positions in the source // data reader match the column positions in // the destination table so there is no need to // map columns. try (SQLServerBulkCopy bulkCopy = new SQLServerBulkCopy(destinationConnection)) { bulkCopy.setDestinationTableName("dbo.BulkCopyDemoMatchingColumns"); try { // Write from the source to the destination. bulkCopy.writeToServer(fileRecord); } catch (Exception e) { // Handle any errors that may have occurred. e.printStackTrace(); } } // Perform a final count on the destination // table to see how many rows were added. try (ResultSet rsRowCount = stmt.executeQuery( "SELECT COUNT(*) FROM dbo.BulkCopyDemoMatchingColumns;")) { rsRowCount.next(); long countEnd = rsRowCount.getInt(1); System.out.println("Ending row count = " + countEnd); System.out.println((countEnd - countStart) + " rows were added."); } } } } catch (Exception e) { // Handle any errors that may have occurred. e.printStackTrace(); } finally { if (fileRecord != null) try { fileRecord.close(); } catch(Exception e) {} } } // To avoid storing the sourceConnection String in your code, // you can retrieve it from a configuration file. private static String GetConnectionString() { // Create a variable for the connection string. String connectionUrl = "jdbc:sqlserver://localhost:1433;" + "databaseName=AdventureWorks;user=UserName;password=*****"; return connectionUrl; } }  
  
```  
  
## Massenkopieren\-API für JDBC Driver  
  
### SQLServerBulkCopy  
 Damit können Sie effizient eine SQL Server\-Tabelle mit Massendaten aus einer anderen Quelle laden.  
  
 Microsoft SQL Server enthält ein beliebtes Befehlszeilen\-Hilfsprogramm namens bcp zum Verschieben von Daten aus einer Tabelle in eine andere, das auf einem einzelnen Server oder serverübergreifend ausgeführt werden kann. Die Klasse „SQLServerBulkCopy“ ermöglicht Ihnen das Erstellen von Codelösungen in Java, die eine ähnliche Funktionalität bereitstellen. Es gibt eine Reihe weiterer Verfahren, Daten in eine SQL\-Server\-Tabelle zu laden \(beispielsweise INSERT\-Anweisungen\), doch bietet „SQLServerBulkCopy“ ihnen gegenüber einen erheblichen Leistungsvorteil.  
  
 Die Klasse „SQLServerBulkCopy“ kann nur verwendet werden, um Daten in SQL Server\-Tabellen zu schreiben. Die Datenquelle ist aber nicht auf SQL Server beschränkt; jede beliebige Datenquelle kann verwendet werden, sofern die Daten mit einer Instanz von „ResultSet“ oder einer Implementierung von „ISQLServerBulkRecord“ gelesen werden können.  
  
|Konstruktor|Beschreibung|  
|-----------------|------------------|  
|SQLServerBulkCopy\(Connection\)|Initialisiert eine neue Instanz der Klasse „SQLServerBulkCopy“ mithilfe der angegebenen offenen Instanz von „SQLServerConnection“. Wenn für die Verbindung Transaktionen aktiviert sind, werden die Kopiervorgänge innerhalb der betreffenden Transaktion ausgeführt.|  
|SQLServerBulkCopy\(String\)|Initialisiert und öffnet basierend auf der übergebenen „connectionURL“ eine neue Instanz von „SQLServerConnection“. Der Konstruktor verwendet „SQLServerConnection“, um eine neue Instanz der Klasse „SQLServerBulkCopy“ zu initialisieren.|  
  
|Eigenschaft|Beschreibung|  
|-----------------|------------------|  
|DestinationTableName|Name der Zieltabelle auf dem Server.<br /><br /> Wenn „DestinationTableName“ beim Aufruf von „writeToServer“ nicht festgelegt ist, wird eine SQLServerException ausgelöst.<br /><br /> „DestinationTableName“ ist ein dreiteiliger Name \(\<database\>.\<owningschema\>.\<name\>\). Sie können den Tabellennamen mit seiner Datenbank und dem besitzenden Schema qualifizieren, wenn Sie das wünschen. Wenn im Tabellennamen jedoch ein Unterstrich \("\_"\) oder ein anderes Sonderzeichen vorkommt, müssen Sie den Namen in eckige Klammern einschließen. Weitere Informationen finden Sie in der SQL Server\-Onlinedokumentation unter "Bezeichner".|  
|ColumnMappings|Spaltenzuordnungen definieren die Beziehungen zwischen Spalten in der Datenquelle und Spalten im Ziel.<br /><br /> Wenn keine Zuordnungen definiert sind, werden die Spalten implizit auf der Grundlage ihrer Ordinalposition zugeordnet. Damit dies funktioniert, müssen Quell\- und Zielschema übereinstimmen. Ist dies nicht der Fall, wird eine Ausnahme ausgelöst.<br /><br /> Wenn die Zuordnung nicht leer ist, muss nicht jede in der Datenquelle vorhandene Spalte angegeben werden. Nicht zugeordnete Spalten werden ignoriert.<br /><br /> Sie können auf Quell\- und Zielspalten über den Namen oder die Ordnungszahl verweisen.|  
  
|Methode|Beschreibung|  
|-------------|------------------|  
|AddColumnMapping \(Int, Int\)|Fügt eine neue Spaltenzuordnung hinzu, und verwendet für die Angabe von Quell\- und Zielspalten Ordnungszahlen.|  
|AddColumnMapping \(Int, String\)|Fügt eine neue Spaltenzuordnung hinzu und verwendet für die Quellspalte eine Ordnungszahl und für die Zielspalte den Spaltennamen.|  
|addColumnMapping \(String, int\)|Fügt eine neue Spaltenzuordnung hinzu und verwendet einen Spaltennamen zum Beschreiben der Quellspalte und eine Ordnungszahl zum Angeben der Zielspalte.|  
|addColumnMapping \(String, String\)|Fügt eine neue Spaltenzuordnung hinzu, und verwendet für die Angabe von Quell\- und Zielspalten Spaltennamen.|  
|clearColumnMappings\(\)|Löscht den Inhalt der Spaltenzuordnungen.|  
|close\(\)|Schließt die SQLServerBulkCopy\-Instanz.|  
|getBulkCopyOptions\(\)|Ruft den aktuellen Satz von „SQLServerBulkCopyOptions“ ab.|  
|getDestinationTableName\(\)|Ruft den Namen der aktuellen Zieltabelle ab.|  
|setBulkCopyOptions\(SQLServerBulkCopyOptions\)|Aktualisiert das Verhalten der SQLServerBulkCopy\-Instanz gemäß den angegebenen Optionen.|  
|setDestinationTableName\(String\)|Legt den Namen der Zieltabelle fest.|  
|writeToServer\(ResultSet\)|Kopiert alle Zeilen im angegebenen ResultSet in eine durch die Eigenschaft „DestinationTableName“ des SQLServerBulkCopy\-Objekts angegebene Zieltabelle.|  
|writeToServer\(RowSet\)|Kopiert alle Zeilen im angegebenen RowSet in eine durch die Eigenschaft „DestinationTableName“ des SQLServerBulkCopy\-Objekts angegebene Zieltabelle.|  
|writeToServer\(ISQLServerBulkRecord\)|Kopiert alle Zeilen in der angegebenen ISQLServerBulkRecord\-Implementierung in eine durch die Eigenschaft „DestinationTableName“ des SQLServerBulkCopy\-Objekts angegebene Zieltabelle.|  
  
### SQLServerBulkCopyOptions  
 Eine Auflistung von Einstellungen, die steuern, wie sich die writeToServer\-Methoden in einer Instanz von „SQLServerBulkCopy“ verhalten.  
  
|Konstruktor|Beschreibung|  
|-----------------|------------------|  
|SQLServerBulkCopyOptions\(\)|Initialisiert eine neue Instanz der Klasse SQLServerBulkCopyOptions mit Standardwerten für alle Einstellungen.|  
  
 Für die folgenden Optionen sind Getter und Setter vorhanden:  
  
|Option|Beschreibung|Standardwert|  
|------------|------------------|------------------|  
|CheckConstraints|Überprüft Bedingungen während der Einfügung von Daten.|False – es werden keine Bedingungen überprüft.|  
|FireTriggers|Wenn der Wert angegeben wird, wird der Server veranlasst, die Einfügetrigger für die in die Datenbank eingefügten Zeilen auszulösen.|False – es werden keine Trigger ausgelöst|  
|KeepIdentity|Die Identitätswerte der Quelltabelle werden beibehalten.|False – die Identitätswerte werden vom Ziel zugewiesen|  
|KeepNulls|NULL\-Werte in der Zieltabelle werden beibehalten, unabhängig von der Einstellung für Standardwerte.|False – NULL\-Werte werden, falls anwendbar, durch Standardwerte ersetzt.|  
|TableLock|Für die Dauer des Massenimportvorgangs wird eine Sperre für Massenaktualisierung aktiviert.|False – es werden Sperren auf Zeilenebene verwendet.|  
|UseInternalTransaction|Wenn angegeben, wird jeder Batch des Massenkopiervorgangs innerhalb einer Transaktion verarbeitet. Wenn „SQLServerBulkCopy“ eine vorhandene Verbindung verwendet, \(wie im Konstruktor angegeben\), tritt eine SQLServerException auf.  Wenn „SQLServerBulkCopy“ eine dedizierte Verbindung erstellt hat, wird eine Transaktion aktiviert.|False – keine Transaktion|  
|Batchgröße|Die Anzahl der Zeilen pro Batch. Am Ende jedes Batches werden die im Batch enthaltenen Zeilen an den Server gesendet.<br /><br /> Ein Batch ist abgeschlossen, wenn die Anzahl „BatchSize“ Zeilen verarbeitet wurde oder keine weiteren Zeilen zum Senden an die Zieldatenquelle mehr vorhanden sind.  Wenn die SQLServerBulkCopy\-Instanz ohne aktive Option „UseInternalTransaction“ deklariert wurde, werden Zeilen zu jeweils „BatchSize“ zugleich an den Server gesendet, es wird jedoch keine transaktionsbezogene Aktion eingeleitet. Wenn „UseInternalTransaction“ aktiviert ist, wird jeder Batch Zeilen als separate Transaktion eingefügt.|0 – gibt an, dass jeder writeToServer\-Vorgang ein einzelner Batch ist.|  
|BulkCopyTimeout|Anzahl der Sekunden für den Abschluss des Vorgangs, bevor ein Timeout eintritt. Der Wert „0“ bedeutet keine Einschränkung; der Massenkopiervorgang wartet unbegrenzt.|60 Sekunden.|  
  
### ISQLServerBulkRecord  
 Die Schnittstelle „ISQLServerBulkRecord“ kann verwendet werden, um Klassen zu erstellen, die Daten aus jeder beliebigen Quelle \(wie etwa einer Datei\) einlesen und ermöglicht es einer SQLServerBulkCopy\-Instanz, ein Massenladen einer SQL Server\-Tabelle mit diesen Daten auszuführen.  
  
|Schnittstellenmethoden|Beschreibung|  
|----------------------------|------------------|  
|getColumnOrdinals\(\)|Ruft die Ordnungszahlen für jede der in diesem Datensatz enthaltenen Spalten ab.|  
|getColumnName\(int\)|Ruft den Namen der angegebenen Spalte ab.|  
|getColumnType\(int\)|Ruft den JDBC\-Datentyp der angegebenen Spalte ab.|  
|getPrecision\(int\)|Ruft die Genauigkeit für die angegebene Spalte ab.|  
|getRowData\(\)|Ruft die Daten für die aktuelle Zeile als Array von Objekten ab.<br /><br /> Jedes Objekt muss mit dem Java\-Sprachtyp übereinstimmen, der zur Darstellung des angegebenen JDBC\-Datentyps für die angegebene Spalte verwendet wird.  Weitere Informationen und die passenden Zuordnungen finden Sie unter „Grundlegendes zu den Datentypen in JDBC Driver“.|  
|getScale\(int\)|Ruft die Dezimalstellen für die angegebene Spalte ab.|  
|isAutoIncrement\(int\)|Zeigt an, ob es sich bei der Spalte um eine Identitätsspalte handelt.|  
|next\(\)|Springt zur nächsten Datenzeile.|  
  
### SQLServerBulkCSVFileRecord  
 Eine einfache Implementierung der ISQLServerBulkRecord\-Schnittstelle, die zum Einlesen der einfachen Java\-Datentypen aus einer Datei mit Trennzeichen verwendet werden kann, in der jede Zeile eine Datenzeile darstellt.  
  
 Hinweise zur Implementierung und Einschränkungen:  
  
1.  Die maximal in jeder vorhandenen Zeile zulässige Datenmenge ist durch den verfügbaren Arbeitsspeicher begrenzt, da die Daten zeilenweise gelesen werden.  
  
2.  Das Streaming großer Datentypen, wie etwa „varchar\(max\)“, „varbinary\(max\)“, „nvarchar\(max\)“, „sqlxml“, „ntext“ wird nicht unterstützt.  
  
3.  Das für die CSV\-Datei verwendete Trennzeichen darf an keiner Stelle innerhalb der Daten auftreten und muss ordnungsgemäß escaped werden, wenn es in den regulären Java\-Ausdrücken zu den eingeschränkten Zeichen gehört.  
  
4.  In der CSV\-Dateiimplementierung werden doppelte Anführungszeichen als Teil der Daten behandelt. Beispielsweise würde die Zeile Hallo,”Welt”,”Hallo,Welt” als aus vier Spalten mit den Werten Hallo, “Welt”, “Hallo und Welt” bestehend aufgefasst, wenn als Trennzeichen Komma verwendet wird.  
  
5.  Zeilenvorschubzeichen werden als Zeilenendzeichen verwendet und dürfen an keiner Stelle in den Daten auftreten.  
  
|Konstruktor|Beschreibung|  
|-----------------|------------------|  
|SQLServerBulkCSVFileRecord\(String, String, String, boolean\)|Initialisiert eine neue Instanz der SQLServerBulkCSVFileRecord\-Klasse, die jede Zeile in der zu analysierenden Datei „fileToParse“ mit dem angegebenen Trennzeichen und der angegebenen Codierung analysiert. Wenn „firstLineIsColumnNames“ auf „True“ festgelegt ist, wird der Inhalt der ersten Zeile der Datei als Spaltennamen analysiert.  Wenn die Codierung NULL ist, wird die Standardcodierung verwendet.|  
|SQLServerBulkCSVFileRecord\(String, String, boolean\)|Initialisiert eine neue Instanz der SQLServerBulkCSVFileRecord\-Klasse, die jede Zeile in der zu analysierenden Datei „fileToParse“ mit Komma als Trennzeichen und der angegebenen Codierung analysiert.|  
|SQLServerBulkCSVFileRecord\(String, boolean\)|Initialisiert eine neue Instanz der SQLServerBulkCSVFileRecord\-Klasse, die jede Zeile in der zu analysierenden Datei „fileToParse“ mit Komma als Trennzeichen und der Standardcodierung analysiert.|  
  
|Methode|Beschreibung|  
|-------------|------------------|  
|addColumnMetadata\(int, String, int, int, int\)|Fügt Metadaten für die angegebene Spalte in der Datei hinzu.|  
|close\(\)|Gibt alle dem Dateileser zugeordneten Ressourcen frei.|  
|setTimestampWithTimezoneFormat\(DateTimeFormatter\)|Legt das Format für die Analyse von Zeitstempeldaten aus der Datei auf „java.sql.Types.TIMESTAMP\_WITH\_TIMEZONE“ fest.|  
|setTimeWithTimezoneFormat\(DateTimeFormatter\)|Legt das Format für die Analyse von Uhrzeitdaten aus der Datei auf „java.sql.Types.TIME\_WITH\_TIMEZONE“ fest.|  
  
## Siehe auch  
 [Übersicht über den JDBC-Treiber](../content/Overview-of-the-JDBC-Driver.md)  
  
  