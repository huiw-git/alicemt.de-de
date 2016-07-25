---
title: "Verbindungs-URL - Beispiel"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 96fabc42-59d1-4cc0-93c5-db00cbe55e95
caps.latest.revision: 28
caps.handback.revision: 22
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
# Verbindungs-URL - Beispiel
  Diese Beispielanwendung für [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] veranschaulicht, wie unter Verwendung einer Verbindungs\-URL eine Verbindung mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank hergestellt wird. Darüber hinaus wird gezeigt, wie Daten mithilfe einer SQL\-Anweisung aus einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank abgerufen werden.  
  
 Die Codedatei für dieses Beispiel heißt "connectURL.java" und befindet sich im folgenden Pfad:  
  
 \<*Installationsverzeichnis*\>\\sqljdbc\_\<*Version*\>\\\<*Sprache*\>\\help\\samples\\connections  
  
## Anforderungen  
 Wenn Sie diese Beispielanwendung ausführen möchten, müssen Sie die Datei **sqljdbc.jar** oder **sqljdbc4.jar** in den Klassenpfad aufnehmen. Wenn im Klassenpfad kein Eintrag für **sqljdbc.jar** oder **sqljdbc4.jar** vorhanden ist, löst die Beispielanwendung die allgemeine Ausnahme "Klasse nicht gefunden" aus. Sie benötigen darüber hinaus Zugriff auf die [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank. Weitere Informationen zum Festlegen des Klassenpfads finden Sie unter [Verwenden des JDBC-Treibers](../content/Using-the-JDBC-Driver.md).  
  
> [!NOTE]  
>  [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] enthält die Klassenbibliotheksdateien "sqljdbc.jar" und "sqljdbc4.jar" für die jeweilige Verwendung mit den bevorzugten JRE \(Java Runtime Environment\)\-Einstellungen. Weitere Informationen zum Auswählen der richtigen JAR\-Datei finden Sie unter [Systemanforderungen für den JDBC-Treiber](../content/System-Requirements-for-the-JDBC-Driver.md).  
  
## Beispiel  
 Der folgende Beispielcode legt zunächst verschiedene Verbindungseigenschaften fest. Anschließend wird die getConnection\-Methode der DriverManager\-Klasse aufgerufen, um ein [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt zurückzugeben.  
  
 Danach wird mithilfe der [createStatement](../content/createStatement-Method--SQLServerConnection-.md)\-Methode des SQLServerConnection\-Objekts ein [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt erstellt. Anschließend wird die [executeQuery](../content/executeQuery-Method--SQLServerStatement-.md)\-Methode aufgerufen, um die SQL\-Anweisung auszuführen.  
  
 Schließlich wird das [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt, das von der executeQuery\-Methode zurückgegeben wurde, verwendet, um die von der SQL\-Anweisung zurückgegebenen Ergebnisse zu durchlaufen.  
  
```  
import java.sql.*;  
  
public class connectURL {  
  
   public static void main(String[] args) {  
  
      // Create a variable for the connection string.  
      String connectionUrl = "jdbc:sqlserver://localhost:1433;" +  
         "databaseName=AdventureWorks;user=UserName;password=*****";  
  
      // Declare the JDBC objects.  
      Connection con = null;  
      Statement stmt = null;  
      ResultSet rs = null;  
  
      try {  
         // Establish the connection.  
         Class.forName("com.microsoft.sqlserver.jdbc.SQLServerDriver");  
         con = DriverManager.getConnection(connectionUrl);  
  
         // Create and execute an SQL statement that returns some data.  
         String SQL = "SELECT TOP 10 * FROM Person.Contact";  
         stmt = con.createStatement();  
         rs = stmt.executeQuery(SQL);  
  
         // Iterate through the data in the result set and display it.  
         while (rs.next()) {  
            System.out.println(rs.getString(4) + " " + rs.getString(6));  
         }  
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
}  
```  
  
## Siehe auch  
 [Verbinden und Abrufen von Daten](../content/Connecting-and-Retrieving-Data.md)  
  
  