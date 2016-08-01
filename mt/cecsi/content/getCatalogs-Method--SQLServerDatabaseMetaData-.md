---
title: "getCatalogs-Methode (SQLServerDatabaseMetaData)"
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
  - SQLServerDatabaseMetaData.getCatalogs
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 7f8bd0f1-f340-4bb9-b559-0a6176124033
caps.latest.revision: 22
caps.handback.revision: 21
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
# getCatalogs-Methode (SQLServerDatabaseMetaData)
  Ruft die Katalognamen ab, die auf dem Server verfügbar sind, mit dem eine Verbindung besteht.  
  
## Syntax  
  
```  
  
public java.sql.ResultSet getCatalogs()  
```  
  
## Rückgabewert  
 Ein [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getCatalogs\-Methode wird von der getCatalogs\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
> [!NOTE]  
>  In SQL Azure müssen Sie für einen Aufruf von **SQLServerDatabaseMetaData.getCatalogs** eine Verbindung mit der Masterdatenbank herstellen. Die Rückgabe sämtlicher Kataloge aus einer Benutzerdatenbank wird von SQL Azure nicht unterstützt. **SQLServerDatabaseMetaData.getCatalogs** verwendet die sys.databases\-Sicht, um die Kataloge abzurufen. Lesen Sie die Beschreibung zu den Berechtigungen unter [sys.databases \(SQL Azure\-Datenbank\)](http://go.microsoft.com/fwlink/?LinkId=217396) durch, um sich mit dem **SQLServerDatabaseMetaData.getCatalogs**\-Verhalten für SQL Azure vertraut zu machen.  
  
 Das von der getCatalogs\-Methode zurückgegebene Resultset enthält folgende Informationen:  
  
|Name|Typ|Beschreibung|  
|----------|---------|------------------|  
|TABLE\_CAT|**String**|Der Name des Katalogs einschließlich Systemdatenbanken in [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)].|  
  
## Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie mithilfe der getCatalogs\-Methode die Namen aller Datenbanken zurückgegeben werden können, die in [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] \(einschließlich Systemdatenbanken\) verfügbar sind.  
  
```  
public static void executeGetCatalogs(Connection con) {  
   try {  
      DatabaseMetaData dbmd = con.getMetaData();  
      ResultSet rs = dbmd.getCatalogs();  
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
  
  