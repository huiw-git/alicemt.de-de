---
title: "setPacketSize-Methode (SQLServerDataSource)"
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
  - SQLServerDataSource.setPacketSize
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 5d490edc-a223-4870-a838-784952497e5f
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
# setPacketSize-Methode (SQLServerDataSource)
  Legt die aktuelle Netzwerkpaketgröße \(in Bytes\) für die Kommunikation mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] fest.  
  
## Syntax  
  
```  
  
public void setPacketSize(int packetSize)  
```  
  
#### Parameter  
 *packetSize*  
  
 Ein Wert vom Typ **int** mit der Netzwerkpaketgröße.  
  
## Hinweise  
 Der akzeptable Wertebereich dieser Eigenschaft lautet "\[\-1 | 0 | 512..32767\]". Wenn diese Eigenschaft auf einen Wert außerhalb des zulässigen Bereichs festgelegt wird, wird eine Ausnahme ausgelöst.  
  
 Von der Anwendung wird unter Umständen versucht, die packetSize\-Eigenschaft beim Herstellen einer Verbindung mit SSL \(Secure Sockets Layer\)\-Verschlüsselung festzulegen. Die Paketgröße wird von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] mit dem Server ausgehandelt. Ist die encrypt\-Eigenschaft auf "**true**" festgelegt, und übersteigt die ausgehandelte Paketgröße die SSL\-Datensatzgröße des Standardsicherheitsanbieters der Java Virtual Machine \(JVM\), wird vom Treiber ein Fehler ausgelöst, und die Verbindung wird getrennt.  
  
 Darüber hinaus wird von der Anwendung unter Umständen versucht, die packetSize\-Eigenschaft ohne Anforderung der SSL\-Verschlüsselung festzulegen. In diesem Fall gilt Folgendes: Wird vom Server vorausgesetzt, dass der Clientcomputer die SSL\-Verschlüsselung unterstützt, wird vom Treiber die SSL\-Datensatzgröße des Standardsicherheitsanbieters der JVM überprüft. Übersteigt die packetSize\-Eigenschaft die Datensatzgröße des Standardsicherheitsanbieters der Java Virtual Machine \(JVM\), wird vom Treiber ein Fehler ausgelöst, und die Verbindung wird getrennt.  
  
 Weitere Informationen zum Verwenden von SSL finden Sie unter [Verwenden der SSL-Verschlüsselung](../content/Using-SSL-Encryption.md).  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  