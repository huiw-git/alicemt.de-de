---
title: "getTables-Methode (SQLServerDatabaseMetaData)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLServerDatabaseMetaData.getTables
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: a7514673-3457-4541-9560-28a8284ad9e3
caps.latest.revision: 15
caps.handback.revision: 10
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
# getTables-Methode (SQLServerDatabaseMetaData)
    
## getTables\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft eine Beschreibung der Tabellen ab, die im angegebenen Katalog, Schema oder Tabellennamenmuster verfügbar sind.  
  
## Syntax  
  
```  
  
public java.sql.ResultSet getTables(java.lang.String catalog,  
                                    java.lang.String schema,  
                                    java.lang.String table,  
                                    java.lang.String[] types)  
```  
  
#### Parameter  
 *catalog*  
  
 Ein **String** mit dem Katalognamen. Durch Festlegen dieses Parameters auf NULL wird angegeben, dass der Katalogname nicht verwendet werden muss.  
  
 *schema*  
  
 Ein **String** mit dem Schemanamenmuster. Durch Festlegen dieses Parameters auf NULL wird angegeben, dass der Schemaname nicht verwendet werden muss.  
  
 *tableName*  
  
 Ein **String** mit dem Tabellennamenmuster.  
  
 *types*  
  
 Ein Zeichenfolgenarray mit den einzubeziehenden Tabellentypen. Mit "NULL" wird angegeben, dass alle Tabellentypen einbezogen werden sollen.  
  
## Rückgabewert  
 Ein [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getTables\-Methode wird von der getTables\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
 Das von der getTables\-Methode zurückgegebene Resultset enthält folgende Informationen:  
  
|Name|Typ|Beschreibung|  
|----------|---------|------------------|  
|TABLE\_CAT|**String**|Der Name der Datenbank, in der die angegebene Tabelle gespeichert ist.|  
|TABLE\_SCHEM|**String**|Der Tabellenschemaname.|  
|TABLE\_NAME|**String**|Der Tabellenname.|  
|TABLE\_TYPE|**String**|Der Tabellentyp.|  
|REMARKS|**String**|Die Beschreibung der Tabelle. **Note:**  [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] gibt für diese Spalte keinen Wert zurück.|  
|TYPE\_CAT|**String**|Wird vom JDBC\-Treiber nicht unterstützt.|  
|TYPE\_SCHEM|**String**|Wird vom JDBC\-Treiber nicht unterstützt.|  
|TYPE\_NAME|**String**|Wird vom JDBC\-Treiber nicht unterstützt.|  
|SELF\_REFERENCING\_COL\_NAME|**String**|Wird vom JDBC\-Treiber nicht unterstützt.|  
|REF\_GENERATION|**String**|Wird vom JDBC\-Treiber nicht unterstützt.|  
  
> [!NOTE]  
>  Weitere Informationen zu den Daten, die von der getTables\-Methode zurückgegeben werden, finden Sie in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation unter "sp\_tables \(Transact\-SQL\)".  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie mithilfe der getTables\-Methode Tabellenbeschreibungsinformationen für die Tabelle "Person.Contact" aus der [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)][!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank zurückgegeben werden können.  
  
```  
public static void executeGetTables(Connection con) {  
   try {  
      DatabaseMetaData dbmd = con.getMetaData();  
      ResultSet rs = dbmd.getTables("AdventureWorks", "Person", "Contact", null);  
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
  
  