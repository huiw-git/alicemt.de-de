---
title: "getTablePrivileges-Methode (SQLServerDatabaseMetaData)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLServerDatabaseMetaData.getTablePrivileges
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 0610d667-a16d-4201-a14b-0a40048911e1
caps.latest.revision: 14
caps.handback.revision: 11
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
# getTablePrivileges-Methode (SQLServerDatabaseMetaData)
    
## getTablePrivileges\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft eine Beschreibung der Zugriffsrechte für die einzelnen Tabellen ab, die im angegebenen Katalog, Schema oder Tabellennamenmuster verfügbar sind.  
  
## Syntax  
  
```  
  
public java.sql.ResultSet getTablePrivileges(java.lang.String catalog,  
                                             java.lang.String schema,  
                                             java.lang.String table)  
```  
  
#### Parameter  
 *catalog*  
  
 Ein **String** mit dem Katalognamen. Durch Festlegen dieses Parameters auf NULL wird angegeben, dass der Katalogname nicht verwendet werden muss.  
  
 *schema*  
  
 Ein **String** mit dem Schemanamenmuster. Durch Festlegen dieses Parameters auf NULL wird angegeben, dass der Schemaname nicht verwendet werden muss.  
  
 *table*  
  
 Ein **String** mit dem Tabellennamenmuster.  
  
## Rückgabewert  
 Ein [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getTablePrivileges\-Methode wird von der getTablePrivileges\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
 Das von der getTablePrivileges\-Methode zurückgegebene Resultset enthält folgende Informationen:  
  
|Name|Typ|Beschreibung|  
|----------|---------|------------------|  
|TABLE\_CAT|**String**|Der Name des Katalogs.|  
|TABLE\_SCHEM|**String**|Der Tabellenschemaname.|  
|TABLE\_NAME|**String**|Der Tabellenname.|  
|GRANTOR|**String**|Das Objekt, von dem der Zugriff gewährt wird.|  
|GRANTEE|**String**|Das Objekt, von dem der Zugriff empfangen wird.|  
|PRIVILEGE|**String**|Der Typ des gewährten Zugriffs.|  
|IS\_GRANTABLE|**String**|Gibt an, ob der Empfänger seinerseits anderen Benutzern Zugriff gewähren darf.|  
  
> [!NOTE]  
>  Weitere Informationen zu den Daten, die von der getTablePrivileges\-Methode zurückgegeben werden, finden Sie in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation unter "sp\_table\_privileges \(Transact\-SQL\)".  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie mithilfe der getTablePrivileges\-Methode Zugriffsrechte für die Tabelle "Person.Contact" aus der [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)][!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank zurückgegeben werden können.  
  
```  
public static void executeGetTablePrivileges(Connection con) {  
   try {  
      DatabaseMetaData dbmd = con.getMetaData();  
      ResultSet rs = dbmd.getTablePrivileges("AdventureWorks", "Person", "Contact");  
      ResultSetMetaData rsmd = rs.getMetaData();  
  
      // Display the result set data.  
      int cols = rsmd.getColumnCount();  
      while(rs.next()) {  
         for (int i = 1; i <= cols; i++) {  
            System.out.println(rs.getString(i));  
         }  
      }  
      rs.close();  
   }   
  
   catch (Exception e) {  
      e.printStackTrace();  
   }  
}  
```  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  