---
title: "Zwischenspeichern von Resultsetdaten - Beispiel"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 13a95ebb-996c-4713-a1bd-5834fe22a334
caps.latest.revision: 20
caps.handback.revision: 14
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
# Zwischenspeichern von Resultsetdaten - Beispiel
  Diese Beispielanwendung für [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] veranschaulicht, wie umfangreiche Daten aus einer Datenbank abgerufen werden und mithilfe der [setFetchSize](../content/setFetchSize-Method--SQLServerResultSet-.md)\-Methode des [SQLServerResultSet](../content/SQLServerResultSet-Class.md) \-Objekts die Anzahl der Datenzeilen gesteuert wird, die im Client zwischengespeichert werden.  
  
> [!NOTE]  
>  Die Einschränkung der im Client zwischengespeicherten Zeilen ist nicht mit der Einschränkung der Gesamtanzahl von Zeilen identisch, die ein Resultset enthalten kann. Um die Gesamtanzahl der in einem Resultset enthaltenen Zeilen zu steuern, verwenden Sie die [setMaxRows](../content/setMaxRows-Method--SQLServerStatement-.md)\-Methode des [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekts, das von [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\- und [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Objekten geerbt wird.  
  
 Um die Anzahl der im Client zwischengespeicherten Zeilen zu beschränken, müssen Sie bei der Erstellung eines der Statement\-Objekte zuerst einen serverseitigen Cursor verwenden, indem Sie ausdrücklich den Cursortyp angeben, der beim Erstellen des Statement\-Objekts verwendet werden soll. Der JDBC\-Treiber enthält beispielsweise den Cursortyp TYPE\_SS\_SERVER\_CURSOR\_FORWARD\_ONLY \(ein schneller schreibgeschützter serverseitiger Vorwärtscursor für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbanken\).  
  
> [!NOTE]  
>  Alternativ zum SQL Server\-spezifischen Cursortyp kann die selectMethod\-Verbindungszeichenfolgeneigenschaft verwendet werden, indem deren Wert auf "cursor" festgelegt wird. Weitere Informationen zu den vom JDBC\-Treiber unterstützten Cursortypen finden Sie unter [Grundlegendes zu Cursortypen](../content/Understanding-Cursor-Types.md).  
  
 Nachdem die im Statement\-Objekt enthaltene Abfrage ausgeführt und die Daten als Resultset an den Client zurückgegeben wurden, können Sie die setFetchSize\-Methode aufrufen und den aus der Datenbank abgerufenen Umfang der Daten steuern. Wenn eine Tabelle beispielsweise 100 Datenzeilen enthält und die Abrufgröße auf 10 festgelegt wird, werden im Client jeweils nur immer 10 Datenzeilen zwischengespeichert. Obwohl dadurch die Verarbeitungsgeschwindigkeit der Daten sinkt, ist auf dem Client weniger Speicher erforderlich, was insbesondere dann von Nutzen sein kann, wenn umfangreiche Daten verarbeitet werden müssen.  
  
 Die Codedatei für dieses Beispiel heißt "cacheRS.java" und befindet sich im folgenden Pfad:  
  
 \<*Installationsverzeichnis*\>\\sqljdbc\_\<*Version*\>\\\<*Sprache*\>\\help\\samples\\resultsets  
  
## Anforderungen  
 Wenn Sie diese Beispielanwendung ausführen möchten, müssen Sie die Datei **sqljdbc.jar** oder **sqljdbc4.jar** in den Klassenpfad aufnehmen. Wenn im Klassenpfad kein Eintrag für **sqljdbc.jar** oder **sqljdbc4.jar** vorhanden ist, löst die Beispielanwendung die allgemeine Ausnahme "Klasse nicht gefunden" aus. Sie benötigen darüber hinaus Zugriff auf die [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank. Weitere Informationen zum Festlegen des Klassenpfads finden Sie unter [Verwenden des JDBC-Treibers](../content/Using-the-JDBC-Driver.md).  
  
> [!NOTE]  
>  [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] enthält die Klassenbibliotheksdateien "sqljdbc.jar" und "sqljdbc4.jar" für die jeweilige Verwendung mit den bevorzugten JRE \(Java Runtime Environment\)\-Einstellungen. Weitere Informationen zum Auswählen der richtigen JAR\-Datei finden Sie unter [Systemanforderungen für den JDBC-Treiber](../content/System-Requirements-for-the-JDBC-Driver.md).  
  
## Beispiel  
 Im folgenden Beispielcode wird eine Verbindung mit der [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank hergestellt. Anschließend wird eine SQL\-Anweisung mit dem [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt verwendet und der serverseitige Cursortyp angegeben. Die SQL\-Anweisung wird ausgeführt, und die zurückgegebenen Daten werden in ein SQLServerResultSet\-Objekt eingefügt.  
  
 Danach wird die benutzerdefinierte timerTest\-Methode aufgerufen, wobei die zu verwendende Abrufgröße und das Resultset als Argumente übergeben werden. Die timerTest\-Methode legt dann die Abrufgröße des Resultsets mithilfe der setFetchSize\-Methode sowie die Startzeit des Tests fest. Anschließend wird das Resultset mit einer `While`\-Schleife durchlaufen. Unmittelbar, nachdem die `While`\-Schleife verlassen wurde, wird die Beendigungszeit des Tests festgelegt. Anschließend wird das Testergebnis einschließlich Abrufgröße, der Anzahl verarbeiteter Zeilen und der Zeit für die Testausführung angezeigt.  
  
```  
import java.sql.*;  
import com.microsoft.sqlserver.jdbc.SQLServerResultSet;  
  
public class cacheRS {  
  
   public static void main(String[] args) {  
  
      // Create a variable for the connection string.  
      String connectionUrl = "jdbc:sqlserver://localhost:1433;" +  
            "databaseName=AdventureWorks;integratedSecurity=true;";  
  
      // Declare the JDBC objects.  
      Connection con = null;  
      Statement stmt = null;  
      ResultSet rs = null;  
  
      try {  
  
         // Establish the connection.  
         Class.forName("com.microsoft.sqlserver.jdbc.SQLServerDriver");  
         con = DriverManager.getConnection(connectionUrl);  
  
         // Create and execute an SQL statement that returns a large  
         // set of data and then display it.  
         String SQL = "SELECT * FROM Sales.SalesOrderDetail;";  
         stmt = con.createStatement(SQLServerResultSet.TYPE_SS_SERVER_CURSOR_FORWARD_ONLY, +  
               SQLServerResultSet.CONCUR_READ_ONLY);  
  
         // Perform a fetch for every row in the result set.  
         rs = stmt.executeQuery(SQL);  
         timerTest(1, rs);  
         rs.close();  
  
         // Perform a fetch for every tenth row in the result set.  
         rs = stmt.executeQuery(SQL);  
         timerTest(10, rs);  
         rs.close();  
  
         // Perform a fetch for every 100th row in the result set.  
         rs = stmt.executeQuery(SQL);  
         timerTest(100, rs);  
         rs.close();  
  
         // Perform a fetch for every 1000th row in the result set.  
         rs = stmt.executeQuery(SQL);  
         timerTest(1000, rs);  
         rs.close();  
  
         // Perform a fetch for every 128th row (the default) in the result set.  
         rs = stmt.executeQuery(SQL);  
         timerTest(0, rs);  
         rs.close();  
      }  
  
      // Handle any errors that may have occurred.  
      catch (Exception e) {  
         e.printStackTrace();  
      }  
  
      finally {  
         if (rs != null) try { rs.close(); } catch(Exception e) {}  
         if (stmt != null) try { stmt.close(); } catch(Exception e) {}  
         if (con != null) try { con.close(); } catch(Exception e) {}  
      }  
   }  
  
   private static void timerTest(int fetchSize, ResultSet rs) {  
      try {  
  
         // Declare the variables for tracking the row count and elapsed time.  
         int rowCount = 0;  
         long startTime = 0;  
         long stopTime = 0;  
         long runTime = 0;  
  
         // Set the fetch size then iterate through the result set to  
         // cache the data locally.  
         rs.setFetchSize(fetchSize);  
         startTime = System.currentTimeMillis();  
         while (rs.next()) {  
            rowCount++;  
         }  
         stopTime = System.currentTimeMillis();  
         runTime = stopTime - startTime;  
  
         // Display the results of the timer test.  
         System.out.println("FETCH SIZE: " + rs.getFetchSize());  
         System.out.println("ROWS PROCESSED: " + rowCount);  
         System.out.println("TIME TO EXECUTE: " + runTime);  
         System.out.println();  
  
      } catch (Exception e) {  
         e.printStackTrace();  
      }  
   }  
}  
```  
  
## Siehe auch  
 [Arbeiten mit Resultsets](../content/Working-with-Result-Sets.md)  
  
  