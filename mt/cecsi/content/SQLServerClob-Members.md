---
title: "SQLServerClob-Elemente"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apitype: Assembly
ms.assetid: 7db785ca-edd5-4833-8053-17fdbf87279a
caps.latest.revision: 15
caps.handback.revision: 15
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
# SQLServerClob-Elemente
    
## SQLServerClob\-Elemente  
 In den folgenden Tabellen sind die Elemente aufgeführt, die von der [SQLServerClob](../content/SQLServerClob-Class.md)\-Klasse verfügbar gemacht werden.  
  
### Konstruktoren  
  
|Name|Beschreibung|  
|----------|------------------|  
|[SQLServerClob](../content/SQLServerClob-Constructor--SQLServerConnection--java.lang.String-.md)|Initialisiert eine neue Instanz der SQLServerClob\-Klasse.|  
  
### Felder  
 Keine  
  
### Geerbte Felder  
 Keine  
  
### Methoden  
  
|Name|Beschreibung|  
|----------|------------------|  
|[free](../content/free-Method--SQLServerClob-.md)|Mit dieser Methode werden das CLOB sowie die von diesem verwendeten Ressourcen freigegeben.|  
|[getAsciiStream](../content/getAsciiStream-Method--SQLServerClob-.md)|Materialisiert das CLOB als ASCII\-Datenstrom.|  
|[getCharacterStream](../content/getCharacterStream-Method--SQLServerClob-.md)|Gibt die CLOB\-Daten als java.io.Reader\-Objekt oder als Zeichendatenstrom zurück.|  
|[getSubString](../content/getSubString-Method--SQLServerClob-.md)|Gibt eine Kopie der angegebenen Teilzeichenfolge im CLOB auf der Grundlage der angegebenen Startposition und der Anzahl der zu kopierenden Zeichen zurück.|  
|[length](../content/length-Method--SQLServerClob-.md)|Gibt die Anzahl von Zeichen im CLOB zurück.|  
|[position](../content/position-Method--SQLServerClob-.md)|Gibt die Zeichenposition des angegebenen CLOBs oder der Zeichenfolge im CLOB auf der Grundlage der angegebenen Startposition zurück.|  
|[setAsciiStream](../content/setAsciiStream-Method--SQLServerClob-.md)|Gibt einen Datenstrom zurück, der verwendet wird, um ab der angegebenen Position ASCII\-Zeichen in das CLOB zu schreiben.|  
|[setCharacterStream](../content/setCharacterStream-Method--SQLServerClob-.md)|Gibt einen Datenstrom zurück, der verwendet wird, um ab der angegebenen Position einen Unicode\-Zeichendatenstrom in das CLOB zu schreiben.|  
|[setString](../content/setString-Method--SQLServerClob-.md)|Schreibt die angegebene Zeichenfolge ab der angegebenen Position in das CLOB.|  
|[truncate](../content/truncate-Method--SQLServerClob-.md)|Kürzt das CLOB auf die angegebene Länge.|  
  
### Geerbte Methoden  
  
|Klasse geerbt von:|Methoden|  
|------------------------|--------------|  
|java.lang.Object|clone, equals, finalize, getClass, hashCode, notify, notifyAll, toString, wait|  
  
## Siehe auch  
 [SQLServerClob-Klasse](../content/SQLServerClob-Class.md)  
  
  