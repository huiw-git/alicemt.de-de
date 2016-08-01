---
title: "Grundlegendes zu den Unterschieden von Datentypen"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ab8fa00f-cb16-47e2-94b8-3a76f56c2b84
caps.latest.revision: 33
caps.handback.revision: 32
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
# Grundlegendes zu den Unterschieden von Datentypen
  Es gibt eine Reihe von Unterschieden zwischen den Java\-Datentypen und den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentypen.[!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] berücksichtigt diese Unterschiede durch verschiedenartige Konvertierungen.  
  
## Zeichentypen  
 Die JDBC\-Datentypen für Zeichenfolgen lauten **CHAR**, **VARCHAR** und **LONGVARCHAR**. Der JDBC\-Treiber unterstützt die JDBC 4.0\-API. In JDBC 4.0 sind auch **NCHAR**, **NVARCHAR** und **LONGNVARCHAR** als JDBC\-Zeichenfolgentypen möglich. Diese neuen Zeichenfolgentypen verwalten die systemeigenen Java\-Zeichentypen im Unicode\-Format, sodass keine Konvertierung von ANSI nach Unicode und Unicode nach ANSI mehr erforderlich ist.  
  
|Typ|Beschreibung|  
|---------|------------------|  
|Feste Länge|Die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentypen **char** und **nchar** sind direkt den JDBC\-Typen **CHAR** und **NCHAR** zugeordnet. Diese Typen weisen eine feste Länge auf und werden vom Server mit Leerstellen aufgefüllt, wenn für die Spalte SET ANSI\_PADDING ON festgelegt wurde. Die Auffüllung mit Leerstellen ist für **nchar** immer aktiviert. Bei **char** fügt der JDBC\-Treiber die Leerstellen jedoch nur hinzu, wenn die char\-Spalten des Servers nicht aufgefüllt wurden.|  
|Variable Länge|Die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Typen **varchar** und **nvarchar** sind direkt den JDBC\-Typen **VARCHAR** bzw. **NVARCHAR** zugeordnet.|  
|Long|Die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Typen **text** und **ntext** sind direkt den JDBC\-Typen **LONGVARCHAR** bzw. **LONGNVARCHAR** zugeordnet. Diese Typen sind ab [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] veraltet, sodass Sie stattdessen die Typen mit umfangreichen Werten, **varchar\(max\)** oder **nvarchar\(max\)**, verwenden sollten.<br /><br /> Mit der update\<Numeric Type\>\-Methode und der [updateObject \(int, java.lang.Object\)](../content/updateObject-Method--int--java.lang.Object-.md)\-Methode treten bei **text**\- und **ntext**\-Serverspalten Fehler auf. Allerdings wird die Verwendung der [setObject](../content/setObject-Method--SQLServerPreparedStatement-.md)\-Methode mit Angabe eines Zeichenkonvertierungstyps für **text**\- und **ntext**\-Serverspalten unterstützt.|  
  
## Binäre Zeichenfolgetypen  
 Die binären JDBC\-Zeichenfolgentypen lauten **BINARY**, **VARBINARY** und **LONGVARBINARY**.  
  
|Typ|Beschreibung|  
|---------|------------------|  
|Feste Länge|Der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Typ **binary** ist direkt dem JDBC\-Typ **BINARY** zugeordnet. Dieser Typ weist eine feste Länge auf und wird vom Server mit Leerstellen aufgefüllt, wenn für die Spalte SET ANSI\_PADDING ON eingestellt wurde. Wenn die Zeichenspalten des Servers nicht mit Leerstellen aufgefüllt sind, fügt der JDBC\-Treiber die Leerstellen hinzu.<br /><br /> Bei dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Typ **timestamp** handelt es sich um einen JDBC\-**BINARY**\-Typ mit einer festen Länge von 8 Bytes.|  
|Variable Länge|Der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Typ **varbinary** ist dem JDBC\-Typ **VARBINARY** zugeordnet.<br /><br /> Der **udt**\-Typ in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] entspricht dem **VARBINARY**\-Typ in JDBC.|  
|Long|Der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Typ **image** ist dem JDBC\-Typ **LONGVARBINARY** zugeordnet. Dieser Typ ist ab [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] veraltet, sodass Sie stattdessen einen Typ mit umfangreichen Werten, d. h. **varbinary\(max\)**, verwenden sollten.|  
  
## Exakte numerische Typen  
 Die exakten numerischen JDBC\-Typen sind direkt den entsprechenden SQL Server\-Typen zugeordnet.  
  
|Typ|Beschreibung|  
|---------|------------------|  
|BIT|Der JDBC\-Typ **BIT** stellt ein Bit dar, das 0 oder 1 sein kann. Entspricht dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Typ **bit**.|  
|TINYINT|Der JDBC\-Typ **TINYINT** stellt ein einzelnes Byte dar. Entspricht dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Typ **tinyint**.|  
|SMALLINT|Der JDBC\-Typ **SMALLINT** stellt eine 16\-Bit\-Ganzzahl mit Vorzeichen dar. Entspricht dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Typ **smallint**.|  
|INTEGER|Der JDBC\-Typ **INTEGER** stellt eine 32\-Bit\-Ganzzahl mit Vorzeichen dar. Entspricht dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Typ **int**.|  
|BIGINT|Der JDBC\-Typ **BIGINT** stellt eine 64\-Bit\-Ganzzahl mit Vorzeichen dar. Entspricht dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Typ **bigint**.|  
|NUMERIC|Der JDBC\-Typ **NUMERIC** stellt einen Dezimalwert fester Genauigkeit dar, der Werte mit identischer Genauigkeit enthält. Der **NUMERIC**\-Typ ist dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Typ **numeric** zugeordnet.|  
|DECIMAL|Der JDBC\-Typ **DECIMAL** stellt einen Dezimalwert fester Genauigkeit dar, der Werte mit mindestens der angegebenen Genauigkeit enthält. Der **DECIMAL**\-Typ ist dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Typ **decimal** zugeordnet.<br /><br /> Der JDBC\-Typ **DECIMAL** ist außerdem den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Typen **money** und **smallmoney** zugeordnet. Dabei handelt es sich um spezielle Dezimaltypen fester Genauigkeit, die in 8 bzw. 4 Bytes gespeichert werden.|  
  
## Angenäherte numerische Typen  
 Die angenäherten numerischen JDBC\-Typen lauten **REAL**, **DOUBLE** und **FLOAT**.  
  
|Typ|Beschreibung|  
|---------|------------------|  
|REAL|Der JDBC\-Typ **REAL** weist sieben Ziffern für die Genauigkeit auf \(einfache Genauigkeit\) und ist dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Typ **real** zugeordnet.|  
|DOUBLE|Der JDBC\-Typ **DOUBLE** weist 15 Ziffern für die Genauigkeit auf \(doppelte Genauigkeit\) und ist dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Typ **float** zugeordnet. Bei dem JDBC\-Typ **FLOAT** handelt es sich um ein Synonym für **DOUBLE**. Um Verwechslungen zwischen **FLOAT** und **DOUBLE** zu vermeiden, sollte vorzugsweise **DOUBLE** verwendet werden.|  
  
## Datum\-\/Zeittypen  
 Der JDBC\-Typ **TIMESTAMP** ist den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Typen **datetime** und **smalldatetime** zugeordnet. Der **datetime**\-Typ wird in zwei integer\-Werten mit einer Länge von 4 Byte gespeichert. Der **smalldatetime**\-Typ enthält die gleichen Informationen \(Datum und Uhrzeit\), allerdings mit geringerer Genauigkeit in zwei integer\-Werten mit einer Länge von 2 Byte.  
  
> [!NOTE]  
>  Bei dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Typ **timestamp** handelt es sich um einen binären Zeichenfolgetyp mit fester Länge. Er ist keinem der JDBC\-Typen **DATE**, **TIME** oder **TIMESTAMP** zugeordnet.  
  
## Benutzerdefinierte Typzuordnung  
 Die Zuordnungsfunktion für benutzerdefinierte Typen von JDBC, die die SQLData\-Schnittstellen für die erweiterten JDBC\-Typen \(UDTs, Struct usw.\) verwendet, ist im JDBC\-Treiber nicht implementiert.  
  
## Siehe auch  
 [Grundlegendes zu den Datentypen in JDBC Driver](../content/Understanding-the-JDBC-Driver-Data-Types.md)  
  
  