---
title: "PDO::exec"
ms.custom: na
ms.date: 06/16/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 359a87c6-c13a-4518-8f23-a922e7f3b171
caps.latest.revision: 11
caps.handback.revision: 10
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
# PDO::exec
Bereitet eine SQL-Anweisung vor, führt diese in einem einzelnen Funktionsaufruf aus und gibt die Anzahl der von dieser Anweisung betroffenen Zeilen zurück.  
  
## Syntax  
  
```  
  
int PDO::exec ($statement)  
```  
  
#### Parameter  
*$statement*: Eine Zeichenfolge, die die auszuführende SQL-Anweisung enthält.  
  
## Rückgabewert  
Eine ganze Zahl, die über die Anzahl der betroffenen Zeilen Auskunft gibt.  
  
## Hinweise  
Wenn *$statement* mehrere SQL-Anweisungen enthält, wird nur die Anzahl der von der letzten Anweisung betroffenen Zeilen in der Zahl widergespiegelt.  
  
PDO::exec Gibt keine Ergebnisse für eine SELECT Anweisung zurück.  
  
Die folgenden Attribute beeinflussen das Verhalten der PDO::exec:  
  
-   PDO::ATTR\_DEFAULT\_FETCH\_MODE  
  
-   PDO::SQLSRV\_ATTR\_ENCODING  
  
-   PDO::SQLSRV\_ATTR\_QUERY\_TIMEOUT  
  
Weitere Informationen finden Sie unter [PDO::setAttribute](../Topic/PDO::setAttribute.md) .  
  
Unterstützung für PDO wurde in Version 2.0 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt.  
  
## Beispiel  
Dieses Beispiel löscht Zeilen in Tabelle 1, die in Spalte 1 „xxxyy“ aufweisen. Anschließend meldet das Beispiel, wie viele Zeilen gelöscht wurden.  
  
```  
<?php  
   $c = new PDO( "sqlsrv:server=(local)");  
  
   $c->exec("use Test");  
   $ret = $c->exec("delete from Table1 where col1 = 'xxxyy'");  
   echo $ret;  
?>  
```  
  
## Siehe auch  
[PDO-Klasse](../content/PDO-Class.md)  
[PDO](http://go.microsoft.com/fwlink/?LinkID=187441)  
  
