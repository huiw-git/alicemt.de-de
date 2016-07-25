---
title: "sqlsrv_server_info"
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
  - sqlsrv_server_info
apitype: NA
ms.assetid: ef6fe2b7-d267-4379-b948-5626c4684367
caps.latest.revision: 21
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
  - zh-cn
  - zh-tw
---
# sqlsrv_server_info
Gibt Informationen über den Server zurück. Eine Verbindung muss hergestellt werden, bevor Sie diese Funktion aufrufen.  
  
## Syntax  
  
```  
  
sqlsrv_server_info( resource $conn)  
```  
  
#### Parameter  
*$conn*: Die Verbindungsressource, durch die der Client und der Server verbunden sind.  
  
## Rückgabewert  
Ein assoziatives Array mit den folgenden Schlüsseln:  
  
|Key|Beschreibung|  
|-------|---------------|  
|CurrentDatabase|Die Datenbank, die derzeit das Ziel darstellt.|  
|SQLServerVersion|Die Version von SQL Server.|  
|SQLServerName|Der Name des Servers.|  
  
## Beispiel  
Das folgende Beispiel schreibt Server-Informationen an die Konsole, wenn das Beispiel über die Befehlszeile ausgeführt wird.  
  
```  
<?php  
/* Connect to the local server using Windows Authentication. */  
$serverName = "(local)";  
$conn = sqlsrv_connect( $serverName);  
if( $conn === false )  
{  
     echo "Could not connect.\n";  
     die( print_r( sqlsrv_errors(), true));  
}  
  
$server_info = sqlsrv_server_info( $conn);  
if( $server_info )  
{  
      foreach( $server_info as $key => $value)  
      {  
             echo $key.": ".$value."\n";  
      }  
}  
else  
{  
      echo "Error in retrieving server info.\n";  
      die( print_r( sqlsrv_errors(), true));  
}  
  
/* Free connection resources. */  
sqlsrv_close( $conn);  
?>  
```  
  
## Siehe auch  
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
[Informationen zu den Codebeispielen in der Dokumentation](../content/About-Code-Examples-in-the-Documentation.md)  
  
