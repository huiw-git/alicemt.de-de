---
title: "Abrufen von Resultsetdaten - Beispiel"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1b190c36-3d38-49a2-8599-612329675851
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
# Abrufen von Resultsetdaten - Beispiel
  Diese Beispielanwendung für [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] veranschaulicht, wie Daten aus einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank abgerufen und anschließend angezeigt werden.  
  
 Die Codedatei für dieses Beispiel heißt "retrieveRS.java" und befindet sich im folgenden Pfad:  
  
 \<*Installationsverzeichnis*\>\\sqljdbc\_\<*Version*\>\\\<*Sprache*\>\\help\\samples\\resultsets  
  
## Anforderungen  
 Wenn Sie diese Beispielanwendung ausführen möchten, müssen Sie die Datei **sqljdbc.jar** oder **sqljdbc4.jar** in den Klassenpfad aufnehmen. Wenn im Klassenpfad kein Eintrag für **sqljdbc.jar** oder **sqljdbc4.jar** vorhanden ist, löst die Beispielanwendung die allgemeine Ausnahme "Klasse nicht gefunden" aus. Sie benötigen darüber hinaus Zugriff auf die [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank. Weitere Informationen zum Festlegen des Klassenpfads finden Sie unter [Verwenden des JDBC-Treibers](../content/Using-the-JDBC-Driver.md).  
  
> [!NOTE]  
>  [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] enthält die Klassenbibliotheksdateien "sqljdbc.jar" und "sqljdbc4.jar" für die jeweilige Verwendung mit den bevorzugten JRE \(Java Runtime Environment\)\-Einstellungen. Weitere Informationen zum Auswählen der richtigen JAR\-Datei finden Sie unter [Systemanforderungen für den JDBC-Treiber](../content/System-Requirements-for-the-JDBC-Driver.md).  
  
## Beispiel  
 Im folgenden Beispielcode wird eine Verbindung mit der [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank hergestellt. Anschließend wird eine SQL\-Anweisung mit dem [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt verwendet. Die SQL\-Anweisung wird ausgeführt, und die zurückgegebenen Daten werden in ein [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt eingefügt.  
  
 Danach ruft der Beispielcode die benutzerdefinierte displayRow\-Methode auf, um die im Resultset enthaltenen Datenzeilen zu durchlaufen. Mithilfe der [getString](../content/getString-Method--SQLServerResultSet-.md)\-Methode werden einige enthaltene Daten angezeigt.  
  
```  
import java.sql.*;  
  
public class retrieveRS {  
  
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
  
         // Create and execute an SQL statement that returns a  
         // set of data and then display it.  
         String SQL = "SELECT * FROM Production.Product;";  
         stmt = con.createStatement();  
         rs = stmt.executeQuery(SQL);  
         displayRow("PRODUCTS", rs);  
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
  
   private static void displayRow(String title, ResultSet rs) {  
      try {  
         System.out.println(title);  
         while (rs.next()) {  
            System.out.println(rs.getString("ProductNumber") + " : " + rs.getString("Name"));  
         }  
      } catch (Exception e) {  
         e.printStackTrace();  
      }  
   }  
}  
```  
  
## Siehe auch  
 [Arbeiten mit Resultsets](../content/Working-with-Result-Sets.md)  
  
  