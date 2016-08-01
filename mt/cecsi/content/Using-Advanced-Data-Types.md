---
title: "Verwenden von erweiterten Datentypen"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b39461d3-48d6-4048-8300-1a886c00756d
caps.latest.revision: 58
caps.handback.revision: 57
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
# Verwenden von erweiterten Datentypen
  [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] verwendet die erweiterten JDBC\-Datentypen für die Konvertierung der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentypen in ein Format, das von der Programmiersprache Java verarbeitet werden kann.  
  
## Hinweise  
 Die folgende Tabelle enthält eine Liste der Standardzuordnungen zwischen den erweiterten [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentypen sowie den JDBC\- und Java\-Datentypen.  
  
|SQL Server\-Typen|JDBC\-Typen \(java.sql.Types\)|Java\-Typen|  
|-----------------------|------------------------------------|-----------------|  
|varbinary\(max\)<br /><br /> image|LONGVARBINARY|byte\[\] \(Standard\), Blob, InputStream, String|  
|text<br /><br /> varchar\(max\)|LONGVARCHAR|String \(Standard\), Clob, InputStream|  
|ntext<br /><br /> nvarchar\(max\)|LONGVARCHAR<br /><br /> LONGNVARCHAR \(Java SE 6.0\)|String \(Standard\), Clob, NClob \(Java SE 6.0\)|  
|xml|LONGVARCHAR<br /><br /> SQLXML \(Java SE 6.0\)|String \(Standard\), InputStream, Clob, byte\[\], Blob, SQLXML \(Java SE 6.0\)|  
|Udt<sup>1</sup>|VARBINARY|String \(Standard\), byte\[\], InputStream|  
  
 <sup>1</sup> [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] unterstützt zwar das Senden und Abrufen von CLR\-UDTs als binäre Daten, CLR\-Metadaten können jedoch nicht bearbeitet werden.  
  
 Die folgenden Abschnitte enthalten Beispiele für die Verwendung des JDBC\-Treibers und der erweiterten Datentypen.  
  
## BLOB\-, CLOB\- und NCLOB\-Datentypen  
 Der JDBC\-Treiber implementiert alle Methoden der java.sql.Blob\-, java.sql.Clob\- und java.sql.NClob\-Schnittstellen.  
  
> [!NOTE]  
>  CLOB\-Werte können mit [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] \(oder höher\)\-Datentypen mit umfangreichen Werten verwendet werden. Insbesondere können CLOB\-Typen mit den Datentypen **varchar\(max\)** und **nvarchar\(max\)**, BLOB\-Typen mit den Datentypen **varbinary\(max\)** und **image** sowie NCLOB\-Typen mit **ntext** und **nvarchar\(max\)** verwendet werden.  
  
## Datentypen mit umfangreichen Werten  
 In früheren Versionen von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] war bei der Verarbeitung von Datentypen mit umfangreichen Werten eine besondere Behandlung erforderlich. Datentypen mit umfangreichen Werten sind solche, die die maximale Zeilengröße von 8 KB überschreiten.[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] führt einen Maximalbezeichner für die Datentypen **varchar**, **nvarchar** und **varbinary** ein, um die Speicherung von Werten bis zur Größe von 2^31 Byte zu ermöglichen. Tabellenspalten und [!INCLUDE[tsql](../content/includes/tsql_md.md)]\-Variablen können **varchar\(max\)**\-, **nvarchar\(max\)**\- oder **varbinary\(max\)**\-Datentypen angeben.  
  
 Die Verarbeitung von Typen mit umfangreichen Werten umfasst hauptsächlich das Abrufen aus einer Datenbank sowie das Hinzufügen zu einer Datenbank. Die folgenden Abschnitte beschreiben die verschiedenen Verfahren für diese Aufgaben.  
  
### Abrufen von Typen mit umfangreichen Werten aus einer Datenbank  
 Beim Abrufen eines nicht binären Datentyps mit umfangreichen Werten aus einer Datenbank, wie z. B. dem **varchar\(max\)**\-Datentyp, besteht eine Vorgehensweise darin, diese Daten als Zeichendatenstrom zu lesen. Im folgenden Beispiel werden Daten mit der [executeQuery](../content/executeQuery-Method--SQLServerStatement-.md)\-Methode der [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Klasse aus der Datenbank abgerufen und als Resultset zurückgegeben. Anschließend werden die Daten mit umfangreichen Werten mit der [getCharacterStream](../content/getCharacterStream-Method--SQLServerResultSet-.md)\-Methode der [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Klasse aus dem Resultset gelesen.  
  
```  
ResultSet rs = stmt.executeQuery("SELECT TOP 1 * FROM Test1");  
rs.next();  
Reader reader = rs.getCharacterStream(2);  
```  
  
> [!NOTE]  
>  Diese Vorgehensweise kann auch für **text**\-, **ntext**\- und **nvarchar\(max\)**\-Datentypen verwendet werden.  
  
 Beim Abrufen eines binären Datentyps mit umfangreichen Werten aus einer Datenbank, wie z. B. dem **varbinary\(max\)**\-Datentyp, gibt es mehrere mögliche Verfahren. Die effizienteste Vorgehensweise besteht darin, die Daten als Binärdatenstrom zu lesen, wie z. B.:  
  
```  
ResultSet rs = stmt.executeQuery("SELECT photo FROM mypics");  
rs.next();  
InputStream is = rs.getBinaryStream(2);  
```  
  
 Sie können die Daten auch mit der [getBytes](../content/getBytes-Method--SQLServerResultSet-.md)\-Methode als Bytearray lesen, wie z. B.:  
  
```  
ResultSet rs = stmt.executeQuery("SELECT photo FROM mypics");  
rs.next();  
byte [] b = rs.getBytes(2);  
```  
  
> [!NOTE]  
>  Die Daten können auch als BLOB gelesen werden. Diese Vorgehensweise ist jedoch weniger effizient als die beiden oben erwähnten Methoden.  
  
### Hinzufügen von Typen mit umfangreichen Werten zu einer Datenbank  
 Das Hochladen von umfangreichen Daten mit dem JDBC\-Treiber funktioniert problemlos, wenn die Daten in den Arbeitsspeicher passen. Wenn der Umfang der Daten größer ist als der Arbeitsspeicher, sollte Streaming verwendet werden. Die effizienteste Möglichkeit für das Hochladen von umfangreichen Daten bilden die stream\-Schnittstellen.  
  
 Es besteht auch die Möglichkeit, eine Zeichenfolge oder Bytes zu verwenden, wie z. B.:  
  
```  
PreparedStatement pstmt = con.prepareStatement("INSERT INTO test1 (c1_id, c2_vcmax) VALUES (?, ?)");  
pstmt.setInt(1, 1);  
pstmt.setString(2, htmlStr);  
pstmt.executeUpdate();  
```  
  
> [!NOTE]  
>  Diese Vorgehensweise kann auch für Werte verwendet werden, die in **text**\-, **ntext**\- und **nvarchar\(max\)**\-Spalten gespeichert sind.  
  
 Wenn auf dem Server eine Bildbibliothek vorhanden ist und alle binären Bilddateien in eine **varbinary\(max\)**\-Spalte geladen werden müssen, besteht die effizienteste Methode des JDBC\-Treibers darin, direkt Datenströme zu verwenden, wie z. B.:  
  
```  
PreparedStatement pstmt = con.prepareStatement("INSERT INTO test1 (Col1, Col2) VALUES(?,?)");  
File inputFile = new File("CLOBFile20mb.jpg");  
FileInputStream inStream = new FileInputStream(inputFile);  
int id = 1;  
pstmt.setInt(1,id);  
pstmt.setBinaryStream(2, inStream);  
pstmt.executeUpdate();  
inStream.close();  
```  
  
> [!NOTE]  
>  Das Hochladen von umfangreichen Daten mit der CLOB\- oder BLOB\-Methode ist nicht effizient.  
  
### Ändern von Typen mit umfangreichen Werten in einer Datenbank  
 In den meisten Fällen wird empfohlen, zum Aktualisieren oder Ändern von umfangreichen Werten in der Datenbank mit [!INCLUDE[tsql](../content/includes/tsql_md.md)]\-Befehlen wie UPDATE, WRITE und SUBSTRING Parameter über die [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\- und [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Klassen zu übergeben.  
  
 Wenn Sie in einer umfangreichen Textdatei ein Wort ersetzen müssen, z. B. in einer archivierten HTML\-Datei, können Sie ein Clob\-Objekt verwenden, wie z. B.:  
  
```  
String SQL = "SELECT * FROM test1;";  
Statement stmt = con.createStatement(ResultSet.TYPE_SCROLL_SENSITIVE, ResultSet.CONCUR_UPDATABLE);  
ResultSet rs = stmt.executeQuery(SQL);  
rs.next();  
  
Clob clob = rs.getClob(2);  
long pos = clob.position("dog", 1);  
clob.setString(pos, "cat");  
rs.updateClob(2, clob);  
rs.updateRow();  
```  
  
 Darüber hinaus besteht die Möglichkeit, die gesamte Arbeit auf dem Server auszuführen und lediglich Parameter an eine vorbereitete UPDATE\-Anweisung zu übergeben.  
  
 Weitere Informationen zu Typen mit umfangreichen Werten finden Sie in der SQL Server\-Onlinedokumentation unter "Verwenden von Datentypen mit umfangreichen Werten".  
  
## XML\-Datentyp  
 [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] umfasst einen **xml**\-Datentyp, mit dem Sie XML\-Dokumente und \-Fragmente in einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank speichern können. Der **xml**\-Datentyp ist ein integrierter Datentyp in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] und ähnelt in gewisser Weise anderen integrierten Typen wie **int** und **varchar**. Wie andere integrierte Typen können Sie den **xml**\-Datentyp beim Erstellen einer Tabelle als Spaltentyp, als Variablentyp, als Parametertyp oder als Funktionsrückgabetyp bzw. in [!INCLUDE[tsql](../content/includes/tsql_md.md)] CAST\- und CONVERT\-Funktionen verwenden.  
  
 Im JDBC\-Treiber kann der **xml**\-Datentyp als Zeichenfolge\-, Bytearray\-, Datenstrom\-, CLOB\-, BLOB\- oder SQLXML\-Objekt zugeordnet werden. Der Standard lautet Zeichenfolge. Ab JDBC Driver, Version 2.0, unterstützt der JDBC\-Treiber die JDBC 4.0\-API, in der die SQLXML\-Schnittstelle eingeführt wurde. Die SQLXML\-Schnittstelle definiert Methoden für die Interaktion mit und die Bearbeitung von XML\-Daten. Der **SQLXML**\-Typ ist dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentyp **xml** zugeordnet. Weitere Informationen über das Lesen und Schreiben von XML\-Daten in bzw. aus einer relationalen Datenbank mit dem **SQLXML**\-Java\-Datentyp finden Sie unter [Unterstützen von XML-Daten](../content/Supporting-XML-Data.md).  
  
 Die Implementierung des **xml**\-Datentyps im JDBC\-Treiber ermöglicht Folgendes:  
  
-   Zugriff auf XML\-Daten als normale Java UTF\-16\-Zeichenfolge bei den gebräuchlichsten Programmierszenarien  
  
-   Eingabe von UTF\-8\- und anderen 8\-Bit\-codierten XML\-Daten  
  
-   Zugriff auf XML\-Daten als Bytearray mit führender Bytereihenfolgemarke \(Byte Order Mark, BOM\) bei Codierung in UTF\-16 für den Austausch mit anderen XML\-Prozessoren und Datenträgerdateien  
  
 [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] setzt eine führende BOM für UTF\-16\-codierte XML\-Daten voraus. Die Anwendung muss diese bereitstellen, wenn XML\-Parameterwerte als Bytearrays angegeben werden.[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] gibt XML\-Werte immer in Form von UTF\-16\-Zeichenfolgen ohne BOM oder eingebettete Kodierungsdeklaration aus. Wenn XML\-Werte als "byte\[\]", "BinaryStream" oder "Blob" abgerufen werden, steht vor dem Wert ein UTF\-16\-BOM.  
  
 Weitere Informationen zum **xml**\-Datentyp finden Sie in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation unter "XML\-Datentyp".  
  
## Benutzerdefinierte Datentypen  
 Das SQL\-Typensystem wird durch Einführung von benutzerdefinierten Typen \(UDTs, User\-defined Types\) in [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] erweitert, sodass Sie Objekte und benutzerdefinierte Datenstrukturen in einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank speichern können. UDTs können mehrere Datentypen enthalten und Verhalten zeigen, das sie von den herkömmlichen Aliasdatentypen aus einem einzelnen [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Systemdatentyp unterscheidet. UDTs werden mit einer der von der Microsoft .NET Common Language Runtime \(CLR\) unterstützten Sprachen definiert, die überprüfbaren Code erzeugen. Dazu gehören Visual C\# und Visual Basic .NET. Die Daten werden als Felder und Eigenschaften einer .NET Framework\-basierten Klasse oder Struktur offen gelegt. Die Verhalten werden durch Methoden der Klasse bzw. Struktur definiert.  
  
 In [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] kann ein UDT als Spaltendefinition einer Tabelle, als Variable in einem [!INCLUDE[tsql](../content/includes/tsql_md.md)]\-Batch oder als Argument einer [!INCLUDE[tsql](../content/includes/tsql_md.md)]\-Funktion oder gespeicherten Prozedur verwendet werden.  
  
 Weitere Informationen zu benutzerdefinierten Datentypen finden Sie in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation unter "Verwenden und Ändern von Instanzen von benutzerdefinierten Typen".  
  
## Siehe auch  
 [Grundlegendes zu den Datentypen in JDBC Driver](../content/Understanding-the-JDBC-Driver-Data-Types.md)  
  
  