---
title: "sqlsrv_close"
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
  - sqlsrv_close
apitype: NA
ms.assetid: 6ac6209c-a134-4f8f-b88b-8eefaa1cbc7f
caps.latest.revision: 25
caps.handback.revision: 24
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
# sqlsrv_close
Schließt die angegebene Verbindung und gibt die zugeordneten Ressourcen frei.  
  
## Syntax  
  
```  
  
sqlsrv_close( resource $conn )  
```  
  
#### Parameter  
*$conn*: Die Verbindung, die geschlossen werden soll.  
  
## Rückgabewert  
Der boolesche Wert **true** , außer die Funktion wird mit einem ungültigen Parameter aufgerufen. Wenn die Funktion mit einem ungültigen Parameter aufgerufen wird, wird **false** zurückgegeben.  
  
> [!NOTE]  
> **NULL** ist ein gültiger Parameter für diese Funktion. Dadurch kann die Funktion mehrmals in einem Skript aufgerufen werden. Wenn Sie z. B. eine Verbindung in einem Fehlerzustand schließen und sie erneut am Ende des Skripts schließen, wird der zweite Aufruf von **sqlsrv\_close** den Wert **true** zurückgeben, da der erste Aufruf von **sqlsrv\_close** \(im Fehlerzustand\) die Verbindungsressource auf **NULL** setzt.  
  
## Beispiel  
Im folgenden Beispiel wird eine Verbindung geschlossen. Das Beispiel setzt voraus, dass SQL Server auf dem lokalen Computer installiert ist. Wenn das Beispiel über die Befehlszeile ausgeführt wird, werden alle Ausgaben in die Konsole geschrieben.  
  
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
  
//-----------------------------------------------  
// Perform operations with connection here.  
//-----------------------------------------------  
  
/* Close the connection. */  
sqlsrv_close( $conn);  
echo "Connection closed.\n";  
?>  
```  
  
## Siehe auch  
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
[Informationen zu den Codebeispielen in der Dokumentation](../content/About-Code-Examples-in-the-Documentation.md)  
  
