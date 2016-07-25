---
title: "PDO::getAttribute"
ms.custom: na
ms.date: 07/18/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c81833ea-8b8a-459d-8f24-920098da994d
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
  - zh-cn
  - zh-tw
---
# PDO::getAttribute
Ruft den Wert eines vordefinierten PDO- oder Treiberattributs ab.  
  
## Syntax  
  
```  
  
mixed PDO::getAttribute ( $attribute )  
```  
  
#### Parameter  
*$attribute*: Eines der unterstützten Attribute. Eine Liste der unterstützten Attribute finden Sie bei den Anmerkungen.  
  
## Rückgabewert  
Im Erfolgsfall wird der Wert einer Verbindungsoption, eines vordefinierten PDO-Attributs, oder eines benutzerdefinierten Treiberattributs zurückgegeben. Gibt bei einem Fehler NULL zurück.  
  
## Hinweise  
Die nachfolgende Tabelle enthält die Liste mit den unterstützten Attributen:  
  
|Attribut|Verarbeitet von|Unterstützte Werte|Beschreibung|  
|-------------|----------------|--------------------|---------------|  
|PDO::ATTR\_CASE|PDO|PDO::CASE\_LOWER<br /><br />PDO::CASE\_NATURAL<br /><br />PDO::CASE\_UPPER|Dies gibt an, ob die Spaltennamen entweder groß oder klein geschrieben sein sollen. PDO::CASE\_LOWER erzwingt die Schreibung der Spaltennamen in Kleinbuchstaben, PDO::CASE\_NATURAL belässt die Spaltennamen so wie sie aus der Datenbank zurückgegeben wurden und PDO::CASE\_UPPER erzwingt die Schreibung der Spaltennamen in Großbuchstaben.<br /><br />Der Standardwert ist PDO::CASE\_NATURAL.<br /><br />Dieses Attribut kann auch mit PDO::setAttribute eingerichtet werden.|  
|PDO::ATTR\_CLIENT\_VERSION|[!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]|Ein Array von Zeichenfolgen|Beschreibt die Version des Treibers und der verbundenen Bibliotheken Gibt ein Array mit den folgenden Elementen zurück: ODBC-Version \(*MajorVer*.*MinorVer*\), [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Name und Version der nativen Client-DLL, [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]-Version \(*MajorVer*.*MinorVer*.*BuildNumber*.*Revision*\)|  
|PDO::ATTR\_DEFAULT\_FETCH\_MODE|PDO|Siehe PDO-Dokumentation.|Siehe PDO-Dokumentation.|  
|PDO::ATTR\_DRIVER\_NAME|PDO|String|Gibt immer „sqlsrv“ zurück.|  
|PDO::ATTR\_DRIVER\_VERSION|[!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]|String|Gibt die [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]-Version \(*MajorVer*.*MinorVer*.*BuildNumber*.*Revision* an.\)|  
|PDO::ATTR\_ERRMODE|PDO|PDO::ERRMODE\_SILENT<br /><br />PDO::ERRMODE\_WARNING<br /><br />PDO::ERRMODE\_EXCEPTION|Gibt an, wie Fehler vom Treiber behandelt werden sollen.<br /><br />PDO::ERRMODE\_SILENT \(der Standardwert\) legt die Fehlercodes und -informationen fest.<br /><br />PDO::ERRMODE\_WARNING löst eine \_WARNUNG aus.<br /><br />PDO::ERRMODE\_EXCEPTION löst eine Ausnahme aus.<br /><br />Dieses Attribut kann auch mit PDO::setAttribute eingerichtet werden.|  
|PDO::ATTR\_ORACLE\_NULLS|PDO|Siehe PDO-Dokumentation.|Siehe PDO-Dokumentation.|  
|PDO::ATTR\_SERVER\_INFO|[!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]|Array aus drei Elementen|Gibt die aktuelle Datenbank, SQL Server-Version und SQL  Server-Instanz zurück.|  
|PDO::ATTR\_SERVER\_VERSION|[!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]|String|Gibt die SQL Server-Version \(*Major*.*Minor*.*BuildNumber* an.\)|  
|PDO::ATTR\_STATEMENT\_CLASS|PDO|Siehe PDO-Dokumentation.|Siehe PDO-Dokumentation. \(gibt PDOStatement zurück.\)|  
|PDO::ATTR\_STRINGIFY\_FETCHES|PDO|Siehe PDO-Dokumentation.|Siehe PDO-Dokumentation.|  
|PDO::SQLSRV\_ATTR\_CLIENT\_BUFFER\_MAX\_KB\_SIZE|[!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]|1 bis zur Grenze des PHP-Speichers.|Konfiguriert die Größe des Puffers, der das Resultset für einen clientseitigen Cursor enthält.<br /><br />Die Standardeinstellung ist 10240 KB \(10 MB\).<br /><br />Weitere Informationen zu clientseitigen Cursorn finden Sie unter [Cursortypen &#40;SQLSRV Driver&#41;](../Topic/Cursor%20Types%20(SQLSRV%20Driver).md).|  
|PDO::SQLSRV\_ATTR\_DIRECT\_QUERY|[!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]|true<br /><br />false|Legt fest, ob eine direkte oder eine vorbereitete Anweisung ausgeführt wird. Weitere Informationen finden Sie unter [Direkte Anweisungsausführung und vorbereitete Anweisungsausführung im PDO_SQLSRV-Treiber](../Topic/Direct%20Statement%20Execution%20and%20Prepared%20Statement%20Execution%20in%20the%20PDO_SQLSRV%20Driver.md).|  
|PDO::SQLSRV\_ATTR\_ENCODING|[!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]|Einer der folgenden Typen:<br /><br />PDO::SQLSRV\_ENCODING\_UTF8<br /><br />PDO::SQLSRV\_ENCODING\_SYSTEM|Legt die Zeichensatzcodierung fest, die vom Treiber verwendet wird, um mit dem Server zu kommunizieren<br /><br />Der Standardwert ist PDO::SQLSRV\_ENCODING\_UTF8.|  
  
PDO verarbeitet einige der vordefinierten Attribute selbst, während für die Handhabung anderer der Treiber erforderlich ist. Alle benutzerdefinierten Attribute und Verbindungsoptionen werden vom Treiber gehandhabt. Ein nicht unterstütztes Attribut oder eine nicht unterstützte Verbindungsversion geben NULL zurück.  
  
Unterstützung für PDO wurde in Version 2.0 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt.  
  
## Beispiel  
Dieses Beispiel zeigt den Wert des Attributs PDO::ATTR\_ERRMODE, bevor und nachdem der Wert geändert wurde.  
  
```  
<?php  
$database = "AdventureWorks";  
$conn = new PDO( "sqlsrv:server=(local) ; Database = $database", "", "");  
  
$attributes1 = array( "ERRMODE" );  
foreach ( $attributes1 as $val ) {  
     echo "PDO::ATTR_$val: ";  
     var_dump ($conn->getAttribute( constant( "PDO::ATTR_$val" ) ));  
}  
  
$conn->setAttribute( PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION );  
  
$attributes1 = array( "ERRMODE" );  
foreach ( $attributes1 as $val ) {  
     echo "PDO::ATTR_$val: ";  
     var_dump ($conn->getAttribute( constant( "PDO::ATTR_$val" ) ));  
}  
  
// An example using PDO::ATTR_CLIENT_VERSION  
print_r($conn->getAttribute( PDO::ATTR_CLIENT_VERSION ));  
?>  
```  
  
## Siehe auch  
[PDO-Klasse](../content/PDO-Class.md)  
[PDO](http://go.microsoft.com/fwlink/?LinkID=187441)  
  
