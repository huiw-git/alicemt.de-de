---
title: "getColumns-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.getColumns
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: f173fa5d-e114-4a37-a5c4-2baad9ff3af1
caps.latest.revision: 39
caps.handback.revision: 34
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
# getColumns-Methode (SQLServerDatabaseMetaData)
  Ruft eine Beschreibung der Tabellenspalten ab, die im angegebenen Katalog verfügbar sind.  
  
## Syntax  
  
```  
  
public java.sql.ResultSet getColumns(java.lang.String catalog,  
                                     java.lang.String schema,  
                                     java.lang.String table,  
                                     java.lang.String col)  
```  
  
#### Parameter  
 *catalog*  
  
 Ein **String** mit dem Katalognamen.  
  
 *schema*  
  
 Ein **String** mit dem Schemanamenmuster.  
  
 *table*  
  
 Ein **String** mit dem Tabellennamenmuster.  
  
 *col*  
  
 Ein **String** mit dem Spaltennamenmuster.  
  
## Rückgabewert  
 Ein [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getColumns\-Methode wird von der getColumns\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
 Das von der getColumns\-Methode zurückgegebene Resultset enthält folgende Informationen:  
  
|Name|Typ|Beschreibung|  
|----------|---------|------------------|  
|TABLE\_CAT|**String**|Der Name des Katalogs.|  
|TABLE\_SCHEM|**String**|Der Tabellenschemaname.|  
|TABLE\_NAME|**String**|Der Tabellenname.|  
|COLUMN\_NAME|**String**|Der Spaltenname.|  
|DATA\_TYPE|**smallint**|Der SQL\-Datentyp aus "java.sql.Types".|  
|TYPE\_NAME|**String**|Der Name des Datentyps.|  
|COLUMN\_SIZE|**int**|Die Genauigkeit der Spalte.|  
|BUFFER\_LENGTH|**smallint**|Die Übertragungsgröße der Daten.|  
|DECIMAL\_DIGITS|**smallint**|Die Dezimalstellen der Spalte.|  
|NUM\_PREC\_RADIX|**smallint**|Die Basis der Spalte.|  
|NULLABLE|**smallint**|Gibt an, ob in der Spalte NULL\-Werte zulässig sind. Mögliche Werte:<br /><br /> columnNoNulls \(0\)<br /><br /> columnNullable \(1\)|  
|REMARKS|**String**|Die der Spalte zugeordneten Kommentare. **Note:**  Für diese Spalte wird von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] immer NULL zurückgegeben.|  
|COLUMN\_DEF|**String**|Der Standardwert der Spalte.|  
|SQL\_DATA\_TYPE|**smallint**|Der Wert des SQL\-Datentyps, wie er im TYPE\-Feld des Deskriptors angezeigt wird. Diese Spalte entspricht der DATA\_TYPE\-Spalte mit Ausnahme des datetime\-Datentyps und des SQL\-92\-Datentyps interval. Diese Spalte gibt immer einen Wert zurück.|  
|SQL\_DATETIME\_SUB|**smallint**|Untertypcode für den datetime\-Datentyp und den SQL\-92\-Datentyp interval. Bei allen anderen Datentypen gibt diese Spalte NULL zurück.|  
|CHAR\_OCTET\_LENGTH|**int**|Die maximale Anzahl von Bytes in der Spalte.|  
|ORDINAL\_POSITION|**int**|Der Index der Spalte innerhalb der Tabelle.|  
|IS\_NULLABLE|**String**|Gibt an, ob in der Spalte NULL\-Werte zulässig sind.|  
|SS\_IS\_SPARSE|**smallint**|Besitzt den Wert 1, wenn die Spalte eine Spalte mit geringer Dichte ist, andernfalls 0.<sup>1</sup>|  
|SS\_IS\_COLUMN\_SET|**smallint**|Besitzt den Wert 1, wenn die Spalte die column\_set\-Spalte mit geringer Dichte ist, andernfalls 0. <sup>1</sup>|  
|SS\_IS\_COMPUTED|**smallint**|Zeigt an, ob eine TABLE\_TYPE\-Spalte eine berechnete Spalte ist. <sup>1</sup>|  
|IS\_AUTOINCREMENT|**String**|"YES", wenn die Spalte automatisch inkrementiert wird. "NO", wenn die Spalte nicht automatisch inkrementiert wird. "" \(leere Zeichenfolge\), wenn vom Treiber nicht ermittelt werden kann, ob die Spalte automatisch inkrementiert wird. <sup>1</sup>|  
|SS\_UDT\_CATALOG\_NAME|**String**|Der Name des Katalogs, der den benutzerdefinierten Typ \(UDT\) enthält. <sup>1</sup>|  
|SS\_UDT\_SCHEMA\_NAME|**String**|Der Name des Schemas, der den benutzerdefinierten Typ \(UDT\) enthält. <sup>1</sup>|  
|SS\_UDT\_ASSEMBLY\_TYPE\_NAME|**String**|Der benutzerdefinierte Typ \(UDT\) für den vollqualifizierten Namen. <sup>1</sup>|  
|SS\_XML\_SCHEMACOLLECTION\_CATALOG\_NAME|**String**|Der Name des Katalogs, in dem eine XML\-Schemaauflistung definiert ist. Wenn der Katalogname nicht gefunden werden kann, enthält diese Variable eine leere Zeichenfolge. <sup>1</sup>|  
|SS\_XML\_SCHEMACOLLECTION\_SCHEMA\_NAME|**String**|Der Name des Schemas, in dem eine XML\-Schemaauflistung definiert ist. Wenn der Schemaname nicht gefunden werden kann, handelt es sich dabei um eine leere Zeichenfolge. <sup>1</sup>|  
|SS\_XML\_SCHEMACOLLECTION\_NAME|**String**|Name der XML\-Schemaauflistung. Wenn der Schemaname nicht gefunden werden kann, handelt es sich dabei um eine leere Zeichenfolge. <sup>1</sup>|  
|SS\_DATA\_TYPE|**tinyint**|Der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentyp, der von erweiterten gespeicherten Prozeduren verwendet wird.<br /><br /> **Hinweis** Weitere Informationen zu den Datentypen, die von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] zurückgegeben werden, finden Sie in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation unter "Datentypen \(Transact\-SQL\)".|  
  
 \(1\) Diese Spalte ist nicht vorhanden, wenn Sie eine Verbindung mit [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] herstellen.  
  
> [!NOTE]  
>  Weitere Informationen zu den Daten, die von der getColumns\-Methode zurückgegeben werden, finden Sie in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation unter "sp\_columns \(Transact\-SQL\)".  
  
 [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 weist im Vergleich zu früheren Versionen von JDBC Driver folgende Verhaltensänderungen auf:  
  
 Die DATA\_TYPE\-Spalte wurde folgendermaßen geändert:  
  
|[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentyp|Rückgabetyp in JDBC Driver 2.0 \(oder bei Verbindung mit [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)]\) und zugeordnete numerische Konstante|Rückgabetyp in JDBC Driver 3.0 bei Verbindung mit [!INCLUDE[ssKatmai](../content/includes/ssKatmai_md.md)] oder einer höheren Version|  
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|  
|benutzerdefinierter, 8 KB überschreitender Typ|LONGVARBINARY \(\-4\)|VARBINARY \(\-3\)|  
|geography|LONGVARBINARY \(\-4\)|VARBINARY \(\-3\)|  
|geometry|LONGVARBINARY \(\-4\)|VARBINARY \(\-3\)|  
|varbinary\(max\)|LONGVARBINARY \(\-4\)|VARBINARY \(\-3\)|  
|nvarchar\(max\)|LONGVARCHAR \(\-1\) oder LONGNVARCHAR \(JDBC 4\) \(\-16\)|VARCHAR \(12\) oder NVARCHAR \(JDBC 4\) \(\-9\)|  
|varchar\(max\)|LONGVARCHAR \(\-1\)|VARCHAR \(12\)|  
|time|VARCHAR \(12\) oder NVARCHAR \(JDBC 4\) \(\-9\)|TIME \(\-154\)|  
|date|VARCHAR \(12\) oder NVARCHAR \(JDBC 4\) \(\-9\)|DATE \(91\)|  
|datetime2|VARCHAR \(12\) oder NVARCHAR \(JDBC 4\) \(\-9\)|TIMESTAMP \(93\)|  
|datetimeoffset|VARCHAR \(12\) oder NVARCHAR \(JDBC 4\) \(\-9\)|microsoft.sql.Types.DATETIMEOFFSET \(\-155\)|  
  
 Die COLUMN\_SIZE\-Spalte wurde folgendermaßen geändert:  
  
|[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentyp|Rückgabetyp in JDBC Driver 2.0|Rückgabetyp in JDBC Driver 3.0|  
|-------------------------------------------------------------------|------------------------------------|------------------------------------|  
|nvarchar\(max\)|1073741823|2147483647 \(Datenbankmetadaten\)|  
|xml|1073741823|2147483647 \(Datenbankmetadaten\)|  
|benutzerdefinierter Typ mit weniger oder genau 8 KB|8 KB \(Resultset\- und Parametermetadaten\)|Die tatsächliche von der gespeicherten Prozedur zurückgegebene Größe|  
|time||Die Länge \(in Zeichen\) der Zeichenfolgendarstellung des Typs, wobei die maximal zulässige Genauigkeit der Komponente für Sekundenbruchteile vorausgesetzt wird.|  
|date||entspricht "time"|  
|datetime2||entspricht "time"|  
|datetimeoffset||entspricht "time"|  
  
 Die BUFFER\_LENGTH\-Spalte wurde folgendermaßen geändert:  
  
|[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentyp|Rückgabetyp in JDBC Driver 2.0|Rückgabetyp in JDBC Driver 3.0|  
|-------------------------------------------------------------------|------------------------------------|------------------------------------|  
|benutzerdefinierter, 8 KB überschreitender Typ||2147483647|  
  
 Die TYPE\_NAME\-Spalte wurde folgendermaßen geändert:  
  
|[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentyp|Rückgabetyp in JDBC Driver 2.0|Rückgabetyp in JDBC Driver 3.0|  
|-------------------------------------------------------------------|------------------------------------|------------------------------------|  
|varchar\(max\)|text|varchar|  
|varbinary\(max\)|image|varbinary|  
  
 Die DECIMAL\_DIGITS\-Spalte wurde folgendermaßen geändert:  
  
|[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Typ|JDBC Driver 2.0|JDBC Driver 3.0|  
|--------------------------------------------------------------|---------------------|---------------------|  
|time|NULL|7 \(oder – falls angegeben – kleiner\)|  
|date|NULL|NULL|  
|datetime2|NULL|7 \(oder – falls angegeben – kleiner\)|  
|datetimeoffset|NULL|7 \(oder – falls angegeben – kleiner\)|  
  
 Die SQL\_DATA\_TYPE\-Spalte wurde folgendermaßen geändert:  
  
|[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentyp|[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] 2008\-Datenwert in JDBC Driver 2.0|[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] 2008\-Datenwert in JDBC Driver 3.0|  
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|  
|varchar\(max\)|\-10|\-9|  
|nvarchar\(max\)|\-1|\-9|  
|xml|\-10|\-152|  
|benutzerdefinierter Typ mit weniger oder genau 8 KB|\-3|\-151|  
|benutzerdefinierter, 8 KB überschreitender Typ|Nicht verfügbar in JDBC Driver 2.0|\-151|  
|geography|\-4|\-151|  
|geometry|\-4|\-151|  
|hierarchyid|\-4|\-151|  
|time|\-9|92|  
|date|\-9|91|  
|datetime2|\-9|93|  
|datetimeoffset|\-9|\-155|  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie mithilfe der getColumns\-Methode Informationen für die Tabelle "Person.Contact" aus der [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank zurückgegeben werden können.  
  
```  
import java.sql.*;  
public class c1 {  
   public static void main(String[] args) {  
      String connectionUrl = "jdbc:sqlserver://localhost:1433;databaseName=AdventureWorks;integratedsecurity=true";  
  
      Connection con = null;  
      Statement stmt = null;  
      ResultSet rs = null;  
  
      try {  
         Class.forName("com.microsoft.sqlserver.jdbc.SQLServerDriver");  
         con = DriverManager.getConnection(connectionUrl);  
         DatabaseMetaData dbmd = con.getMetaData();  
         rs = dbmd.getColumns("AdventureWorks", "Person", "Contact", "FirstName");  
  
         ResultSet r = dbmd.getColumns(null, null, "Contact", null);  
         ResultSetMetaData rm = r.getMetaData();   
         int noofcols = rm.getColumnCount();  
  
         if (r.next())  
            for (int i = 0 ; i < noofcols ; i++ )  
            System.out.println(rm.getColumnName( i + 1 ) + ": \t\t" + r.getString( i + 1 ));  
      }  
  
      catch (Exception e) {}  
      finally {}  
   }  
}  
```  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Methoden](../content/SQLServerDatabaseMetaData-Methods.md)   
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  