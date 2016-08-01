---
title: "getPrimaryKeys-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.getPrimaryKeys
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: ebfe236a-dc02-493e-a3ab-5353d3769e36
caps.latest.revision: 13
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
# getPrimaryKeys-Methode (SQLServerDatabaseMetaData)
    
## getPrimaryKeys\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft eine Beschreibung der Primärschlüsselspalten der angegebenen Tabelle ab.  
  
## Syntax  
  
```  
  
public java.sql.ResultSet getPrimaryKeys(java.lang.String cat,  
                                         java.lang.String schema,  
                                         java.lang.String table)  
```  
  
#### Parameter  
 *cat*  
  
 Ein **String** mit dem Katalognamen.  
  
 *schema*  
  
 Ein **String** mit dem Schemanamen.  
  
 *table*  
  
 Ein **String** mit dem Tabellennamen.  
  
## Rückgabewert  
 Ein [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getPrimaryKeys\-Methode wird von der getPrimaryKeys\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
 Das von der getPrimaryKeys\-Methode zurückgegebene Resultset enthält folgende Informationen:  
  
|Name|Typ|Beschreibung|  
|----------|---------|------------------|  
|TABLE\_CAT|String|Der Name der Datenbank, in der die angegebene Tabelle gespeichert ist.|  
|TABLE\_SCHEM|String|Das Schema für die Tabelle.|  
|TABLE\_NAME|String|Der Name der Tabelle.|  
|COLUMN\_NAME|String|Der Name der Spalte.|  
|KEY\_SEQ|short|Die Sequenznummer der Spalte bei einem Primärschlüssel, der durch mehrere Spalten definiert wird.|  
|PK\_NAME|String|Der Name des Primärschlüssels.|  
  
> [!NOTE]  
>  Weitere Informationen zu den Daten, die von der getPrimaryKeys\-Methode zurückgegeben werden, finden Sie in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation unter "sp\_pkeys \(Transact\-SQL\)".  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie mithilfe der getPrimaryKeys\-Methode Informationen zu den Primärschlüsseln der Tabelle "Person.Contact" aus der [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)][!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank zurückgegeben werden können.  
  
```  
public static void executeGetPrimaryKeys(Connection con) {  
   try {  
      DatabaseMetaData dbmd = con.getMetaData();  
      ResultSet rs = dbmd.getPrimaryKeys("AdventureWorks", "Person", "Contact");  
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
  
  