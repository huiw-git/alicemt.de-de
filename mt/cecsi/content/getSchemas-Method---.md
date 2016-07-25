---
title: "getSchemas-Methode ()"
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
  - SQLServerDatabaseMetaData.getSchemas
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: adba0ee6-ff6d-4215-b646-62c735be3fe9
caps.latest.revision: 19
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
# getSchemas-Methode ()
    
## getSchemas\-Methode \(\)  
 Ruft die Schemanamen ab, die in der aktuellen Datenbank verfügbar sind.  
  
## Syntax  
  
```  
  
public java.sql.ResultSet getSchemas()  
```  
  
## Rückgabewert  
 Ein [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getSchemas\-Methode wird von der getSchemas\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
 Das von der getSchemas\-Methode zurückgegebene Resultset enthält folgende Informationen:  
  
|Name|Typ|Beschreibung|  
|----------|---------|------------------|  
|TABLE\_SCHEM|**String**|Der Name des Schemas.|  
|TABLE\_CATALOG|**String**|Der Katalogname für das Schema.|  
  
 Die Ergebnisse werden nach "TABLE\_CATALOG" und anschließend nach "TABLE\_SCHEM" sortiert. In jeder Zeile bildet "TABLE\_SCHEM" die erste Spalte und "TABLE\_CATALOG" die zweite Spalte.  
  
> [!NOTE]  
>  Weitere Informationen zu den Daten, die von der getSchemas\-Methode zurückgegeben werden, finden Sie in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation unter "sys.schemas \(Transact\-SQL\)".  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie mithilfe der getSchemas\-Methode Informationen zum Katalog und den ihm zugeordneten Schemanamen in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] zurückgegeben werden können, wenn die zu verwendende Datenbank durch das connection\-Argument angegeben wird.  
  
```  
public static void executeGetSchemas(Connection con) {  
   try {  
      DatabaseMetaData dbmd = con.getMetaData();  
      ResultSet rs = dbmd.getSchemas();  
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
  
  