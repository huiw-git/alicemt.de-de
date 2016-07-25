---
title: "getCrossReference-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.getCrossReference
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 099dd0bf-b017-479d-9696-f5b06f4c6bf9
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
# getCrossReference-Methode (SQLServerDatabaseMetaData)
    
## getCrossReference\-Methode \(SQLServerDatabaseMetaData\)  
 Ruft eine Beschreibung der Fremdschlüsselspalten in der angegebenen Fremdschlüsseltabelle ab, von der auf die Primärschlüsselspalten der angegebenen Primärschlüsseltabelle verwiesen wird.  
  
## Syntax  
  
```  
  
public java.sql.ResultSet getCrossReference(java.lang.String cat1,  
                                            java.lang.String schem1,  
                                            java.lang.String tab1,  
                                            java.lang.String cat2,  
                                            java.lang.String schem2,  
                                            java.lang.String tab2)  
```  
  
#### Parameter  
 *cat1*  
  
 Ein **String** , der den Katalognamen der Tabelle enthält, die den primären Schlüssel enthält.  
  
 *schem1*  
  
 Ein **String** , der den Schemanamen der Tabelle enthält, die den primären Schlüssel enthält.  
  
 *tab1*  
  
 Ein **String** , der den Tabellennamen der Tabelle enthält, die den primären Schlüssel enthält.  
  
 *cat2*  
  
 Ein **String** , der den Katalognamen der Tabelle enthält, die den Fremdschlüssel enthält.  
  
 *schem2*  
  
 Ein **String** , der den Schemanamen der Tabelle enthält, die den Fremdschlüssel enthält.  
  
 *tab2*  
  
 Ein **String** , der den Tabellennamen der Tabelle enthält, die den Fremdschlüssel enthält.  
  
## Rückgabewert  
 Ein [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getCrossReference\-Methode wird von der getCrossReference\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
 Das von der getCrossReference\-Methode zurückgegebene Resultset enthält folgende Informationen:  
  
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
>  Weitere Informationen zu den Daten, die von der getCrossReference\-Methode zurückgegeben werden, finden Sie in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation unter "sp\_fkeys \(Transact\-SQL\)".  
  
## Beispiel  
 Im folgenden Beispiel wird dargestellt, wie die getCrossReference\-Methode zur Rückgabe von Informationen über die Primär\- und Fremdschlüsselbeziehung zwischen der Person.Contact\- und der HumanResources.Employee\-Tabelle in der [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)][!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank verwendet wird.  
  
```  
public static void executeGetCrossReference(Connection con) {  
   try {  
      DatabaseMetaData dbmd = con.getMetaData();  
      ResultSet rs = dbmd.getCrossReference("AdventureWorks", "Person", "Contact", null, "HumanResources", "Employee");  
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
  
  