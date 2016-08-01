---
title: "Verwenden von gespeicherten Prozeduren mit Eingabeparametern"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8f491b70-7d1b-42bd-964f-9a8b86af5eaa
caps.latest.revision: 21
caps.handback.revision: 18
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
# Verwenden von gespeicherten Prozeduren mit Eingabeparametern
  Eine aufrufbare gespeicherte [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Prozedur enthält mindestens einen IN\-Parameter, über den Daten an die gespeicherte Prozedur übergeben werden können. [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] enthält die [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\-Klasse, mit der Sie diese Art von gespeicherter Prozedur aufrufen und die zurückgegebenen Daten verarbeiten können.  
  
 Wenn Sie eine gespeicherte Prozedur mit IN\-Parametern mit dem JDBC\-Treiber aufrufen, müssen Sie die  `call` \-SQL\-Escapesequenz zusammen mit der [prepareCall](../content/prepareCall-Method--SQLServerConnection-.md)\-Methode der [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Klasse verwenden. Die Syntax für die  `call` \-Escapesequenz mit IN\-Parameter lautet wie folgt:  
  
 `{call procedure-name[([parameter][,[parameter]]...)]}`  
  
> [!NOTE]  
>  Weitere Informationen zu SQL\-Escapesequenzen finden Sie unter [Verwenden von SQL-Escapesequenzen](../content/Using-SQL-Escape-Sequences.md).  
  
 Geben Sie die IN\-Parameter beim Erstellen der  `call` \-Escapesequenz mit dem Fragezeichen \(?\) an. das als Platzhalter für die Parameterwerte fungiert, die an die gespeicherte Prozedur übergeben werden. Mit den Festlegungsmethoden der SQLServerPreparedStatement\-Klasse können Sie für einen Parameter einen Wert angeben. Die verwendbare Festlegungsmethode hängt vom Datentyp des IN\-Parameters ab.  
  
 Wenn Sie einen Wert an die Festlegungsmethode übergeben, müssen Sie nicht nur den Wert angeben, der im Parameter verwendet wird, sondern auch die ordinale Position des Parameters in der gespeicherten Prozedur. Wenn die gespeicherte Prozedur beispielsweise einen einzigen IN\-Parameter enthält, ist der Ordinalwert "1". Wenn die gespeicherte Prozedur zwei Parameter enthält, ist der erste Ordinalwert "1" und der zweite Ordinalwert "2".  
  
 Ein Beispiel für den Aufruf einer gespeicherten Prozedur mit einem IN\-Parameter enthält die gespeicherte Prozedur "uspGetEmployeeManagers" in der [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank. Diese gespeicherte Prozedur übernimmt einen einzelnen Eingabeparameter mit dem Namen "EmployeeID" \(integer\-Wert\) und gibt abhängig von der angegebenen "EmployeeID" eine rekursive Liste der Mitarbeiter und deren Vorgesetzten zurück. Der Java\-Code für den Aufruf dieser gespeicherten Prozedur sieht folgendermaßen aus:  
  
```  
public static void executeSprocInParams(Connection con) {  
   try {  
      PreparedStatement pstmt = con.prepareStatement("{call dbo.uspGetEmployeeManagers(?)}");  
      pstmt.setInt(1, 50);  
      ResultSet rs = pstmt.executeQuery();  
  
      while (rs.next()) {  
         System.out.println("EMPLOYEE:");  
         System.out.println(rs.getString("LastName") + ", " + rs.getString("FirstName"));  
         System.out.println("MANAGER:");  
         System.out.println(rs.getString("ManagerLastName") + ", " + rs.getString("ManagerFirstName"));  
         System.out.println();  
      }  
      rs.close();  
      pstmt.close();  
   }  
  
   catch (Exception e) {  
      e.printStackTrace();  
    }  
}  
```  
  
## Siehe auch  
 [Verwenden von Anweisungen mit gespeicherten Prozeduren](../content/Using-Statements-with-Stored-Procedures.md)  
  
  