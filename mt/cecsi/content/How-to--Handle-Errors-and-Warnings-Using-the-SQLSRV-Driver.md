---
title: "Vorgehensweise: Fehlerbehandlung und Warnungen bei Verwendung des SQLSRV-Treibers"
ms.custom: na
ms.date: 06/28/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fa231d60-4c06-4137-89e8-097c28638c5d
caps.latest.revision: 18
caps.handback.revision: 17
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
# Vorgehensweise: Fehlerbehandlung und Warnungen bei Verwendung des SQLSRV-Treibers
Standardmäßig werden im SQLSRV-Treiber Warnungen als Fehler behandelt; ein Aufruf einer **sqlsrv** -Funktion, die einen Fehler oder eine Warnung generiert, gibt **false**zurück. Dieses Thema demonstriert wie dieses Standardverhalten abgestellt wird und wie Warnungen separat von Fehlern behandelt werden.  
  
> [!NOTE]  
> Es gibt einige Ausnahmen zum Standardverhalten, dass Warnungen als Fehler behandelt werden. Warnungen, die den SQLSTATE-Werten 01000, 01001, 01003 und 01S02 entsprechen, werden nie als Fehler behandelt.  
  
## Beispiel  
Das folgende Codebeispiel verwendet zwei benutzerdefinierte Funktionen, **DisplayErrors** und **DisplayWarnings**, um Fehler und Warnungen zu behandeln. Das Beispiel zeigt, wie Warnungen und Fehler folgendermaßen getrennt behandelt werden:   
  
1.  Schaltet das Standardverhalten, mit dem Warnungen als Fehler behandelt werden, ab.  
  
2.  Erstellt eine gespeicherte Prozedur, welche die Urlaubsstunden eines Arbeitnehmers aktualisiert und die verbleibenden Urlaubsstunden als einen Ausgabeparameter zurück gibt. Falls die verfügbaren Urlaubsstunden des Arbeitnehmers negativ sind, gibt die gespeicherte Prozedur eine Warnung aus.  
  
3.  Aktualisiert die Urlaubsstunden für mehrere Arbeitnehmer, indem es die gespeicherte Prozedur für jeden Arbeitnehmer aufruft, und zeigt die passenden Meldungen für jede anfallende Warnung oder jeden anfallenden Fehler an.  
  
4.  Zeigt die verbleibenden Urlaubsstunden für jeden Arbeitnehmer an.  
  
Beachten Sie, dass beim ersten Aufruf einer **sqlsrv**-Funktion \([sqlsrv\_configure](../content/sqlsrv_configure.md)\) Warnungen als Fehler behandelt werden. Da Warnungen der Fehlersammlung hinzugefügt werden, müssen Sie unabhängig von den Fehlern nicht nochmals nach Warnungen suchen. In den folgenden Aufrufen der Funktion **sqlsrv** werden Warnungen hingegen nicht als Fehler behandelt.,Sie müssen das Auftreten Warnungen und Fehlern also explizit überprüfen.  
  
Beachten Sie auch, dass der Beispielcode nach jedem Anruf einer **sqlsrv** -Funktion nach Fehlern sucht. Dies ist die empfohlene Vorgehensweise.  
  
Dieses Beispiel setzt voraus, dass SQL Server und die [AdventureWorks-Datenbank](http://go.microsoft.com/fwlink/?LinkID=67739) auf dem lokalen Computer installiert sind. Wenn das Beispiel über die Befehlszeile ausgeführt wird, werden alle Ausgaben in die Konsole geschrieben. Wenn das Beispiel in einer neuen Installation der AdventureWorks-Datenbank ausgeführt wird, produziert es drei Warnungen und zwei Fehler. Die ersten beiden Warnungen sind Standardwarnungen, die beim Herstellen einer Verbindung mit einer Datenbank ausgegeben werden. Die dritte Warnung tritt auf, weil die verfügbaren Urlaubsstunden des Arbeitnehmers auf einen negativen Wert aktualisiert werden. Dieser Fehler tritt auf, weil die verfügbaren Urlaubsstunden des Arbeitnehmers auf einen Wert von weniger als \-40 Stunden aktualisiert werden. Dies verletzt eine der Einschränkungen aus der Tabelle.  
  
```  
<?php  
/* Turn off the default behavior of treating errors as warnings.  
Note: Turning off the default behavior is done here for demonstration  
purposes only. If setting the configuration fails, display errors and  
exit the script. */  
if( sqlsrv_configure("WarningsReturnAsErrors", 0) === false)  
{  
     DisplayErrors();  
     die;  
}  
  
/* Connect to the local server using Windows Authentication and   
specify the AdventureWorks database as the database in use. */  
$serverName = "(local)";  
$connectionInfo = array("Database"=>"AdventureWorks");  
$conn = sqlsrv_connect( $serverName, $connectionInfo);  
  
/* If the connection fails, display errors and exit the script. */  
if( $conn === false )  
{  
     DisplayErrors();  
     die;  
}  
/* Display any warnings. */  
DisplayWarnings();  
  
/* Drop the stored procedure if it already exists. */  
$tsql1 = "IF OBJECT_ID('SubtractVacationHours', 'P') IS NOT NULL  
                DROP PROCEDURE SubtractVacationHours";  
$stmt1 = sqlsrv_query($conn, $tsql1);  
  
/* If the query fails, display errors and exit the script. */  
if( $stmt1 === false)  
{  
     DisplayErrors();  
     die;  
}  
/* Display any warnings. */  
DisplayWarnings();  
  
/* Free the statement resources. */  
sqlsrv_free_stmt( $stmt1 );  
  
/* Create the stored procedure. */  
$tsql2 = "CREATE PROCEDURE SubtractVacationHours  
                  @EmployeeID int,  
                  @VacationHours smallint OUTPUT  
              AS  
                  UPDATE HumanResources.Employee  
                  SET VacationHours = VacationHours - @VacationHours  
                  WHERE EmployeeID = @EmployeeID;  
                  SET @VacationHours = (SELECT VacationHours    
                                       FROM HumanResources.Employee  
                                       WHERE EmployeeID = @EmployeeID);  
              IF @VacationHours < 0   
              BEGIN  
                PRINT 'WARNING: Vacation hours are now less than zero.'  
              END;";  
$stmt2 = sqlsrv_query( $conn, $tsql2 );  
  
/* If the query fails, display errors and exit the script. */  
if( $stmt2 === false)  
{  
     DisplayErrors();  
     die;  
}  
/* Display any warnings. */  
DisplayWarnings();  
  
/* Free the statement resources. */  
sqlsrv_free_stmt( $stmt2 );  
  
/* Set up the array that maps employee ID to used vacation hours. */  
$emp_hrs = array (7=>4, 8=>5, 9=>8, 11=>50);  
  
/* Initialize variables that will be used as parameters. */  
$employeeId = 0;  
$vacationHrs = 0;  
  
/* Set up the parameter array. */  
$params = array(  
                 array(&$employeeId, SQLSRV_PARAM_IN),  
                 array(&$vacationHrs, SQLSRV_PARAM_INOUT)  
                );  
  
/* Define and prepare the query to substract used vacation hours. */  
$tsql3 = "{call SubtractVacationHours(?, ?)}";  
$stmt3 = sqlsrv_prepare($conn, $tsql3, $params);  
  
/* If the statement preparation fails, display errors and exit the script. */  
if( $stmt3 === false)  
{  
     DisplayErrors();  
     die;  
}  
/* Display any warnings. */  
DisplayWarnings();  
  
/* Loop through the employee=>vacation hours array. Update parameter  
 values before statement execution. */  
foreach(array_keys($emp_hrs) as $employeeId)  
{  
     $vacationHrs = $emp_hrs[$employeeId];  
     /* Execute the query.  If it fails, display the errors. */  
     if( sqlsrv_execute($stmt3) === false)  
     {  
          DisplayErrors();  
          die;  
     }  
     /* Display any warnings. */  
     DisplayWarnings();  
  
     /*Move to the next result returned by the stored procedure. */  
     if( sqlsrv_next_result($stmt3) === false)  
     {  
          DisplayErrors();  
          die;  
     }  
     /* Display any warnings. */  
     DisplayWarnings();  
  
     /* Display updated vacation hours. */  
     echo "EmployeeID $employeeId has $vacationHrs ";  
     echo "remaining vacation hours.\n";  
}  
  
/* Free the statement and connection resources. */  
sqlsrv_free_stmt( $stmt3 );  
sqlsrv_close( $conn );  
  
/* ------------- Error Handling Functions --------------*/  
function DisplayErrors()  
{  
     $errors = sqlsrv_errors(SQLSRV_ERR_ERRORS);  
     foreach( $errors as $error )  
     {  
          echo "Error: ".$error['message']."\n";  
     }  
}  
  
function DisplayWarnings()  
{  
     $warnings = sqlsrv_errors(SQLSRV_ERR_WARNINGS);  
     if(!is_null($warnings))  
     {  
          foreach( $warnings as $warning )  
          {  
               echo "Warning: ".$warning['message']."\n";  
          }  
     }  
}  
?>  
```  
  
## Siehe auch  
[Vorgehensweise: Konfigurieren der Behandlung von Fehlern und Warnungen unter Verwendung des SQLSRV-Treibers](../Topic/How%20to:%20Configure%20Error%20and%20Warning%20Handling%20Using%20the%20SQLSRV%20Driver.md)  
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
  
