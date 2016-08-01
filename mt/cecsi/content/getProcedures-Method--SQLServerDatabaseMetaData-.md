---
title: "getProcedures-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.getProcedures
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 66c9a8b0-dc4c-4cbb-8004-c7157368cab4
caps.latest.revision: 24
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
# getProcedures-Methode (SQLServerDatabaseMetaData)
    
## getProcedures\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft eine Beschreibung der gespeicherten Prozeduren ab, die im angegebenen Katalog, Schema oder Namensmuster für gespeicherte Prozeduren verfügbar sind.  
  
## Syntax  
  
```  
  
public java.sql.ResultSet getProcedures(java.lang.String sCatalog,  
                                        java.lang.String sSchema,  
                                        java.lang.String proc)  
```  
  
#### Parameter  
 *sCatalog*  
  
 Ein **String** mit dem Katalognamen. Durch Festlegen dieses Parameters auf NULL wird angegeben, dass der Katalogname nicht verwendet werden muss.  
  
 *sSchema*  
  
 Ein **String** mit dem Schemanamenmuster. Durch Festlegen dieses Parameters auf NULL wird angegeben, dass der Schemaname nicht verwendet werden muss.  
  
 *proc*  
  
 Ein **String** mit dem Prozedurnamenmuster.  
  
## Rückgabewert  
 Ein [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getProcedures\-Methode wird von der getProcedures\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
 Das von der getProcedures\-Methode zurückgegebene Resultset enthält folgende Informationen:  
  
|Name|Typ|Beschreibung|  
|----------|---------|------------------|  
|PROCEDURE\_CAT|**String**|Der Name der Datenbank, in der sich die angegebene gespeicherte Prozedur befindet.|  
|PROCEDURE\_SCHEM|**String**|Das Schema für die gespeicherte Prozedur.|  
|PROCEDURE\_NAME|**String**|Der Name der gespeicherten Prozedur.|  
|NUM\_INPUT\_PARAMS|**int**|Reserviert für zukünftige Verwendung. Gibt derzeit den Wert "\-1" zurück.|  
|NUM\_OUTPUT\_PARAMS|**int**|Reserviert für zukünftige Verwendung. Gibt derzeit den Wert "\-1" zurück.|  
|NUM\_RESULT\_SETS|**int**|Reserviert für zukünftige Verwendung. Gibt derzeit den Wert "\-1" zurück.|  
|REMARKS|**String**|Die Beschreibung der Prozedurspalte. **Note:**  [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] gibt für diese Spalte keinen Wert zurück.|  
|PROCEDURE\_TYPE|**smallint**|Der Typ der gespeicherten Prozedur. Mögliche Werte:<br /><br /> SQL\_PT\_UNKNOWN \(0\)<br /><br /> SQL\_PT\_PROCEDURE \(1\)<br /><br /> SQL\_PT\_FUNCTION \(2\)|  
  
> [!NOTE]  
>  Weitere Informationen zu den Daten, die von der getProcedures\-Methode zurückgegeben werden, finden Sie in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation unter "sp\_stored\_procedures \(Transact\-SQL\)".  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie mithilfe der getProcedures\-Methode Informationen zur gespeicherten Prozedur "uspGetBillOfMaterials" aus der [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)][!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank zurückgegeben werden können.  
  
```  
public static void executeGetProcedures(Connection con) {  
   try {  
      DatabaseMetaData dbmd = con.getMetaData();  
      ResultSet rs = dbmd.getProcedures(null, null, "uspGetBillOfMaterials");  
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
  
  