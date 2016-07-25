---
title: "Beispiel f&#252;r Datenquellen"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b4a933ee-f2c6-4e0d-a96d-6dd061abf759
caps.latest.revision: 25
caps.handback.revision: 19
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
# Beispiel f&#252;r Datenquellen
  Diese Beispielanwendung für [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] veranschaulicht, wie unter Verwendung eines Datenquellenobjekts eine Verbindung mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank hergestellt wird. Darüber hinaus wird gezeigt, wie Daten mithilfe einer gespeicherten Prozedur aus einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank abgerufen werden.  
  
 Die Codedatei für dieses Beispiel heißt "connectDS.java" und befindet sich im folgenden Pfad:  
  
 \<*Installationsverzeichnis*\>\\sqljdbc\_\<*Version*\>\\\<*Sprache*\>\\help\\samples\\connections  
  
## Anforderungen  
 Wenn Sie diese Beispielanwendung ausführen möchten, müssen Sie die Datei **sqljdbc.jar** oder **sqljdbc4.jar** in den Klassenpfad aufnehmen. Wenn im Klassenpfad kein Eintrag für **sqljdbc.jar** oder **sqljdbc4.jar** vorhanden ist, löst die Beispielanwendung die allgemeine Ausnahme "Klasse nicht gefunden" aus. Sie benötigen darüber hinaus Zugriff auf die [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank. Weitere Informationen zum Festlegen des Klassenpfads finden Sie unter [Verwenden des JDBC-Treibers](../content/Using-the-JDBC-Driver.md).  
  
> [!NOTE]  
>  [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] enthält die Klassenbibliotheksdateien "sqljdbc.jar" und "sqljdbc4.jar" für die jeweilige Verwendung mit den bevorzugten JRE \(Java Runtime Environment\)\-Einstellungen. Weitere Informationen zum Auswählen der richtigen JAR\-Datei finden Sie unter [Systemanforderungen für den JDBC-Treiber](../content/System-Requirements-for-the-JDBC-Driver.md).  
  
## Beispiel  
 Der folgende Beispielcode legt mit den Festlegungsmethoden des [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Objekts verschiedene Verbindungseigenschaften fest. Anschließend wird die [getConnection](../content/getConnection-Method--SQLServerDataSource-.md)\-Methode des SQLServerDataSource\-Objekts aufgerufen, um ein [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Objekt zurückzugeben.  
  
 Danach wird mithilfe der [prepareCall](../content/prepareCall-Method--SQLServerConnection-.md)\-Methode des SQLServerConnection\-Objekts ein [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Objekt erstellt. Anschließend wird die [executeQuery](../content/executeQuery-Method--SQLServerPreparedStatement-.md)\-Methode aufgerufen, um die gespeicherte Prozedur auszuführen.  
  
 Abschließend wird das [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt, das von der executeQuery\-Methode zurückgegeben wurde, verwendet, um die von der gespeicherten Prozedur zurückgegebenen Ergebnisse zu durchlaufen.  
  
```  
import java.sql.*;  
import com.microsoft.sqlserver.jdbc.*;  
  
public class connectDS {  
  
   public static void main(String[] args) {  
  
      // Declare the JDBC objects.  
      Connection con = null;  
      CallableStatement cstmt = null;  
      ResultSet rs = null;  
  
      try {  
         // Establish the connection.   
         SQLServerDataSource ds = new SQLServerDataSource();  
         ds.setUser("UserName");  
         ds.setPassword("*****");  
         ds.setServerName("localhost");  
         ds.setPortNumber(1433);   
         ds.setDatabaseName("AdventureWorks");  
         con = ds.getConnection();  
  
         // Execute a stored procedure that returns some data.  
         cstmt = con.prepareCall("{call dbo.uspGetEmployeeManagers(?)}");  
         cstmt.setInt(1, 50);  
         rs = cstmt.executeQuery();  
  
         // Iterate through the data in the result set and display it.  
         while (rs.next()) {  
            System.out.println("EMPLOYEE: " + rs.getString("LastName") +   
               ", " + rs.getString("FirstName"));  
            System.out.println("MANAGER: " + rs.getString("ManagerLastName") +   
               ", " + rs.getString("ManagerFirstName"));  
            System.out.println();  
         }  
      }  
  
      // Handle any errors that may have occurred.  
      catch (Exception e) {  
         e.printStackTrace();  
      }  
      finally {  
         if (rs != null) try { rs.close(); } catch(Exception e) {}  
         if (cstmt != null) try { cstmt.close(); } catch(Exception e) {}  
         if (con != null) try { con.close(); } catch(Exception e) {}  
         System.exit(1);  
      }  
   }  
}  
```  
  
## Siehe auch  
 [Verbinden und Abrufen von Daten](../content/Connecting-and-Retrieving-Data.md)  
  
  