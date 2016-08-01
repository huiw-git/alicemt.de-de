---
title: "SQLServerNClob-Elemente"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b063f191-175e-4430-aab7-d88907f4ebec
caps.latest.revision: 11
caps.handback.revision: 11
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
# SQLServerNClob-Elemente
    
## SQLServerNClob\-Elemente  
 In den folgenden Tabellen sind die Elemente aufgeführt, die von der [SQLServerNClob](../content/SQLServerNClob-Class.md)\-Klasse verfügbar gemacht werden.  
  
### Konstruktoren  
 Keine  
  
### Felder  
 Keine  
  
### Geerbte Felder  
 Keine  
  
### Methoden  
  
|Name|Beschreibung|  
|----------|------------------|  
|[free](../content/free-Method--SQLServerNClob-.md)|Mit dieser Methode werden das **NCLOB**\-Objekt sowie die von diesem verwendeten Ressourcen freigegeben.|  
|[getAsciiStream](../content/getAsciiStream-Method--SQLServerNClob-.md)|Ruft den vom **java.sql.NClob**\-Objekt angegebenen **NCLOB**\-Wert als ASCII\-Datenstrom ab.|  
|[getCharacterStream](../content/getCharacterStream-Method--SQLServerNClob-.md)|Ruft den vom **java.sql.NClob**\-Objekt angegebenen **NCLOB**\-Wert ab.|  
|[getSubString](../content/getSubString-Method--SQLServerNClob-.md)|Ruft eine Kopie der angegebenen Teilzeichenfolge im vom **java.sql.NClob**\-Objekt angegebenen **NCLOB**\-Wert ab.|  
|[length](../content/length-Method--SQLServerNClob-.md)|Ruft die Anzahl von Zeichen im vom **java.sql.NClob**\-Objekt angegebenen **NCLOB**\-Wert ab.|  
|[position](../content/position-Method--SQLServerNClob-.md)|Ruft die Zeichenposition des angegebenen **java.sql.NClob**\-Objekts oder der Zeichenfolge in **java.sql.NClob** auf der Grundlage der angegebenen Startposition ab.|  
|[setAsciiStream](../content/setAsciiStream-Method--SQLServerNClob-.md)|Ruft einen Datenstrom ab, der verwendet wird, um ab der angegebenen Position ASCII\-Zeichen in den **NCLOB**\-Wert zu schreiben, der von diesem **java.sql.NClob**\-Objekt dargestellt wird.|  
|[setCharacterStream](../content/setCharacterStream-Method--SQLServerNClob-.md)|Ruft einen Datenstrom ab, der verwendet wird, um ab der angegebenen Position einen Unicode\-Zeichendatenstrom in den **NCLOB**\-Wert zu schreiben, der von diesem **java.sql.NClob**\-Objekt dargestellt wird.|  
|[setString](../content/setString-Method--SQLServerNClob-.md)|Schreibt den angegebenen **String** ab der angegebenen Position in das **NCLOB**.|  
|[truncate](../content/truncate-Method--SQLServerNClob-.md)|Kürzt den **NCLOB**\-Wert auf die angegebene Länge.|  
  
### Geerbte Methoden  
  
|Klasse geerbt von:|Methoden|  
|------------------------|--------------|  
|java.lang.Object|clone, equals, finalize, getClass, hashCode, notify, notifyAll, toString, wait|  
|java.sql.Clob|free, getAsciiStream, getCharacterStream, getSubString, length, position, setAsciiStream, setCharacterStream, setString, truncate|  
  
## Siehe auch  
 [SQLServerClob-Klasse](../content/SQLServerClob-Class.md)  
  
  