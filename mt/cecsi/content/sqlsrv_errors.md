---
title: "sqlsrv_errors"
ms.custom: na
ms.date: 06/28/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - sqlsrv_errors
apitype: NA
ms.assetid: d1fcffec-f34f-46de-9a0e-343f3b5dbae2
caps.latest.revision: 39
caps.handback.revision: 38
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
# sqlsrv_errors
Gibt erweiterte Informationen über Fehler und\/oder Warnungen für den letzten **sqlsrv**-Vorgang zurück.  
  
Die **sqlsrv\_errors**-Funktion kann eine Information über Fehler und\/oder Warnungen zurückgeben, indem sie diese mit einem der Parameterwerte aufruft, die unten im Abschnitt „Parameter“ angegeben sind.  
  
Standardmäßig werden Warnungen, die bei einem Aufruf einer **sqlsrv** -Funktion generiert werden, als Fehler behandelt. Wenn eine Warnung bei einem Aufruf einer **sqlsrv** -Funktion auftritt, gibt die Funktion „false“ zurück. Jedoch werden Warnungen, die den SQLSTATE-Werten 01000, 01001, 01003 und 01S02 entsprechen, nie als Fehler behandelt.  
  
Die folgende Codezeile deaktiviert das oben genannte Verhalten. Eine Warnung, die durch einen Aufruf einer **sqlsrv** -Funktion generiert wurde, führt nicht dazu, dass die Funktion „false“ zurückgibt:  
  
```  
sqlsrv_configure("WarningsReturnAsErrors", 0);  
```  
  
Die folgende Codezeile aktiviert wieder das Standardverhalten; Warnungen \(mit Ausnahmen wie oben beschrieben\) werden als Fehler behandelt:  
  
```  
sqlsrv_configure("WarningsReturnAsErrors", 1);  
```  
  
Unabhängig von der Einstellung können Warnungen nur durch Aufrufen von **sqlsrv\_errors** abgerufen werden, entweder mit dem Parameterwert **SQLSRV\_ERR\_ALL** oder **SQLSRV\_ERR\_WARNINGS** \(für Einzelheiten siehe Abschnitt „Parameter“ weiter unten\).  
  
## Syntax  
  
```  
  
sqlsrv_errors( [int $errorsAndOrWarnings] )  
```  
  
#### Parameter  
*$errorsAndOrWarnings*\[OPTIONAL\]: eine vordefinierte Konstante Dieser Parameter kann einen der in der folgenden Tabelle aufgeführten Werte annehmen:  
  
|Wert|Beschreibung|  
|---------|---------------|  
|SQLSRV\_ERR\_ALL|Fehler und Warnungen, die beim letzten **sqlsrv** -Funktionsaufruf generiert wurden, werden zurückgegeben.|  
|SQLSRV\_ERR\_ERRORS|Fehler und Warnungen aus dem letzten **sqlsrv** -Funktionsaufruf werden zurückgegeben.|  
|SQLSRV\_ERR\_WARNINGS|Warnungen aus dem letzten **sqlsrv** -Funktionsaufruf werden zurückgegeben.|  
  
Wenn kein Parameterwert angegeben wird, werden Fehler und Warnungen zurückgegeben, die durch den letzten **sqlsrv** -Funktionsaufruf generiert wurden.  
  
## Rückgabewert  
Ein **Array** von Arrays oder **NULL**. Jedes **Array** im zurückgegebenen **Array** enthält drei Schlüssel\-Wert-Paare. In der folgenden Tabelle wird jeder Schlüssel und dessen Beschreibung aufgelistet.  
  
|Key|Beschreibung|  
|-------|---------------|  
|SQLSTATE|Für Fehler, die aus dem ODBC-Treiber stammen, wird von ODBC der Wert SQLSTATE zurückgegeben Weitere Informationen zu SQLSTATE-Werten für ODBC, finden Sie unter [ODBC-Fehlercodes](http://go.microsoft.com/fwlink/?linkid=119618).<br /><br />Für Fehler, die aus den [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]stammen, ein SQLSTATE von IMSSP<br /><br />Für Warnungen, die aus den [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]stammen, ein SQLSTATE von 01SSP|  
|Code|Für Fehler, die vom SQL Server stammen, den systemeigenen SQL Server-Fehlercode<br /><br />Für Fehler, die aus dem ODBC-Treiber stammen, wird von ODBC der Fehlercode zurückgegeben<br /><br />Für Fehler, die aus den [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]oder dem [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] -Fehlercode stammen Weitere Informationen finden Sie unter [Handling Errors and Warnings](../content/Handling-Errors-and-Warnings.md).|  
|message|Eine Beschreibung des Fehlers|  
  
Auf die Arraywerte kann auch mit den numerischen Schlüsseln 0, 1 und 2 zugegriffen werden. Wenn keine Fehler oder Warnungen auftreten, wird **NULL** zurückgegeben.  
  
## Beispiel  
Das folgende Beispiel zeigt auftretende Fehler, die während einer fehlgeschlagene Anweisungsausführung entstehen. \(Bei der Anweisung tritt ein Fehler auf, da **InvalidColumName** kein gültiger Spaltenname in der angegebenen Tabelle ist.\) Das Beispiel setzt voraus, dass SQL Server und die [AdventureWorks](http://go.microsoft.com/fwlink/?LinkID=67739) -Datenbank auf dem lokalen Computer installiert sind. Wenn das Beispiel über die Befehlszeile ausgeführt wird, werden alle Ausgaben in die Konsole geschrieben.  
  
```  
<?php  
/* Connect to the local server using Windows Authentication and   
specify the AdventureWorks database as the database in use. */  
$serverName = "(local)";  
$connectionInfo = array( "Database"=>"AdventureWorks");  
$conn = sqlsrv_connect( $serverName, $connectionInfo);  
if( $conn === false )  
{  
     echo "Could not connect.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Set up a query to select an invalid column name. */  
$tsql = "SELECT InvalidColumnName FROM Sales.SalesOrderDetail";  
  
/* Attempt execution. */  
/* Execution will fail because of the invalid column name. */  
$stmt = sqlsrv_query( $conn, $tsql);  
if( $stmt === false )  
{  
      if( ($errors = sqlsrv_errors() ) != null)  
      {  
         foreach( $errors as $error)  
         {  
            echo "SQLSTATE: ".$error[ 'SQLSTATE']."\n";  
            echo "code: ".$error[ 'code']."\n";  
            echo "message: ".$error[ 'message']."\n";  
         }  
      }  
}  
  
/* Free connection resources */  
sqlsrv_close( $conn);  
?>  
```  
  
## Siehe auch  
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
[Informationen zu den Codebeispielen in der Dokumentation](../content/About-Code-Examples-in-the-Documentation.md)  
  
