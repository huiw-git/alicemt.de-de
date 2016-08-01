---
title: "getImportedKeys-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.getImportedKeys
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: dc8c1a5e-700e-4059-a5ed-5013bbb87fb6
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
# getImportedKeys-Methode (SQLServerDatabaseMetaData)
    
## getImportedKeys\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft eine Beschreibung der Primärschlüsselspalten ab, auf die von den Fremdschlüsselspalten in einer Tabelle verwiesen wird.  
  
## Syntax  
  
```  
  
public java.sql.ResultSet getImportedKeys(java.lang.String cat,  
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
 Diese getImportedKeys\-Methode wird von der getImportedKeys\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
 Das von der getImportedKeys\-Methode zurückgegebene Resultset enthält folgende Informationen:  
  
|Name|Typ|Beschreibung|  
|----------|---------|------------------|  
|PKTABLE\_CAT|**String**|Der Name des Katalogs, der die Primärschlüsseltabelle enthält.|  
|PKTABLE\_SCHEM|**String**|Der Name des Schemas der Primärschlüsseltabelle.|  
|PKTABLE\_NAME|**String**|Der Name der Primärschlüsseltabelle.|  
|PKCOLUMN\_NAME|**String**|Der Spaltenname des Primärschlüssels.|  
|FKTABLE\_CAT|**String**|Der Name des Katalogs, der die Fremdschlüsseltabelle enthält.|  
|FKTABLE\_SCHEM|**String**|Der Name des Schemas der Fremdschlüsseltabelle.|  
|FKTABLE\_NAME|**String**|Der Name der Fremdschlüsseltabelle.|  
|FKCOLUMN\_NAME|**String**|Der Spaltenname des Fremdschlüssels.|  
|KEY\_SEQ|**short**|Die Sequenznummer der Spalte bei einem Primärschlüssel, der durch mehrere Spalten definiert wird.|  
|UPDATE\_RULE|**short**|Die auf den Fremdschlüssel angewendete Aktion, wenn es sich beim SQL\-Vorgang um ein Update handelt. Mögliche Werte:<br /><br /> importedKeyNoAction \(3\)<br /><br /> importedKeyCascade \(0\)<br /><br /> importedKeySetNull \(2\)<br /><br /> importedKeySetDefault \(4\)<br /><br /> importedKeyRestrict \(1\)|  
|DELETE\_RULE|**short**|Die auf den Fremdschlüssel angewendete Aktion, wenn es sich beim SQL\-Vorgang um eine Löschung handelt. Mögliche Werte:<br /><br /> importedKeyNoAction \(3\)<br /><br /> importedKeyCascade \(0\)<br /><br /> importedKeySetNull \(2\)<br /><br /> importedKeySetDefault \(4\)<br /><br /> importedKeyRestrict \(1\)|  
|FK\_NAME|**String**|Der Name des Fremdschlüssels.|  
|PK\_NAME|**String**|Der Name des Primärschlüssels.|  
|DEFERRABILITY|**short**|Zeigt an, ob die Auswertung der Fremdschlüsseleinschränkung bis zur Ausführung einer Commit\-Aktion verzögert werden kann. Mögliche Werte:<br /><br /> importedKeyInitiallyDeferred \(5\)<br /><br /> importedKeyInitiallyImmediate \(6\)<br /><br /> importedKeyNotDeferrable \(7\)|  
  
> [!NOTE]  
>  Weitere Informationen zu den Daten, die von der getImportedKeys\-Methode zurückgegeben werden, finden Sie in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation unter "sp\_fkeys \(Transact\-SQL\)".  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie mithilfe der getImportedKeys\-Methode Informationen zu allen Primärschlüsseln zurückgegeben werden, die auf die Fremdschlüssel der Tabelle "Person.Address" in der [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)][!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank verweisen.  
  
```  
public static void executeGetImportedKeys(Connection con) {  
   try {  
      DatabaseMetaData dbmd = con.getMetaData();  
      ResultSet rs = dbmd.getImportedKeys("AdventureWorks", "Person", "Address");  
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
  
  