---
title: "setMaxRows-Methode (SQLServerStatement)"
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
  - SQLServerStatement.setMaxRows
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: cccc0667-589b-4655-8ea8-14ae8b2eb9dc
caps.latest.revision: 24
caps.handback.revision: 23
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
# setMaxRows-Methode (SQLServerStatement)
  Legt das Limit für die maximale Anzahl von Zeilen, die ein beliebiges [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt enthalten kann, auf die angegebene Anzahl fest.  
  
## Syntax  
  
```  
  
public final void setMaxRows(int max)  
```  
  
#### Parameter  
 *max*  
  
 Ein Wert vom Typ **int** zum Angeben der maximalen Zeilenanzahl \(oder "0", wenn kein Limit vorhanden ist\).  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese setMaxRows\-Methode wird von der setMaxRows\-Methode in der java.sql.Statement\-Schnittstelle angegeben.  
  
 Diese setMaxRows\-Methode hat keine Auswirkungen auf dynamische, scrollfähige Cursor. Von der Anwendung sollte die Anzahl von Zeilen, die von potenziell umfangreichen Resultsets zurückgegeben wird, mithilfe der SQL\-Syntax "SELECT TOP N" eingeschränkt werden.  
  
 Wenn die setMaxRows\-Methode aufgerufen wird, wird von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] beim Ausführen der Anwendungsabfrage die SQL\-Anweisung "SET ROWCOUNT" ausgeführt. Dadurch wird die maximale Anzahl von Zeilen beschränkt, die von Anweisungen vom Typ [!INCLUDE[tsql](../content/includes/tsql_md.md)] betroffen sind, welche von dieser Abfrage ausgeführt werden \(und nicht nur die Anzahl von Zeilen, die von dieser Abfrage zurückgegeben werden\). Muss von der Anwendung lediglich ein Limit für das oberste [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt festgelegt werden, muss in der Abfrage anstelle der setMaxRows \-Methode die SQL\-Syntax "SELECT TOP N" verwendet werden.  
  
 Weitere Informationen zur SQL\-Anweisung "SET ROWCOUNT" finden Sie in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation im Thema "[SET ROWCOUNT \(Transact\-SQL\)](http://go.microsoft.com/fwlink/?LinkId=139522)".  
  
## Siehe auch  
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  