---
title: "getFunctions-Methode (SQLServerDatabaseMetaData)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 44335cbd-c84d-4ef3-a6a1-fca7eb7ec768
caps.latest.revision: 20
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
# getFunctions-Methode (SQLServerDatabaseMetaData)
  Ruft eine Beschreibung der System\- und Benutzerfunktionen ab.  
  
## Syntax  
  
```  
  
public ResultSet getFunctions(java.lang.String catalog,  
                       java.lang.String schemaPattern,  
                       java.lang.String functionNamePattern)  
```  
  
#### Parameter  
 *catalog*  
  
 Der Name eines Katalogs in der Datenbank. Bei einer leeren Zeichenfolge \(""\) enthält das Ergebnis die Funktionen ohne einen Katalog. Bei **null** wird der Katalogname nicht für die Suche verwendet.  
  
 *schemaPattern*  
  
 Der Name eines Schemas. Bei einer leeren Zeichenfolge \(""\) enthält das Ergebnis die Funktionen ohne ein Schema. Bei **null** wird der Schemaname nicht für die Suche verwendet.  
  
 *functionNamePattern*  
  
 Der Name einer Funktion.  
  
## Rückgabewert  
 Ein [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese getFunctions\-Methode wird von der getFunctions\-Methode in der java.sql.DatabaseMetaData\-Schnittstelle angegeben.  
  
 Von dieser Methode werden nur die System\- und Benutzerfunktionen zurückgegeben, die dem angegebenen Schema\- und Funktionsnamen entsprechen.  
  
> [!IMPORTANT]  
>  Das zurückgegebene Resultset kann Funktionen enthalten, zu deren Ausführung der aufrufende Benutzer nicht berechtigt ist.  
  
 Jede Funktionsbeschreibung umfasst die folgenden Spalten:  
  
|Name|Typ|Beschreibung|  
|----------|---------|------------------|  
|FUNCTION\_CAT|**String**|Der Name der Datenbank, in der die Funktion gespeichert ist.|  
|FUNCTION\_SCHEM|**String**|Der Name des Schemas, in dem die Funktion gespeichert ist.|  
|FUNCTION\_NAME|**String**|Der Name der Funktion.|  
|NUM\_INPUT\_PARAMS|**int**|Reserviert für zukünftige Verwendung. Gibt derzeit den Wert "\-1" zurück.|  
|NUM\_OUTPUT\_PARAMS|**int**|Reserviert für zukünftige Verwendung. Gibt derzeit den Wert "\-1" zurück.|  
|NUM\_RESULT\_SETS|**int**|Reserviert für zukünftige Verwendung. Gibt derzeit den Wert "\-1" zurück.|  
|REMARKS|**String**|Kommentare zur Funktion.|  
|FUNCTION\_TYPE|**short**|Der Typ der Funktion. Mögliche Werte:<br /><br /> SQL\_PT\_UNKNOWN \(0\)<br /><br /> SQL\_PT\_PROCEDURE \(1\)<br /><br /> SQL\_PT\_FUNCTION \(2\)|  
  
 Alle Beschreibungen im zurückgegebenen Resultset sind nach "FUNCTION\_CAT", "FUNCTION\_SCHEM", "FUNCTION\_NAME" und "SPECIFIC\_NAME" sortiert.  
  
## Siehe auch  
 [SQLServerDatabaseMetaData-Elemente](../content/SQLServerDatabaseMetaData-Members.md)   
 [SQLServerDatabaseMetaData-Klasse](../content/SQLServerDatabaseMetaData-Class.md)  
  
  