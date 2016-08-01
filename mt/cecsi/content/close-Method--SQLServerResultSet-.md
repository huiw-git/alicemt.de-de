---
title: "close-Methode (ISQLServerResultSet)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLServerResultSet.close
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 8f3adf5b-874e-4cf2-b4ef-672dda42d77a
caps.latest.revision: 14
caps.handback.revision: 13
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
# close-Methode (ISQLServerResultSet)
    
## close\-Methode \(ISQLServerResultSet\)  
 Gibt die Datenbank\- und JDBC\-Ressourcen dieses [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts umgehend frei, sodass nicht darauf gewartet werden muss, bis dieser Vorgang beim automatischen Schließen ausgeführt wird.  
  
## Syntax  
  
```  
  
public void close()  
```  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Diese close\-Methode wird von der close\-Methode in der java.sql.ResultSet\-Schnittstelle angegeben.  
  
 Ein SQLServerResultSet\-Objekt wird vom [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekt, durch das es generiert wurde, automatisch geschlossen, wenn das SQLServerStatement\-Objekt geschlossen, erneut ausgeführt oder zum Abrufen des nächsten Ergebnisses aus einer Sequenz mit mehreren Ergebnissen verwendet wird. Ein SQLServerResultSet\-Objekt wird auch dann automatisch geschlossen, wenn eine automatische Speicherbereinigung stattfindet.  
  
 Beim Ausführen einer Anweisung, von der ein einzelnes, umfangreiches und schreibgeschütztes Vorwärts\-Resultset erstellt wird, ist für Sie unter Umständen lediglich eine anfängliche Zeilengruppe des zurückgegebenen Resultsets von Interesse. In diesem Fall kann von der Anwendung vor dem Schließen des Resultsets die [cancel](../content/cancel-Method--SQLServerStatement-.md)\-Methode des zugeordneten Anweisungsobjekts aufgerufen werden, um die Verarbeitungszeit beim Verwerfen der übrigen, nicht benötigten Zeilen zu verringern. Wägen Sie bei der Entscheidung, ob Sie diese Methode verwenden möchten, die eingesparte Verarbeitungszeit gegen die Zeit und den Roundtrip zum Server ab, der zum Abbrechen der Ausführung erforderlich ist.  
  
## Siehe auch  
 [ISQLServerResultSet-Elemente](../content/SQLServerResultSet-Members.md)   
 [SQLServerResultSet-Klasse](../content/SQLServerResultSet-Class.md)  
  
  