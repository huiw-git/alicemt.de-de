---
title: "sqlsrv_get_config"
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
  - sqlsrv_get_config
apitype: NA
ms.assetid: ce2befc2-af98-45bb-8d41-60f1674dccfc
caps.latest.revision: 7
caps.handback.revision: 6
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
# sqlsrv_get_config
Gibt den aktuellen Wert der angegebenen Konfigurationseinstellung zurück.  
  
## Syntax  
  
```  
  
sqlsrv_get_config( string $setting )  
```  
  
#### Parameter  
*$setting*: Die Konfigurationseinstellung für die der Wert zurückgegeben wird. Eine Liste der konfigurierbaren Einstellungen finden Sie unter [sqlsrv_configure](../content/sqlsrv_configure.md).  
  
## Rückgabewert  
Der Wert der Einstellung, angegeben durch den *$setting* -Parameter. Wenn eine ungültige Einstellung angegeben wird, wird **false** zurückgegeben und ein Fehler wird zur Fehlersammlung hinzugefügt.  
  
## Hinweise  
Wenn **false** von **sqlsrv\_get\_config** zurückgegeben wird, müssen Sie [sqlsrv_errors](../content/sqlsrv_errors.md) aufrufen, um zu bestimmen, ob ein Fehler aufgetreten ist oder ob **false** der Wert der durch den *$setting*-Parameter angegebenen Einstellung ist.  
  
## Siehe auch  
[API-Referenz für den SQLSRV-Treiber](../content/SQLSRV-Driver-API-Reference.md)  
[sqlsrv_configure](../content/sqlsrv_configure.md)  
[sqlsrv_errors](../content/sqlsrv_errors.md)  
  
