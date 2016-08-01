---
title: "getIndexInfo-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.getIndexInfo
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 8a677cc6-8e33-4e57-8678-0849345aa8d0
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
# getIndexInfo-Methode (SQLServerDatabaseMetaData)
    
## getIndexInfo\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft eine Beschreibung der Indizes und der Statistik für die angegebene Tabelle ab.  
  
## Syntax  
  
```  
  
public java.sql.ResultSet getIndexInfo(java.lang.String cat,  
                                       java.lang.String schema,  
                                       java.lang.String table,  
                                       boolean unique,  
                                       boolean approximate)  
```  
  
#### Parameter  
 *cat*  
  
 Ein **String** mit dem Katalognamen.  
  
 *schema*  
  
 Ein **String** mit dem Schemanamen.  
  
 *table*  
  
 Ein **String** mit dem Tabellennamen.  
  
 *unique*  
  
 **true**, wenn nur Indizes für individuelle Werte zurückgegeben werden. **false**, wenn alle Indizes zurückgegeben werden.  
  
 *approximate*  
  
 **true**, wenn die Ergebnisse ungefähre oder veraltete Werte wiedergeben. **false**, wenn die Ergebnisse korrekt sind.  
  
## Rückgabewert  
 Ein [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getIndexInfo\-Methode wird von der getIndexInfo\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
 Das von der getIndexInfo\-Methode zurückgegebene Resultset enthält folgende Informationen:  
  
|Name|Typ|Beschreibung|  
|----------|---------|------------------|  
|TABLE\_CAT|**String**|Der Name der Datenbank, in der die angegebene Tabelle gespeichert ist.|  
|TABLE\_SCHEM|**String**|Das Schema für die Tabelle.|  
|TABLE\_NAME|**String**|Der Name der Tabelle.|  
|NON\_UNIQUE|**boolean**|Gibt an, ob die Indexwerte nicht eindeutig sein können.|  
|INDEX\_QUALIFIER|**String**|Der Name des Indexbesitzers. Wenn für TYPE das tableIndexStatistic\-Objekt eingetragen wird, entspricht er NULL.|  
|INDEX\_NAME|**String**|Der Name des Indexes.|  
|TYPE|**short**|Der Typ des Indexes. Mögliche Werte:<br /><br /> tableIndexStatistic \(0\)<br /><br /> tableIndexClustered \(1\)<br /><br /> tableIndexHashed \(2\)<br /><br /> tableIndexOther \(3\)|  
|ORDINAL\_POSITION|**short**|Die Ordinalposition der Spalte innerhalb des Indexes. Die erste Spalte im Index hat den Wert 1.|  
|COLUMN\_NAME|**String**|Der Name der Spalte.|  
|ASC\_OR\_DESC|**String**|Der in der Indexsortierung verwendete Befehl. Mögliche Werte:<br /><br /> A \(aufsteigend\)<br /><br /> D \(absteigend\)<br /><br /> NULL \(nicht anwendbar\) **Note:**  [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] gibt immer "A" zurück.|  
|CARDINALITY|**int**|Die Anzahl der Zeilen in der Tabelle oder der eindeutigen Werte im Index|  
|PAGES|**int**|Die Anzahl der Seiten, die zum Speichern des Indexes oder der Tabelle verwendet werden.|  
|FILTER\_CONDITION|**String**|Die Filter\-Bedingung. **Note:**  [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] gibt immer NULL zurück.|  
  
> [!NOTE]  
>  Weitere Informationen zu den Daten, die von der getIndexInfo\-Methode zurückgegeben werden, finden Sie in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation unter "sp\_indexes \(Transact\-SQL\)".  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie mithilfe der getIndexInfo\-Methode Informationen über die Indizes und Statistiken der Tabelle "Person.Contact" aus der [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)][!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank zurückgegeben werden können.  
  
```  
public static void executeGetIndexInfo(Connection con) {  
   try {  
      DatabaseMetaData dbmd = con.getMetaData();  
      ResultSet rs = dbmd.getIndexInfo("AdventureWorks", "Person", "Contact", false, true);  
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
  
  