---
title: "Verwenden von gespeicherten Prozeduren mit Ausgabeparametern"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1c006f27-7e99-43d5-974c-7b782659290c
caps.latest.revision: 29
caps.handback.revision: 26
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
# Verwenden von gespeicherten Prozeduren mit Ausgabeparametern
  Eine aufrufbare gespeicherte [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Prozedur gibt mindestens einen OUT\-Parameter zurück, mit dem die gespeicherte Prozedur Daten an die aufrufende Anwendung zurückgibt. [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] enthält die [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Klasse, mit der Sie diese Art von gespeicherter Prozedur aufrufen und die zurückgegebenen Daten verarbeiten können.  
  
 Wenn Sie diese Art von gespeicherter Prozedur mit dem JDBC\-Treiber aufrufen, müssen Sie die  `call` \-SQL\-Escapesequenz zusammen mit der [prepareCall](../content/prepareCall-Method--SQLServerConnection-.md)\-Methode der [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Klasse verwenden. Die Syntax für die `call`\-Escapesequenz mit OUT\-Parameter lautet wie folgt:  
  
 `{call procedure-name[([parameter][,[parameter]]...)]}`  
  
> [!NOTE]  
>  Weitere Informationen zu SQL\-Escapesequenzen finden Sie unter [Verwenden von SQL-Escapesequenzen](../content/Using-SQL-Escape-Sequences.md).  
  
 Geben Sie die OUT\-Parameter beim Erstellen der `call` \-Escapesequenz mit dem Fragezeichen \(?\) an. das als Platzhalter für die Parameterwerte fungiert, die von der gespeicherten Prozedur zurückgegeben werden. Um einen Wert für einen OUT\-Parameter anzugeben, müssen Sie vor dem Ausführen der gespeicherten Prozedur den Typ der einzelnen Parameter mit der [registerOutParameter](../content/registerOutParameter-Method--SQLServerCallableStatement-.md)\-Methode der SQLServerCallableStatement\-Klasse angeben.  
  
 Bei dem Wert, den Sie für den OUT\-Parameter in der registerOutParameter\-Methode angeben, muss es sich um einen der in **java.sql.Types** enthaltenen JDBC\-Datentypen handeln, der wiederum einem der systemeigenen [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentypen zugeordnet wird. Weitere Informationen zu den JDBC\- und [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentypen finden Sie unter [Grundlegendes zu den Datentypen in JDBC Driver](../content/Understanding-the-JDBC-Driver-Data-Types.md).  
  
 Wenn Sie an die registerOutParameter\-Methode einen Wert für einen OUT\-Parameter übergeben, müssen Sie nicht nur den für den Parameter zu verwendenden Datentyp angeben, sondern auch die ordinale Position des Parameters oder den Namen des Parameters der gespeicherten Prozedur. Wenn die gespeicherte Prozedur beispielsweise einen einzigen OUT\-Parameter enthält, ist der Ordinalwert 1. Wenn die gespeicherte Prozedur zwei Parameter enthält, ist der erste Ordinalwert 1 und der zweite Ordinalwert 2.  
  
> [!NOTE]  
>  Die Verwendung der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentypen CURSOR, SQLVARIANT, TABLE und TIMESTAMP für OUT\-Parameter wird vom JDBC\-Treiber nicht unterstützt.  
  
 Erstellen Sie als Beispiel die folgende Prozedur in der [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank:  
  
```  
CREATE PROCEDURE GetImmediateManager  
   @employeeID INT,  
   @managerID INT OUTPUT  
AS  
BEGIN  
   SELECT @managerID = ManagerID   
   FROM HumanResources.Employee   
   WHERE EmployeeID = @employeeID  
END  
```  
  
 Diese gespeicherte Prozedur gibt abhängig vom angegebenen IN\-Parameter "employeeID" \(ein integer\-Wert\) einen einzigen OUT\-Parameter "managerID" zurück \(ebenfalls ein integer\-Wert\). Bei dem im OUT\-Parameter zurückgegebenen Wert handelt es sich um die auf "EmployeeID" basierende "ManagerID", die in der Tabelle "HumanResources.Employee" enthalten ist.  
  
 Im folgenden Beispiel werden eine offene Verbindung zur [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank an die Funktion übergeben und die gespeicherte Prozedur "GetImmediateManager" mit der [execute](../content/execute-Method--SQLServerStatement-.md)\-Methode aufgerufen:  
  
```  
public static void executeStoredProcedure(Connection con) {  
   try {  
      CallableStatement cstmt = con.prepareCall("{call dbo.GetImmediateManager(?, ?)}");  
      cstmt.setInt(1, 5);  
      cstmt.registerOutParameter(2, java.sql.Types.INTEGER);  
      cstmt.execute();  
      System.out.println("MANAGER ID: " + cstmt.getInt(2));  
   }  
   catch (Exception e) {  
      e.printStackTrace();  
   }  
}  
```  
  
 In diesem Beispiel werden die Ordnungspositionen verwendet, um die Parameter zu identifizieren. Alternativ können Sie einen Parameter mit seinem Namen anstelle der Ordnungsposition identifizieren. Im folgenden Codebeispiel wird das vorhergehende Beispiel geändert, um die Verwendung von benannten Parametern in einer Java\-Anwendung zu veranschaulichen. Beachten Sie, dass die Parameternamen den Parameternamen in der Definition der gespeicherten Prozedur entsprechen:  
  
```  
public static void executeStoredProcedure(Connection con) {  
   try {  
      CallableStatement cstmt = con.prepareCall("{call dbo.GetImmediateManager(?, ?)}");  
      cstmt.setInt("employeeID", 5);  
      cstmt.registerOutParameter("managerID", java.sql.Types.INTEGER);  
      cstmt.execute();  
      System.out.println("MANAGER ID: " + cstmt.getInt("managerID"));  
      cstmt.close();  
   }  
   catch (Exception e) {  
      e.printStackTrace();  
   }  
```  
  
 }  
  
> [!NOTE]  
>  In diesen Beispielen wird die execute\-Methode der SQLServerCallableStatement\-Klasse verwendet, um die gespeicherte Prozedur auszuführen. da von der gespeicherten Prozedur nicht auch ein Resultset zurückgegeben wurde. Andernfalls müsste die [executeQuery](../content/executeQuery-Method--SQLServerStatement-.md)\-Methode verwendet werden.  
  
 Gespeicherte Prozeduren können Updatezählungen und mehrere Resultsets zurückgeben. [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] folgt der JDBC 3.0\-Spezifikation, der zufolge mehrere Resultsets und Updatezählungen abgerufen werden müssen, bevor die OUT\-Parameter abgerufen werden. Dies bedeutet, dass die Anwendung alle ResultSet\-Objekte und Updatezählungen abrufen sollte, bevor die OUT\-Parameter mit den CallableStatement.getter\-Methoden abgerufen werden. Andernfalls gehen die noch nicht abgerufenen ResultSet\-Objekte und Updatezählungen verloren, wenn die OUT\-Parameter abgerufen werden. Weitere Informationen zu Updatezählungen und mehreren Resultsets finden Sie unter [Verwenden von gespeicherten Prozeduren mit einer Updatezählung](../content/Using-a-Stored-Procedure-with-an-Update-Count.md) und [Verwenden von mehreren Resultsets](../content/Using-Multiple-Result-Sets.md)  
  
## Siehe auch  
 [Verwenden von Anweisungen mit gespeicherten Prozeduren](../content/Using-Statements-with-Stored-Procedures.md)  
  
  