---
title: "SQLServerCallableStatement-Klasse"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 30710a63-c05d-47d9-9cf9-c087a1c76373
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
  - sv-se
  - zh-cn
  - zh-tw
---
# SQLServerCallableStatement-Klasse
  Mit dieser Klasse kann der gespeicherte Prozedurname angegeben werden, der mit Eingabe\- und Ausgabeparametern aufgerufen wird. Mit dieser Klasse kann der Rückgabestatus mit der Syntax "? ?\= call\( ?, ..\) \-Syntax abgerufen werden.  
  
 **Paket:** com.microsoft.sqlserver.jdbc  
  
 **Implementiert:** [ISQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)  
  
 **Erweitert:** [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)  
  
## Syntax  
  
```  
  
public final class SQLServerCallableStatement  
```  
  
## Hinweise  
 Mit SQLServerCallableStatement wird der Name der gespeicherten Prozedur angegeben, der gemeinsam mit Ein\- und Ausgabeparametern aufgerufen werden soll. SQLServerCallableStatement ermöglicht auch den Abruf des Rückgabestatuswerts mit der `? = call( ?, ..)`\-Syntax.  
  
 Diese Klasse unterstützt das Entpacken in die Klasse SQLServerCallableStatement, die Schnittstelle ISQLServerCallableStatement, die Schnittstelle  java.sql.CallableStatement sowie die Klassen und Schnittstellen, die von  SQLServerPreparedStatement für das Entpacken unterstützt werden. Weitere Informationen finden Sie unter [Wrapper und Schnittstellen](../content/Wrappers-and-Interfaces.md).  
  
 Wenn eine der SQLServerCallableStatement\-Set\-Methoden für einen Typ aufgerufen wird und der betreffende Typ mit dem von [registerOutParameter](../content/registerOutParameter-Method--SQLServerCallableStatement-.md) angegebenen Typ in Konflikt steht, wird der von der letzten SQLServerCallableStatement\-Set\-Methode angegebene Typ verwendet. Dies kann jedoch zu Konvertierungsfehlern aufgrund von inkompatiblen Datentypen führen. Wird keine SQLServerCallableStatement\-Set\-Methode aufgerufen, wird der Typ verwendet, der mit dem ersten [registerOutParameter](../content/registerOutParameter-Method--SQLServerCallableStatement-.md)\-Aufruf angegeben wird.  
  
 [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 folgt der JDBC 4.0\-Empfehlung, die besagt, dass ein Resultset und Updatezählungen abgerufen werden müssen, bevor OUT\-Parameter abgerufen werden. Sollten OUT\-Parameter vor Abschluss der Verarbeitung des Resultsets und der Updatezählungen abgerufen werden, gehen alle noch nicht verarbeiteten Resultsets und Updatezählungen verloren.  
  
## Siehe auch  
 [SQLServerCallableStatement-Elemente](../content/SQLServerCallableStatement-Members.md)   
 [API-Referenz für den JDBC-Treiber](../content/JDBC-Driver-API-Reference.md)  
  
  