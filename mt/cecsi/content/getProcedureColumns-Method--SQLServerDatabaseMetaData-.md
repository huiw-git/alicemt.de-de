---
title: "getProcedureColumns-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.getProcedureColumns
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 4f0df8fe-3cd6-46e4-ae3c-dc23c35676b2
caps.latest.revision: 22
caps.handback.revision: 17
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
# getProcedureColumns-Methode (SQLServerDatabaseMetaData)
    
## getProcedureColumns\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft eine Beschreibung der Parameter gespeicherter Prozeduren und Ergebnisspalten ab.  
  
## Syntax  
  
```  
  
public java.sql.ResultSet getProcedureColumns(java.lang.String sCatalog,  
                                              java.lang.String sSchema,  
                                              java.lang.String proc,  
                                              java.lang.String col)  
```  
  
#### Parameter  
 *sCatalog*  
  
 Ein **String** mit dem Katalognamen. Durch Festlegen dieses Parameters auf NULL wird angegeben, dass der Katalogname nicht verwendet werden muss.  
  
 *sSchema*  
  
 Ein **String** mit dem Schemanamenmuster. Durch Festlegen dieses Parameters auf NULL wird angegeben, dass der Schemaname nicht verwendet werden muss.  
  
 *proc*  
  
 Ein **String** mit dem Prozedurnamenmuster.  
  
 *col*  
  
 Ein **String** mit dem Spaltennamenmuster. Wird für diesen Parameter NULL angegeben, wird für jede Spalte eine Zeile zurückgegeben.  
  
## Rückgabewert  
 Ein [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getProcedureColumns\-Methode wird von der getProcedureColumns\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
 Das von der getProcedureColumns\-Methode zurückgegebene Resultset enthält folgende Informationen:  
  
|Name|Typ|Beschreibung|  
|----------|---------|------------------|  
|PROCEDURE\_CAT|**String**|Der Name der Datenbank, in der sich die angegebene gespeicherte Prozedur befindet.|  
|PROCEDURE\_SCHEM|**String**|Das Schema für die gespeicherte Prozedur.|  
|PROCEDURE\_NAME|**String**|Der Name der gespeicherten Prozedur.|  
|COLUMN\_NAME|**String**|Der Name der Spalte.|  
|COLUMN\_TYPE|**short**|Der Typ der Spalte. Mögliche Werte:<br /><br /> procedureColumnUnknown \(0\)<br /><br /> procedureColumnIn \(1\)<br /><br /> procedureColumnInOut \(2\)<br /><br /> procedureColumnOut \(4\)<br /><br /> procedureColumnReturn \(5\)<br /><br /> procedureColumnResult \(3\)|  
|DATA\_TYPE|**smallint**|Der SQL\-Datentyp aus "java.sql.Types".|  
|TYPE\_NAME|**String**|Der Name des Datentyps.|  
|PRECISION|**int**|Die Gesamtanzahl von signifikanten Stellen.|  
|LENGTH|**int**|Die Länge der Daten in Bytes.|  
|SCALE|**short**|Die Anzahl von Stellen rechts des Dezimalzeichens.|  
|RADIX|**short**|Die Basis für numerische Typen.|  
|NULLABLE|**short**|Gibt an, ob die Spalte einen NULL\-Wert enthalten kann. Mögliche Werte:<br /><br /> procedureNoNulls \(0\)<br /><br /> procedureNullable \(1\)<br /><br /> procedureNullableUnknown \(2\)|  
|REMARKS|**String**|Die Beschreibung der Prozedurspalte. **Note:**  [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] gibt für diese Spalte keinen Wert zurück.|  
|COLUMN\_DEF|**String**|Der Standardwert der Spalte.|  
|SQL\_DATA\_TYPE|**smallint**|Diese Spalte entspricht \(mit Ausnahme der Datentypen **datetime** und ISO **interval**\) der **DATA\_TYPE**\-Spalte.|  
|SQL\_DATETIME\_SUB|**smallint**|Der Subcode für **datetime** ISO **interval**, wenn der Wert von **SQL\_DATA\_TYPE** dem Wert **SQL\_DATETIME** oder **SQL\_INTERVAL** entspricht. Bei allen anderen Datentypen außer **datetime** und ISO **interval** ist diese Spalte NULL.|  
|CHAR\_OCTET\_LENGTH|**int**|Die maximale Anzahl von Bytes in der Spalte.|  
|ORDINAL\_POSITION|**int**|Der Index der Spalte innerhalb der Tabelle.|  
|IS\_NULLABLE|**String**|Gibt an, ob in der Spalte NULL\-Werte zulässig sind.|  
|SS\_TYPE\_CATALOG\_NAME|**String**|Der Name des Katalogs, der den benutzerdefinierten Typ \(UDT\) enthält.|  
|SS\_TYPE\_SCHEMA\_NAME|**String**|Der Name des Schemas, der den benutzerdefinierten Typ \(UDT\) enthält.|  
|SS\_UDT\_CATALOG\_NAME|**String**|Der benutzerdefinierte Typ \(UDT\) für den vollqualifizierten Namen.|  
|SS\_UDT\_SCHEMA\_NAME|**String**|Der Name des Katalogs, in dem eine XML\-Schemaauflistung definiert ist. Wenn der Katalogname nicht gefunden werden kann, enthält diese Variable eine leere Zeichenfolge.|  
|SS\_UDT\_ASSEMBLY\_TYPE\_NAME|**String**|Der Name des Schemas, in dem eine XML\-Schemaauflistung definiert ist. Wenn der Schemaname nicht gefunden werden kann, handelt es sich dabei um eine leere Zeichenfolge.|  
|SS\_XML\_SCHEMACOLLECTION\_CATALOG\_NAME|**String**|Name der XML\-Schemaauflistung. Wenn der Schemaname nicht gefunden werden kann, handelt es sich dabei um eine leere Zeichenfolge.|  
|SS\_XML\_SCHEMACOLLECTION\_SCHEMA\_NAME|**String**|Der Name des Katalogs, der den benutzerdefinierten Typ \(UDT\) enthält.|  
|SS\_XML\_SCHEMACOLLECTION\_NAME|**String**|Der Name des Schemas, der den benutzerdefinierten Typ \(UDT\) enthält.|  
|SS\_DATA\_TYPE|**tinyint**|Der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentyp, der von erweiterten gespeicherten Prozeduren verwendet wird. **Note:**  Weitere Informationen zu den Datentypen, die von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] zurückgegeben werden, finden Sie in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation unter "Datentypen \(Transact\-SQL\)".|  
  
> [!NOTE]  
>  Weitere Informationen zu den Daten, die von der getProcedureColumns\-Methode zurückgegeben werden, finden Sie in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation unter "sp\_sproc\_columns \(Transact\-SQL\)".  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie mithilfe der getProcedureColumns\-Methode Informationen zur gespeicherten Prozedur "uspGetBillOfMaterials" aus der [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)][!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank zurückgegeben werden können.  
  
```  
public static void executeGetProcedureColumns(Connection con) {  
   try {  
      DatabaseMetaData dbmd = con.getMetaData();  
      ResultSet rs = dbmd.getProcedureColumns(null, null, "uspGetBillOfMaterials", null);  
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
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  