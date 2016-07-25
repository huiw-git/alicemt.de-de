---
title: "SQLServerParameterMetaData-Elemente"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f9ebb203-2013-4feb-94f5-494b7f098f9a
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
  - sv-se
  - zh-cn
  - zh-tw
---
# SQLServerParameterMetaData-Elemente
    
## SQLServerParameterMetaData\-Elemente  
 Die folgenden Tabellen enthalten die Elemente, die von der [SQLServerParameterMetaData](../content/SQLServerParameterMetaData-Class.md)\-Klasse verfügbar gemacht werden.  
  
### Konstruktoren  
 Keine  
  
### Felder  
 Keine  
  
### Geerbte Felder  
  
|Name|Beschreibung|  
|----------|------------------|  
|java.sql.ParameterMetaData|parameterModeIn, parameterModeInOut, parameterModeOut, parameterModeUnknown, parameterNoNulls, parameterNullable, parameterNullableUnknown|  
  
### Methoden  
  
|Name|Beschreibung|  
|----------|------------------|  
|[getParameterClassName](../content/getParameterClassName-Method--SQLServerParameterMetaData-.md)|Ruft den vollqualifizierten Namen der Java\-Klasse ab, deren Instanzen an die [setObject](../content/setObject-Method--SQLServerPreparedStatement-.md)\-Methode der [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\-Klasse übergeben werden sollen.|  
|[getParameterCount](../content/getParameterCount-Method--SQLServerParameterMetaData-.md)|Ruft die Anzahl von Parametern im [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\-Objekt ab, für die dieses [SQLServerParameterMetaData](../content/SQLServerParameterMetaData-Class.md)\-Objekt Informationen enthält.|  
|[getParameterMode](../content/getParameterMode-Method--SQLServerParameterMetaData-.md)|Ruft den Modus des angegebenen Parameters ab.|  
|[getParameterType](../content/getParameterType-Method--SQLServerParameterMetaData-.md)|Ruft den SQL\-Typ des angegebenen Parameters ab.|  
|[getParameterTypeName](../content/getParameterTypeName-Method--SQLServerParameterMetaData-.md)|Ruft den datenbankspezifischen Typnamen des angegebenen Parameters ab.|  
|[getPrecision](../content/getPrecision-Method--SQLServerParameterMetaData-.md)|Ruft die Anzahl von Dezimalstellen für den angegebenen Parameter ab.|  
|[getScale](../content/getScale-Method--SQLServerParameterMetaData-.md)|Ruft für den angegebenen Parameter die Anzahl von Stellen hinter dem Dezimalzeichen ab.|  
|[isNullable](../content/isNullable-Method--SQLServerParameterMetaData-.md)|Ruft ab, ob im angegebenen Parameter NULL\-Werte zulässig sind.|  
|[isSigned](../content/isSigned-Method--SQLServerParameterMetaData-.md)|Ruft ab, ob es sich bei den Werten für den angegebenen Parameter um Zahlen mit Vorzeichen handeln kann.|  
  
### Geerbte Methoden  
  
|Klasse geerbt von:|Methoden|  
|------------------------|--------------|  
|java.lang.Object|clone, equals, finalize, getClass, hashCode, notify, notifyAll, toString, wait|  
|java.sql.Wrapper|isWrapperFor, unwrap|  
  
## Siehe auch  
 [SQLServerParameterMetaData-Klasse](../content/SQLServerParameterMetaData-Class.md)  
  
  