---
title: "sqlsrv_configure"
ms.custom: na
ms.date: 07/18/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - sqlsrv_configure
apitype: NA
ms.assetid: 9393f975-a4ef-4c50-b4dd-14892fc55cc9
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
# sqlsrv_configure
Ändert die Einstellungen für die Fehlerbehandlung und Protokollierungsoptionen.  
  
## Syntax  
  
```  
  
sqlsrv_configure( string $setting, mixed $value )  
```  
  
#### Parameter  
*$setting*: Name der zu konfigurierenden Einstellung. Die Liste der Einstellungen finden Sie in der folgenden Tabelle.  
  
*$value*: Wert, der der Einstellung hinzugefügt werden soll, die im *$setting* Parameter angegeben ist. Die möglichen Werte für diesen Parameter hängen von der angegebenen Einstellung ab. In der folgenden Tabelle sind die Kombinationsmöglichkeiten aufgelistet:  
  
|Einstellung|Mögliche Werte für $value-Parameter \(entsprechende Ganzzahl in Klammern\)|Standardwert|  
|-----------|------------------------------------------------------------------------------|-----------------|  
|ClientBufferMaxKBSize<sup>1</sup>|Eine nicht negative Zahl, bis hin zur PHP-Speichergrenze.<br /><br />Null \(0\) bedeutet keine Beschränkung für die Größe des Puffers.|10240|  
|LogSeverity<sup>2</sup>|SQLSRV\_LOG\_SEVERITY\_ALL \(\-1\)<br /><br />SQLSRV\_LOG\_SEVERITY\_ERROR \(1\)<br /><br />SQLSRV\_LOG\_SEVERITY\_NOTICE \(4\)<br /><br />SQLSRV\_LOG\_SEVERITY\_WARNING \(2\)|SQLSRV\_LOG\_SEVERITY\_ERROR \(1\)|  
|LogSubsystems<sup>2</sup>|SQLSRV\_LOG\_SYSTEM\_ALL \(\-1\)<br /><br />SQLSRV\_LOG\_SYSTEM\_CONN \(2\)<br /><br />SQLSRV\_LOG\_SYSTEM\_INIT \(1\)<br /><br />SQLSRV\_LOG\_SYSTEM\_OFF \(0\)<br /><br />SQLSRV\_LOG\_SYSTEM\_STMT \(4\)<br /><br />SQLSRV\_LOG\_SYSTEM\_UTIL \(8\)|SQLSRV\_LOG\_SYSTEM\_OFF \(0\)|  
|WarningsReturnAsErrors<sup>3</sup>|**true** \(1\) oder **false** \(0\)|**true** \(1\)|  
  
## Rückgabewert  
Wenn **sqlsrv\_configure** mit nicht unterstützten Einstellungen oder Werten aufgerufen wird, gibt die Funktion **false** zurück. Andernfalls gibt die Funktion **true**zurück.  
  
## Hinweise  
\(1\) Weitere Informationen zu clientseitigen Cursorn finden Sie unter [Cursortypen &#40;SQLSRV-Treiber&#41;](../Topic/Cursor%20Types%20(SQLSRV%20Driver).md).  
  
\(2\) Weitere Informationen zur Protokollierung von Aktivitäten finden Sie unter [Logging Activity](../content/Logging-Activity.md) (Protokollaktivität).  
  
\(3\) Weitere Informationen zum Konfigurieren der Fehler- und Warnungsbehandlung finden Sie unter [Gewusst wie: Konfigurieren der Behandlung von Fehlern und Warnungen unter Verwendung des SQLSRV-Treibers](../Topic/How%20to:%20Configure%20Error%20and%20Warning%20Handling%20Using%20the%20SQLSRV%20Driver.md).  
  
## Siehe auch  
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
[Programmierhandbuch für den PHP-SQL-Treiber](../content/Programming-Guide-for-PHP-SQL-Driver.md) 
  
