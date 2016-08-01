---
title: "getVersionColumns-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.getVersionColumns
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 6dd275d3-d9b2-4db7-938a-d4406c940a7a
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
# getVersionColumns-Methode (SQLServerDatabaseMetaData)
    
## getVersionColumns\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft eine Beschreibung der Spalten einer Tabelle ab, die automatisch aktualisiert wird, wenn ein Wert in einer Zeile aktualisiert wird.  
  
## Syntax  
  
```  
  
public java.sql.ResultSet getVersionColumns(java.lang.String catalog,  
                                            java.lang.String schema,  
                                            java.lang.String table)  
```  
  
#### Parameter  
 *catalog*  
  
 Ein **String** mit dem Katalognamen.  
  
 *schema*  
  
 Ein **String** mit dem Schemanamenmuster.  
  
 *table*  
  
 Ein **String** mit dem Tabellennamen.  
  
## Rückgabewert  
 Ein [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getVersionColumns\-Methode wird von der getVersionColumns\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
 Das von der getVersionColumns\-Methode zurückgegebene Resultset enthält folgende Informationen:  
  
|Name|Typ|Beschreibung|  
|----------|---------|------------------|  
|SCOPE|**short**|Wird vom JDBC\-Treiber nicht unterstützt.|  
|COLUMN\_NAME|**String**|Der Spaltenname.|  
|DATA\_TYPE|**short**|Der SQL\-Datentyp aus "java.sql.Types".|  
|TYPE\_NAME|**String**|Der Name des Datentyps.|  
|COLUMN\_SIZE|**int**|Die Genauigkeit der Spalte.|  
|BUFFER\_LENGTH|**int**|Die Länge der Spalten in Bytes.|  
|DECIMAL\_DIGITS|**short**|Die Dezimalstellen der Spalte.|  
|PSEUDO\_COLUMN|**short**|Gibt an, ob die Spalte eine Pseudospalte ist. Mögliche Werte:<br /><br /> versionColumnUnknown \(0\)<br /><br /> versionColumnNotPseudo \(1\)<br /><br /> versionColumnPseudo \(2\)|  
  
> [!NOTE]  
>  Weitere Informationen zu den Daten, die von der getVersionColumns\-Methode zurückgegeben werden, finden Sie in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation unter "sp\_datatype\_info \(Transact\-SQL\)".  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie mithilfe der getVersionColumns\-Methode Informationen zu den Spalten, die in der Tabelle "Person.Contact" in der [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)][!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank automatisch aktualisiert werden, zurückgegeben werden.  
  
```  
public static void executeGetVersionColumns(Connection con) {  
   try {  
      DatabaseMetaData dbmd = con.getMetaData();  
      ResultSet rs = dbmd.getVersionColumns("AdventureWorks", "Person", "Contact");  
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
  
  