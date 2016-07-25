---
title: "PDO::setAttribute"
ms.custom: na
ms.date: 07/18/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 56f9ee96-e1d2-46cc-b137-38f06a251863
caps.latest.revision: 23
caps.handback.revision: 22
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
# PDO::setAttribute
Legt ein vordefiniertes PDO-Attribut oder ein benutzerdefiniertes Treiberattribut fest.  
  
## Syntax  
  
```  
  
bool PDO::setAttribute ( $attribute, $value );  
```  
  
#### Parameter  
*$attribute*: festzulegendes Attribut Eine Liste der unterstützten Attribute finden Sie bei den Hinweisen.  
  
*$value*: Der Wert \(gemischter Typ\).  
  
## Rückgabewert  
„true“ bei Erfolg, andernfalls „false“.  
  
## Hinweise  
  
|Attribut|Verarbeitet von|Unterstützte Werte|Beschreibung|  
|-------------|----------------|--------------------|---------------|  
|PDO::ATTR\_CASE|PDO|PDO::CASE\_LOWER<br /><br />PDO::CASE\_NATURAL<br /><br />PDO::CASE\_UPPER|Legt fest, ob die Spaltennamen in Groß- oder Kleinbuchstaben geschrieben werden.<br /><br />PDO::CASE\_LOWER bewirkt, das die Spaltennamen in Kleinbuchstaben geschrieben werden.<br /><br />PDO::CASE\_NATURAL \(der Standardwert\) zeigt die Spaltennamen so an, wie sie aus der Datenbank zurückgegeben werden.<br /><br />PDO::CASE\_UPPER bewirkt das die Spaltennamen in Großbuchstaben geschrieben werden.<br /><br />Dieses Attribut kann mit PDO::setAttribute eingerichtet werden.|  
|PDO::ATTR\_DEFAULT\_FETCH\_MODE|PDO|Siehe PDO-Dokumentation.|Siehe PDO-Dokumentation.|  
|PDO::ATTR\_ERRMODE|PDO|PDO::ERRMODE\_SILENT<br /><br />PDO::ERRMODE\_WARNING<br /><br />PDO::ERRMODE\_EXCEPTION|Legt fest, wie der Treiber Fehler meldet.<br /><br />PDO::ERRMODE\_SILENT \(der Standardwert\) legt die Fehlercodes und -informationen fest.<br /><br />PDO::ERRMODE\_WARNING löst eine E\_WARNUNG aus.<br /><br />PDO::ERRMODE\_EXCEPTION bewirkt, dass eine Ausnahme ausgelöst wird.<br /><br />Dieses Attribut kann mit PDO::setAttribute eingerichtet werden.|  
|PDO::ATTR\_ORACLE\_NULLS|PDO|Siehe PDO-Dokumentation.|Legt fest, wie NULL-Werte ausgegeben werden sollen.<br /><br />PDO::NULL\_NATURAL nimmt keine Konvertierung vor.<br /><br />PDO::NULL\_EMPTY\_STRING wandelt eine leere Zeichenfolge in NULL um.<br /><br />PDO::NULL\_TO\_STRING wandelt NULL in eine leere Zeichenfolge um.|  
|PDO::ATTR\_STATEMENT\_CLASS|PDO|Siehe PDO-Dokumentation.|Legt die vom PDOStatement abgeleitete und vom Benutzer bereitgestellte Anweisungsklasse fest.<br /><br />Erfordert `array(string classname, array(mixed constructor_args))`.<br /><br />Weitere Informationen finden Sie in der PDO-Dokumentation.|  
|PDO::ATTR\_STRINGIFY\_FETCHES|PDO|true oder false|Wandelt beim Abruf der Daten Zahlenwerte in Zeichenfolgen um.|  
|PDO::SQLSRV\_ATTR\_CLIENT\_BUFFER\_MAX\_KB\_SIZE|[!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]|1 bis zur Grenze des PHP-Speichers.|Konfiguriert die Größe des Puffers, der das Resultset enthält.<br /><br />Die Standardeinstellung ist 10240 KB \(10 MB\).<br /><br />Weitere Informationen zu Abfragen, die clientseitige Cursor erstellen, finden Sie unter [Cursortypen &#40;PDO_SQLSRV-Treiber&#41;](../Topic/Cursor%20Types%20(PDO_SQLSRV%20Driver).md).|  
|PDO::SQLSRV\_ATTR\_DIRECT\_QUERY|[!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]|true<br /><br />false|Legt fest, ob eine direkte oder eine vorbereitete Anweisung ausgeführt wird. Weitere Informationen finden Sie unter [Direkte Anweisungsausführung und vorbereitete Anweisungsausführung im PDO_SQLSRV-Treiber](../Topic/Direct%20Statement%20Execution%20and%20Prepared%20Statement%20Execution%20in%20the%20PDO_SQLSRV%20Driver.md).|  
|PDO::SQLSRV\_ATTR\_ENCODING|[!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]|PDO::SQLSRV\_ENCODING\_UTF8<br /><br />PDO::SQLSRV\_ENCODING\_SYSTEM|Legt die Zeichensatzcodierung fest, die vom Treiber verwendet wird, um mit dem Server zu kommunizieren.<br /><br />PDO::SQLSRV\_ENCODING\_BINARY wird nicht unterstützt.<br /><br />Der Standardwert ist PDO::SQLSRV\_ENCODING\_UTF8.|  
|PDO::SQLSRV\_ATTR\_QUERY\_TIMEOUT|[!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]|integer|Legt das Abfragetimeout in Sekunden fest.<br /><br />Der Standard ist 0, d. h. dass der Treiber unendlich lange auf Ergebnisse wartet.<br /><br />Negative Zahlen sind nicht zulässig.|  
|PDO::SQLSVR\_CLIENT\_BUFFER\_MAX\_SIZE|[!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]|integer|Legt die Größe des Abfragepuffers fest.<br /><br />Der Standardwert ist 0, was eine unbegrenzte Puffergröße bedeutet.<br /><br />Negative Zahlen sind nicht zulässig.<br /><br />Weitere Informationen zu Abfragen, die clientseitige Cursor erstellen, finden Sie unter [Cursortypen &#40;PDO_SQLSRV-Treiber&#41;](../Topic/Cursor%20Types%20(PDO_SQLSRV%20Driver).md).|  
  
PDO verarbeitet einige der vordefinierten Attribute. Die übrigen müssen vom Treiber verarbeitet werden. Alle benutzerdefinierten Attribute und alle Verbindungsoptionen werden vom Treiber verarbeitet. Ein nicht unterstütztes Attribut, eine nicht unterstützte Verbindungsoption oder ein nicht unterstützter Wert wird laut den Einstellungen in PDO::ATTR\_ERRMODE gemeldet.  
  
Unterstützung für PDO wurde in Version 2.0 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt.  
  
## Beispiel  
Dieses Beispiel zeigt, wie das PDO::ATTR\_ERRMODE-Attribut festgelegt wird.  
  
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
?>  
```  
  
## Siehe auch  
[PDO-Klasse](../content/PDO-Class.md)  
[PDO](http://go.microsoft.com/fwlink/?LinkID=187441)  
  
