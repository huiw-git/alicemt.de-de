---
title: "getTypeInfo-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.getTypeInfo
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 23208f01-c1bf-4235-b29c-9051d3df59a3
caps.latest.revision: 21
caps.handback.revision: 20
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
# getTypeInfo-Methode (SQLServerDatabaseMetaData)
    
## getTypeInfo\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft eine Beschreibung aller standardmäßigen SQL\-Typen ab, die von der aktuellen Datenbank unterstützt werden.  
  
## Syntax  
  
```  
  
public java.sql.ResultSet getTypeInfo()  
```  
  
## Rückgabewert  
 Ein [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getTypeInfo\-Methode wird von der getTypeInfo\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
 Das von der getTypeInfo\-Methode zurückgegebene Resultset enthält folgende Informationen:  
  
|Name|Typ|Beschreibung|  
|----------|---------|------------------|  
|TYPE\_NAME|**String**|Der Name des Datentyps.|  
|DATA\_TYPE|**short**|Der SQL\-Datentyp aus "java.sql.Types".|  
|PRECISION|**int**|Die Gesamtanzahl von signifikanten Stellen.|  
|LITERAL\_PREFIX|**String**|Die Zeichen, die einer Konstante vorangestellt werden.|  
|LITERAL\_SUFFIX|**String**|Die Zeichen, die eine Konstante beenden.|  
|CREATE\_PARAMS|**String**|Die Beschreibung der Erstellungsparameter für den Datentyp.|  
|NULLABLE|**short**|Gibt an, ob die Spalte einen NULL\-Wert enthalten kann. Mögliche Werte:<br /><br /> typeNoNulls \(0\)<br /><br /> typeNullable \(1\)<br /><br /> typeNullableUnknown \(2\)|  
|CASE\_SENSITIVE|**boolean**|Gibt an, ob bei dem Datentyp die Groß\-\/Kleinschreibung berücksichtigt wird. "**true**", wenn bei dem Typ die Groß\-\/Kleinschreibung berücksichtigt wird; andernfalls "**false**".|  
|SEARCHABLE|**short**|Gibt an, ob die Spalte in einer SQL\-Klausel vom Typ "WHERE" verwendet werden kann. Mögliche Werte:<br /><br /> typePredNone \(0\)<br /><br /> typePredChar \(1\)<br /><br /> typePredBasic \(2\)<br /><br /> typeSeachable \(3\)|  
|UNSIGNED\_ATTRIBUTE|**boolean**|Gibt das Vorzeichen des Datentyps an. "**true**", wenn der Typ kein Vorzeichen besitzt; andernfalls "**false**".|  
|FIXED\_PREC\_SCALE|**boolean**|Gibt an, dass es sich bei dem Datentyp um eine Währung handeln kann. "**true**", wenn es sich bei dem Datentyp um eine Währung handelt; andernfalls "**false**".|  
|AUTO\_INCREMENT|**boolean**|Gibt an, dass der Datentyp automatisch inkrementiert werden kann. "**true**", wenn der Typ automatisch inkrementiert werden kann; andernfalls "**false**".|  
|LOCAL\_TYPE\_NAME|**String**|Der lokalisierte Name des Datentyps.|  
|MINIMUM\_SCALE|**short**|Die maximale Anzahl von Stellen rechts des Dezimalzeichens.|  
|MAXIMUM\_SCALE|**short**|Die Mindestanzahl von Stellen rechts des Dezimalzeichens.|  
|SQL\_DATA\_TYPE|**int**|Wird vom JDBC\-Treiber nicht unterstützt.|  
|SQL\_DATETIME\_SUB|**int**|Wird vom JDBC\-Treiber nicht unterstützt.|  
|NUM\_PREC\_RADIX|**int**|Die Anzahl von Bits oder Stellen zum Berechnen der höchsten Zahl, die eine Spalte enthalten kann.|  
|INTERVAL\_PRECISION|**smallint**|Die Genauigkeit für anführenden Intervallwert.|  
|USERTYPE|**smallint**|Der **usertype**\-Wert aus der **systypes**\-Tabelle. Weitere Informationen finden Sie in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation.|  
  
> [!NOTE]  
>  Weitere Informationen zu den Daten, die von der getTypeInfo\-Methode zurückgegeben werden, finden Sie in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation unter "sp\_datatype\_info \(Transact\-SQL\)".  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie mithilfe der getTypeInfo\-Methode Informationen zu den Datentypen zurückgegeben werden können, die in einer Datenbank der Version [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] oder später verwendet werden.  
  
```  
public static void executeGetTypeInfo(Connection con) {  
   try {  
      DatabaseMetaData dbmd = con.getMetaData();  
      ResultSet rs = dbmd.getTypeInfo();  
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
  
  