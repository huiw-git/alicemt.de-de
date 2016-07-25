---
title: "cancel-Methode (ISQLServerStatement)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLServerStatement.cancel
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 276bd9c1-9329-4fc9-9622-ed673c83a12d
caps.latest.revision: 19
caps.handback.revision: 18
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
  - sv-se
  - zh-cn
  - zh-tw
---
# cancel-Methode (ISQLServerStatement)
    
## cancel\-Methode \(ISQLServerStatement\)  
 Bricht die SQL\-Anweisung ab, die derzeit von diesem [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt ausgeführt wird.  
  
## Syntax  
  
```  
  
public final void cancel()  
```  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese cancel\-Methode wird von der cancel\-Methode in der java.sql.Statement\-Schnittstelle angegeben.  
  
 Beim Ausführen einer Anweisung, von der ein einzelnes, umfangreiches und schreibgeschütztes Vorwärts\-Resultset erstellt wird, ist für Sie unter Umständen lediglich eine anfängliche Zeilengruppe des zurückgegebenen Resultsets von Interesse. In diesem Fall kann von der Anwendung vor dem Schließen des Resultsets die [cancel](../content/cancel-Method--SQLServerStatement-.md)\-Methode des zugeordneten Anweisungsobjekts aufgerufen werden, um die Verarbeitungszeit beim Verwerfen der übrigen, nicht benötigten Zeilen zu verringern. Wägen Sie bei der Entscheidung, ob Sie diese Methode verwenden möchten, die eingesparte Verarbeitungszeit gegen die Zeit und den Roundtrip zum Server ab, der zum Abbrechen der Ausführung erforderlich ist.  
  
## Siehe auch  
 [SQLServerStatement-Elemente](../content/SQLServerStatement-Members.md)   
 [SQLServerStatement-Klasse](../content/SQLServerStatement-Class.md)  
  
  