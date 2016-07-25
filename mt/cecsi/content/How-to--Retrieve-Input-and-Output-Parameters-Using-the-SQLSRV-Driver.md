---
title: "How to: Retrieve Input and Output Parameters Using the SQLSRV Driver"
ms.custom: na
ms.date: 06/16/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9a7c5f60-67f9-4968-a3a8-c256ee481da2
caps.latest.revision: 15
caps.handback.revision: 14
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
# How to: Retrieve Input and Output Parameters Using the SQLSRV Driver
In diesem Thema wird veranschaulicht, wie der SQLSRV-Treiber verwendet wird, um eine gespeicherte Prozedur aufzurufen, in der ein Parameter als Eingabe-\/Ausgabeparameter definiert wurde, und wie die Ergebnisse abgerufen werden. Beachten Sie, dass beim Abrufen eines Ausgabe- oder Eingabe-\/Ausgabeparameters alle von der gespeicherten Prozedur zurückgegebenen Ergebnisse verarbeitet werden müssen, bevor auf den Wert des zurückgegebenen Parameters zugegriffen werden kann.  
  
> [!NOTE]  
> Variablen, die auf **NULL**, **DateTime** oder Streamtypen aktualisiert oder initialisiert werden, können nicht als Ausgabeparameter verwendet werden.  
  
## Beispiel  
Im folgenden Beispiel wird eine gespeicherte Prozedur aufgerufen, die genommene Urlaubsstunden von den verfügbaren Urlaubsstunden eines bestimmten Mitarbeiters subtrahiert. Die Variable, die die genommenen Urlaubsstunden darstellt, *$vacationHrs*, wird an die gespeicherte Prozedur als Eingabeparameter übergeben. Nach der Aktualisierung der verfügbaren Urlaubsstunden verwendet die gespeicherte Prozedur den gleichen Parameter, um die Anzahl der verbleibenden Urlaubsstunden zurückzugeben.  
  
> [!NOTE]  
> Initialisieren von *$vacationHrs* auf 4 setzt den Rückgabetyp „PHPTYPE auf“ „Integer“ zurück. Um Datentypintegrität sicherzustellen, sollten Eingabe-\/Ausgabeparameter vor dem Aufruf der gespeicherten Prozedur initialisiert oder der gewünschte Typ für PHPTYPE angegeben werden. Informationen zum Angeben des PHPTYPE finden Sie unter [How to: Specify PHP Data Types](../Topic/How%20to:%20Specify%20PHP%20Data%20Types.md).  
  
Da die gespeicherte Prozedur zwei Ergebnisse zurückgibt, muss [sqlsrv\_next\_result](../content/sqlsrv_next_result.md) aufgerufen werden, nachdem die gespeicherte Prozedur ausgeführt wurde, um den Wert des Ausgabeparameters verfügbar zu machen. Nach dem Aufruf von **sqlsrv\_next\_result** enthält *$vacationHrs* den Wert des Ausgabeparameters, der von der gespeicherten Prozedur zurückgegeben wird.  
  
> [!NOTE]  
> Die Verwendung kanonischer Syntax stellt die empfohlene Vorgehensweise für das Abrufen gespeicherter Prozeduren dar. Weitere Informationen zur kanonischen Syntax finden Sie unter [Aufrufen einer gespeicherten Prozedur](http://go.microsoft.com/fwlink/?linkid=119517).  
  
Das Beispiel setzt voraus, dass SQL Server und die [AdventureWorks](http://go.microsoft.com/fwlink/?LinkID=67739) -Datenbank auf dem lokalen Computer installiert sind. Wenn das Beispiel über die Befehlszeile ausgeführt wird, werden alle Ausgaben in die Konsole geschrieben.  
  
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
  
/* Drop the stored procedure if it already exists. */  
$tsql_dropSP = "IF OBJECT_ID('SubtractVacationHours', 'P') IS NOT NULL  
                DROP PROCEDURE SubtractVacationHours";  
$stmt1 = sqlsrv_query( $conn, $tsql_dropSP);  
if( $stmt1 === false )  
{  
     echo "Error in executing statement 1.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Create the stored procedure. */  
$tsql_createSP = "CREATE PROCEDURE SubtractVacationHours  
                        @EmployeeID int,  
                        @VacationHrs smallint OUTPUT  
                  AS  
                  UPDATE HumanResources.Employee  
                  SET VacationHours = VacationHours - @VacationHrs  
                  WHERE EmployeeID = @EmployeeID;  
                  SET @VacationHrs = (SELECT VacationHours  
                                      FROM HumanResources.Employee  
                                      WHERE EmployeeID = @EmployeeID)";  
  
$stmt2 = sqlsrv_query( $conn, $tsql_createSP);  
if( $stmt2 === false )  
{  
     echo "Error in executing statement 2.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/*--------- The next few steps call the stored procedure. ---------*/  
  
/* Define the Transact-SQL query. Use question marks (?) in place of  
the parameters to be passed to the stored procedure */  
$tsql_callSP = "{call SubtractVacationHours( ?, ?)}";  
  
/* Define the parameter array. By default, the first parameter is an  
INPUT parameter. The second parameter is specified as an INOUT  
parameter. Initializing $vacationHrs to 8 sets the returned PHPTYPE to  
integer. To ensure data type integrity, output parameters should be  
initialized before calling the stored procedure, or the desired  
PHPTYPE should be specified in the $params array.*/  
  
$employeeId = 4;  
$vacationHrs = 8;  
$params = array(   
                 array($employeeId, SQLSRV_PARAM_IN),  
                 array($vacationHrs, SQLSRV_PARAM_INOUT)  
               );  
  
/* Execute the query. */  
$stmt3 = sqlsrv_query( $conn, $tsql_callSP, $params);  
if( $stmt3 === false )  
{  
     echo "Error in executing statement 3.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Display the value of the output parameter $vacationHrs. */  
sqlsrv_next_result($stmt3);  
echo "Remaining vacation hours: ".$vacationHrs;  
  
/*Free the statement and connection resources. */  
sqlsrv_free_stmt( $stmt1);  
sqlsrv_free_stmt( $stmt2);  
sqlsrv_free_stmt( $stmt3);  
sqlsrv_close( $conn);  
?>  
```  
  
## Siehe auch  
[Vorgehensweise: Angeben der Parameterrichtung mit dem SQLSRV-Treiber](../Topic/How%20to:%20Specify%20Parameter%20Direction%20Using%20the%20SQLSRV%20Driver.md)  
[Vorgehensweise: Abrufen von Eingabe-/Ausgabeparametern mit dem SQLSRV-Treiber](../Topic/How%20to:%20Retrieve%20Output%20Parameters%20Using%20the%20SQLSRV%20Driver.md)  
[Abrufen von Daten](../content/Retrieving-Data.md)  
  
