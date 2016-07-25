---
title: "Vorgehensweise: Angeben von SQL Server-Datentypen, wenn der SQLSRV-Treiber verwendet wird."
ms.custom: na
ms.date: 06/16/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1fcf73cb-5634-4d89-948f-9326f1dbd030
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
# Vorgehensweise: Angeben von SQL Server-Datentypen, wenn der SQLSRV-Treiber verwendet wird.
In diesem Thema wird veranschaulicht, wie der SQLSRV-Treiber verwendet wird, um den SQL Server-Datentyp für Daten anzugeben, die an den Server gesendet werden. Dieses Thema gilt nicht, wenn der PDO\_SQLSRV-Treiber verwendet wird.  
  
Um den SQL Server-Datentyp anzugeben, müssen Sie das optionale *$params* -Array verwenden, wenn Sie eine Abfrage, die Daten einfügt oder aktualisiert, vorbereiten oder ausführen möchten. Weitere Informationen zur Struktur und Syntax des *$params* -Arrays, finden Sie unter [sqlsrv_query](../content/sqlsrv_query.md) oder [sqlsrv_prepare](../content/sqlsrv_prepare.md).  
  
Die folgenden Schritte fassen zusammen, wie der SQL Server-Datentyp angegeben wird, wenn Daten an den Server gesendet werden:  
  
> [!NOTE]  
> Wenn kein SQL Server-Datentyp festgelegt wurde, werden die Standardtypen verwendet. Informationen zu den SQL Server-Standarddatentypen finden Sie unter [Default SQL Server Data Types](../content/Default-SQL-Server-Data-Types.md).  
  
1.  Definieren Sie eine Transact\-SQL-Abfrage, die Daten einfügt oder aktualisiert. Verwenden Sie Fragezeichen \(?\) als Platzhalter für Parameterwerte in der Abfrage.  
  
2.  Initialisieren oder aktualisieren Sie PHP-Variablen, die den Platzhaltern in der Transact\-SQL-Abfrage entsprechen.  
  
3.  Erstellen Sie das *$params* -Array, das beim Vorbereiten oder Ausführen der Abfrage verwendet werden soll. Beachten Sie, dass jedes Element des *$params* -Arrays auch ein Array sein muss, wenn Sie den SQL Server-Datentyp angeben.  
  
4.  Geben Sie den gewünschten SQL Server-Datentyp mit der entsprechenden **SQLSRV\_SQLTYPE\_\***-Konstanten als vierten Parameter in jedem Subarray des *$params*\-Arrays an. Eine vollständige Liste der **SQLSRV\_SQLTYPE\_\***-Konstanten finden Sie im Abschnitt "SQLTYPES" von [Konstanten &#40; Microsoft-Treiber für PHP für SQLServer &#41;](../content/Constants--Microsoft-Drivers-for-PHP-for-SQL-Server-.md). Im folgenden Code werden z. B. *$changeDate*, *$rate*, und *$payFrequency* jeweils als die SQL Server-Datentypen **datetime**, **money**, und **tinyint** im *$params* -Array angegeben. Da kein SQL Server-Typ für *$employeeId* angegeben ist, und da er mit einem Integer initialisiert wird, wird der  SQL Server-Standardtyp **integer** verwendet.  
  
    ```  
    $employeeId = 5;  
    $changeDate = "2005-06-07";  
    $rate = 30;  
    $payFrequency = 2;  
    $params = array(  
                array($employeeId, null),  
                array($changeDate, null, null, SQLSRV_SQLTYPE_DATETIME),  
                array($rate, null, null, SQLSRV_SQLTYPE_MONEY),  
                array($payFrequency, null, null, SQLSRV_SQLTYPE_TINYINT)  
              );  
    ```  
  
## Beispiel  
Im folgenden Beispiel werden Daten in die *HumanResources.EmployeePayHistory* -Tabelle der Adventureworks-Datenbank eingefügt. SQL Server-Datentypen werden für die Parameter *$changeDate*, *$rate*, und *$payFrequency* angegeben. Für den Parameter *$employeeId* wird der SQL Server-Standardtyp verwendet. Um sicherzustellen, dass die Daten erfolgreich eingefügt wurden, werden dieselben Daten abgerufen und angezeigt.  
  
Dieses Beispiel setzt voraus, dass SQL Server und die [AdventureWorks-Datenbank](http://go.microsoft.com/fwlink/?LinkID=67739) auf dem lokalen Computer installiert sind. Wenn das Beispiel über die Befehlszeile ausgeführt wird, werden alle Ausgaben in die Konsole geschrieben.  
  
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
  
/* Define the query. */  
$tsql1 = "INSERT INTO HumanResources.EmployeePayHistory (EmployeeID,  
                                                        RateChangeDate,  
                                                        Rate,  
                                                        PayFrequency)  
           VALUES (?, ?, ?, ?)";  
  
/* Construct the parameter array. */  
$employeeId = 5;  
$changeDate = "2005-06-07";  
$rate = 30;  
$payFrequency = 2;  
$params1 = array(  
               array($employeeId, null),  
               array($changeDate, null, null, SQLSRV_SQLTYPE_DATETIME),  
               array($rate, null, null, SQLSRV_SQLTYPE_MONEY),  
               array($payFrequency, null, null, SQLSRV_SQLTYPE_TINYINT)  
           );  
  
/* Execute the INSERT query. */  
$stmt1 = sqlsrv_query($conn, $tsql1, $params1);  
if( $stmt1 === false )  
{  
     echo "Error in execution of INSERT.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Retrieve the newly inserted data. */  
/* Define the query. */  
$tsql2 = "SELECT EmployeeID, RateChangeDate, Rate, PayFrequency  
          FROM HumanResources.EmployeePayHistory  
          WHERE EmployeeID = ? AND RateChangeDate = ?";  
  
/* Construct the parameter array. */  
$params2 = array($employeeId, $changeDate);  
  
/*Execute the SELECT query. */  
$stmt2 = sqlsrv_query($conn, $tsql2, $params2);  
if( $stmt2 === false )  
{  
     echo "Error in execution of SELECT.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
/* Retrieve and display the results. */  
$row = sqlsrv_fetch_array( $stmt2 );  
if( $row === false )  
{  
     echo "Error in fetching data.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
echo "EmployeeID: ".$row['EmployeeID']."\n";  
echo "Change Date: ".date_format($row['RateChangeDate'], "Y-m-d")."\n";  
echo "Rate: ".$row['Rate']."\n";  
echo "PayFrequency: ".$row['PayFrequency']."\n";  
  
/* Free statement and connection resources. */  
sqlsrv_free_stmt($stmt1);  
sqlsrv_free_stmt($stmt2);  
sqlsrv_close($conn);  
?>  
```  
  
## Siehe auch  
[Abrufen von Daten](../content/Retrieving-Data.md)  
[Informationen zu den Codebeispielen in der Dokumentation](../content/About-Code-Examples-in-the-Documentation.md)  
[Vorgehensweise: PHP-Datentypen festlegen](../Topic/How%20to:%20Specify%20PHP%20Data%20Types.md)  
[Konvertieren von Datentypen](../content/Converting-Data-Types.md)  
[Vorgehensweise: Senden und Abrufen von UTF-8-Daten mithilfe der eingebauten UTF-8-Unterstützung.](../Topic/How%20to:%20Send%20and%20Retrieve%20UTF-8%20Data%20Using%20Built-In%20UTF-8%20Support.md)  
  
