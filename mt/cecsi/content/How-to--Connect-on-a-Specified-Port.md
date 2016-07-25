---
title: "Vorgehensweise: Verbinden &#252;ber einen angegebenen Port"
ms.custom: na
ms.date: 06/28/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 65a154d1-375c-439b-a653-7815c9d70ff3
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
# Vorgehensweise: Verbinden &#252;ber einen angegebenen Port
In diesem Thema wird beschrieben, wie über einen angegebenen Port mit der [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]eine Verbindung zu SQL Server hergestellt wird.  
  
### Verbinden über einen angegebenen Port  
  
1.  Stellen Sie sicher, dass der Port, auf den der Server konfiguriert ist, Verbindungen akzeptiert. Informationen zum Konfigurieren eines Servers, um Verbindungen über einen angegebenen Port zu akzeptieren, finden Sie unter [Gewusst wie: Konfigurieren ein Servers zur Überwachung eines bestimmten TCP-Ports \(SQL Server-Konfigurations-Manager\)](http://go.microsoft.com/fwlink/?LinkId=121865).  
  
2.  Fügen Sie den gewünschten Port dem *$serverName*-Parameter der [sqlsrv\_connect](../content/sqlsrv_connect.md)-Funktion hinzu. Trennen Sie den Servernamen und den Port durch ein Komma. Beispielsweise verwenden die folgenden Codezeilen die SQLSRV-Treiber, um zu veranschaulichen, wie die Verbindung mit einem Server namens *myServer* über Port 1521 hergestellt wird:  
  
    ```  
    $serverName = "myServer, 1521";  
    sqlsrv_connect( $serverName );  
    ```  
  
    Die folgenden Codezeilen verwenden den PDO\_SQLSRV-Treiber, um zu veranschaulichen, wie die Verbindung mit einem Server namens *myServer* über Port 1521 hergestellt wird:  
  
    ```  
    $serverName = "(local), 1521";  
    $database = "AdventureWorks";  
    $conn = new PDO( "sqlsrv:server=$serverName;Database=$database", "", "");  
    ```  
  
## Siehe auch  
[Verbinden mit dem Server](../content/Connecting-to-the-Server.md)  
[Programmierhandbuch für den PHP-SQL-Treiber](../content/Programming-Guide-for-PHP-SQL-Driver.md)
[Erste Schritte mit dem PHP-SQL-Treiber](../content/Getting-Started-with-the-PHP-SQL-Driver.md) 
[SQLSRV-Treiber – API-Referenz](../content/SQLSRV-Driver-API-Reference.md)  
[Referenz zum Treiber PDO_SQLSRV](../content/PDO_SQLSRV-Driver-Reference.md)  
  
