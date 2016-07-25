---
title: "PDO::getAvailableDrivers"
ms.custom: na
ms.date: 06/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: eab561e6-1229-401a-9482-008c23f9a4e6
caps.latest.revision: 10
caps.handback.revision: 9
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
# PDO::getAvailableDrivers
Gibt ein Array der PDO-Treiber in Ihrer PHP-Installation zurück.  
  
## Syntax  
  
```  
  
array PDO::getAvailableDrivers ();  
```  
  
## Rückgabewert  
Ein Array mit der Liste der PDO-Treiber.  
  
## Hinweise  
Der Name des PDO-Treibers wird verwendet in PDO::\_\_construct, um eine PDO-Instanz zu erstellen.  
  
PDO::getAvailableDrivers muss nicht von PHP-Treibern implementiert werden. Weitere Informationen zu dieser Methode finden Sie in der PHP-Dokumentation.  
  
Unterstützung für PDO wurde in Version 2.0 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt.  
  
## Beispiel  
  
```  
<?php  
print_r(PDO::getAvailableDrivers());  
?>  
```  
  
## Siehe auch  
[PDO-Klasse](../content/PDO-Class.md)  
[PDO](http://go.microsoft.com/fwlink/?LinkID=187441)  
  
