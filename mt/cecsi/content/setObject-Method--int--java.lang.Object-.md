---
title: "setObject-Methode (int, java.lang.Object)"
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
  - SQLServerPreparedStatement.setObject (int, java.lang.Object)
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 61f19faa-3006-4a1c-974c-55951e3b3000
caps.latest.revision: 22
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
  - sv-se
  - zh-cn
  - zh-tw
---
# setObject-Methode (int, java.lang.Object)
    
## setObject\-Methode \(int, java.lang.Object\)  
 Legt den Wert des angegebenen Parameters unter Verwendung des angegebenen Objekts fest.  
  
## Syntax  
  
```  
  
public final void setObject(int index,  
                            java.lang.Object obj)  
```  
  
#### Parameter  
 *index*  
  
 Ein Wert vom Typ **int** zum Angeben der Parameternummer.  
  
 *obj*  
  
 Ein Objekt.  
  
## Ausnahmen  
 [SQLServerException](../content/SQLServerException-Class.md)  
  
## Hinweise  
 Die setObject\-Methode wird von der setObject\-Methode in der java.sql.PreparedStatement\-Schnittstelle angegeben.  
  
 Vor dem Abrufen der setObject\-Methode, kann von der Anwendung der angegebene Parameter mit einer der folgenden Methoden festgelegt werden:  
  
-   Den set\<Type\>\-Methoden der SQLServerPreparedStatement\- oder SQLServerCallableStatement\-Klasse  
  
-   Den setNull\-Methoden der SQLServerPreparedStatement\- oder SQLServerCallableStatement\-Klasse  
  
-   Der [registerOutParameter](../content/registerOutParameter-Method--SQLServerCallableStatement-.md)\-Methode der SQLServerCallableStatement\-Klasse  
  
 In diesem Fall wird der Parametertyp automatisch festgelegt. Wird die setObject\-Methode von der Anwendung mit NULL für den Objektwert aufgerufen, wird vom Treiber angenommen, dass der Parametertyp von der zuvor aufgerufenen Methode festgelegt wird.  
  
 Ist der obj\-Wert NULL und können für diesen Parameter keine Typinformtionen ermittelt werden, wird der angegebene Parameter vor dem Senden an die Datenbank von der setObject\-Methode in einen CHAR\-Wert konvertiert.  
  
 Ab [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 wird das Verhalten der Methode durch die **sendTimeAsDatetime**\-Verbindungseigenschaft \([Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md)\) und [SQLServerDataSource.setSendTimeAsDatetime](../content/setSendTimeAsDatetime-Method--SQLServerDataSource-.md) geändert.  
  
 Weitere Informationen finden Sie unter [Konfigurieren der Art und Weise, wie java.sql.Time-Werte an den Server gesendet werden](../content/Configuring-How-java.sql.Time-Values-are-Sent-to-the-Server.md).  
  
## Siehe auch  
 [setObject-Methode &#40;ISQLServerPreparedStatement&#41;](../content/setObject-Method--SQLServerPreparedStatement-.md)   
 [SQLServerPreparedStatement-Elemente](../content/SQLServerPreparedStatement-Members.md)   
 [SQLServerPreparedStatement-Klasse](../content/SQLServerPreparedStatement-Class.md)  
  
  