---
title: "getBestRowIdentifier-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.getBestRowIdentifier
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: c19e9ca6-2a53-4a0c-91ab-80090c3f7229
caps.latest.revision: 15
caps.handback.revision: 12
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
# getBestRowIdentifier-Methode (SQLServerDatabaseMetaData)
    
## getBestRowIdentifier\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft eine Beschreibung der optimalen Gruppe von Spalten einer Tabelle ab, durch die eine Zeile eindeutig identifiziert wird.  
  
## Syntax  
  
```  
  
public java.sql.ResultSet getBestRowIdentifier(java.lang.String catalog,  
                                               java.lang.String schema,  
                                               java.lang.String table,  
                                               int scope,  
                                               boolean nullable)  
```  
  
#### Parameter  
 *catalog*  
  
 Ein **String** mit dem Katalognamen.  
  
 *schema*  
  
 Ein **String** mit dem Schemanamen.  
  
 *table*  
  
 Ein **String** mit dem Tabellennamen.  
  
 *scope*  
  
 Ein Wert vom Typ **int** zum Angeben des relevanten Bereichs. Die Werte können Folgendes enthalten:  
  
 bestRowTemporary \(0\)  
  
 bestRowTransaction \(1\)  
  
 bestRowSession \(2\)  
  
 *nullable*  
  
 **true**, um Spalten einzuschließen, für die NULL zulässig ist. Andernfalls wird **false** verwendet.  
  
## Rückgabewert  
 Ein [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getBestRowIdentifier\-Methode wird von der getBestRowIdentifier\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
 Das von der getBestRowIdentifier\-Methode zurückgegebene Resultset enthält folgende Informationen:  
  
|Name|Typ|Beschreibung|  
|----------|---------|------------------|  
|SCOPE|short|Der Bereich der zurückgegebenen Ergebnisse. Mögliche Werte:<br /><br /> bestRowTemporary \(0\)<br /><br /> bestRowTransaction \(1\)<br /><br /> bestRowSession \(2\)|  
|COLUMN\_NAME|String|Der Name der Spalte.|  
|DATA\_TYPE|short|Der SQL\-Datentyp aus "java.sql.Types".|  
|TYPE\_NAME|String|Der Name des Datentyps.|  
|COLUMN\_SIZE|int|Die Genauigkeit der Spalte.|  
|BUFFER\_LENGTH|int|Die Pufferlänge.|  
|DECIMAL\_DIGITS|short|Die Dezimalstellen der Spalte.|  
|PSEUDO\_COLUMN|short|Gibt an, ob die Spalte eine Pseudospalte ist. Mögliche Werte:<br /><br /> bestRowUnknown \(0\)<br /><br /> bestRowNotPseudo \(1\)<br /><br /> bestRowPseudo \(2\)|  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie mithilfe der getBestRowIdentifier\-Methode Informationen zum geeignetsten Zeilenidentifizierer für die Tabelle "Person.Contact" aus der [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)][!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank zurückgegeben werden können.  
  
```  
public static void executeGetBestRowIdentifier(Connection con) {  
   try {  
      DatabaseMetaData dbmd = con.getMetaData();  
      ResultSet rs = dbmd.getBestRowIdentifier(null, "Person", "Contact", 0, true);  
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
  
  