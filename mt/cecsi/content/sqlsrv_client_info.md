---
title: "sqlsrv_client_info"
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
  - sqlsrv_client_info
apitype: NA
ms.assetid: 3e2d3679-436a-45d8-8bdc-7c633b65a720
caps.latest.revision: 47
caps.handback.revision: 46
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
# sqlsrv_client_info
Gibt Informationen über die Liste der Verbindungen und den Client-Stack zurück.  
  
## Syntax  
  
```  
  
sqlsrv_client_info( resource $conn)  
```  
  
#### Parameter  
*$conn*: Die Verbindungsressource, mit der der Client verbunden ist.  
  
## Rückgabewert  
Ein assoziatives Array mit Schlüsseln, die in der folgenden Tabelle beschrieben werden, oder **false** , wenn die Verbindungsressource NULL ist.  
  
**Für PHP für SQL Server-Versionen 3.2 und 3.1**:  
  
|Key|Beschreibung|  
|-------|---------------|  
|DriverDllName|MSODBCSQL11.DLL \(ODBC Driver 11 für SQL Server\)|  
|DriverODBCVer|ODBC-Version \(xx.yy\)|  
|DriverVer|ODBC Driver 11 for SQL Server DLL-Version:<br /><br />xx.yy.zzzz (\([!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] Version 3.2 oder 3.1\)|  
|ExtensionVer|php\_sqlsrv.dll-Version:<br /><br />3.2.xxxx.x \(für [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]-Version 3.2\)<br /><br />3.1.xxxx.x \(für [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]-Version 3.1\)|  
  
**Für PHP für SQL Server-Versionen 3.0 und 2.0**:  
  
|Key|Beschreibung|  
|-------|---------------|  
|DriverDllName|SQLNCLI10.DLL \([!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]-Version 2.0\)|  
|DriverODBCVer|ODBC-Version \(xx.yy\)|  
|DriverVer|SQL Server Native Client DLL-Version<br /><br />10.50.xxx \([!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]-Version 2.0\)|  
|ExtensionVer|php\_sqlsrv.dll-Version:<br /><br />2.0.xxxx.x \([!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]-Version 2.0\)|  
  
## Beispiel  
Das folgende Beispiel schreibt Client-Informationen an die Konsole, wenn das Beispiel über die Befehlszeile ausgeführt wird. Das Beispiel setzt voraus, dass SQL Server auf dem lokalen Computer installiert ist. Wenn das Beispiel über die Befehlszeile ausgeführt wird, werden alle Ausgaben in die Konsole geschrieben.  
  
```  
<?php  
/*Connect to the local server using Windows Authentication and   
specify the AdventureWorks database as the database in use. */  
$serverName = "(local)";  
$conn = sqlsrv_connect( $serverName);  
  
if( $conn === false )  
{  
     echo "Could not connect.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
if( $client_info = sqlsrv_client_info( $conn))  
{  
       foreach( $client_info as $key => $value)  
      {  
              echo $key.": ".$value."\n";  
      }  
}  
else  
{  
       echo "Client info error.\n";  
}  
  
/* Close connection resources. */  
sqlsrv_close( $conn);  
?>  
```  
  
## Siehe auch  
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
[Informationen zu den Codebeispielen in der Dokumentation](../content/About-Code-Examples-in-the-Documentation.md)  
  
