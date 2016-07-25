---
title: "SQLXML-Schnittstelle"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7c67be98-efb5-446c-a0e3-ee67c43cb170
caps.latest.revision: 19
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
# SQLXML-Schnittstelle
  JDBC Driver bietet Unterstützung für die JDBC 4.0\-API, in der die java.sql.SQLXML\-Schnittstelle eingeführt wird. Die SQLXML\-Schnittstelle definiert Methoden für die Interaktion mit und die Bearbeitung von XML\-Daten. Der **SQLXML**\-Typ ist dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datentyp **xml** zugeordnet.  
  
 Die SQLXML\-Schnittstelle bietet Methoden für den Zugriff auf den XML\-Wert als **String**, **Reader**, **Writer** oder **Stream**. Der Zugriff auf den XML\-Wert ist auch über **Source** möglich, und er kann als **Result** festgelegt werden. Diese werden mit XML\-Parser\-APIs wie DOM \(Document Object Model\), SAX \(Simple API for XML\) und StAX \(Streaming API for XML\) sowie mit XSLT\-Transformationen und XPath verwendet.  
  
## Hinweise  
 In der folgenden Tabelle werden die in der SQLXML\-Schnittstelle definierten Methoden beschrieben:  
  
|Methodensyntax|Methodenbeschreibung|  
|--------------------|--------------------------|  
|[void free\(\)](http://go.microsoft.com/fwlink/?LinkId=131685)|Mit dieser Methode werden das SQLXML\-Objekt und die von diesem verwendeten Ressourcen freigegeben.|  
|[InputStream getBinaryStream\(\)](http://go.microsoft.com/fwlink/?LinkId=131754)|Gibt einen Eingabedatenstrom zum Lesen von Daten aus dem SQLXML zurück.|  
|[Reader getCharacterStream\(\)](http://go.microsoft.com/fwlink/?LinkId=131755)|Gibt die **XML**\-Daten als java.io.Reader\-Objekt oder als Zeichendatenstrom zurück.|  
|[T extends Source T getSource\(Class\<T\> sourceClass\)](http://go.microsoft.com/fwlink/?LinkId=131756)|Gibt eine **Source** zum Lesen des **XML**\-Werts zurück, der von diesem **SQLXML**\-Objekt angegeben wird. **Note:**  Die getSource\-Methode unterstützt die folgenden Quellen: javax.xml.transform.dom.DOMSource, javax.xml.transform.sax.SAXSource, javax.xml.transform.stax.StAXSource und java.io.InputStream.|  
|[String getString\(\)](http://go.microsoft.com/fwlink/?LinkId=131757)|Gibt eine Zeichenfolgendarstellung des **XML**\-Werts zurück, der von diesem SQLXML\-Objekt angegeben wird.|  
|[OutputStream setBinaryStream\(\)](http://go.microsoft.com/fwlink/?LinkId=131758)|Ruft einen Datenstrom ab, der zum Schreiben des **XML**\-Werts verwendet werden kann, der von diesem SQLXML\-Objekt angegeben wird.|  
|[Writer setCharacterStream\(\)](http://go.microsoft.com/fwlink/?LinkId=131759)|Gibt einen Datenstrom zurück, der zum Schreiben des **XML**\-Werts verwendet werden kann, der von diesem SQLXML\-Objekt angegeben wird.|  
|[T extends Result T setResult\(Class\<T\> resultClass\)](http://go.microsoft.com/fwlink/?LinkId=131760)|Gibt ein **Result** zum Festlegen des **XML**\-Werts zurück, der von diesem **SQLXML**\-Objekt angegeben wird. **Note:**  Die setResult\-Methode unterstützt die folgenden Quellen: javax.xml.transform.dom.DOMResult, javax.xml.transform.sax.SAXResult, javax.xml.transform.stax.StaxResult und java.io.OutputStream.|  
|[void setString\(String value\)](http://go.microsoft.com/fwlink/?LinkId=131762)|Legt den von diesem SQLXML\-Objekt angegebenen XML\-Wert auf die angegebene **String**\-Darstellung fest.|  
  
 Die Anwendungen können XML\-Werte nur einmal aus einem SQLXML\-Objekt lesen bzw. in dieses schreiben.  
  
 Nach dem Aufrufen der free\(\)\-Methode wird ein SQLXML\-Objekt ungültig und kann weder gelesen noch geschrieben werden. Wenn die Anwendung versucht, für das SQLXML\-Objekt eine andere Methode als free\(\)aufzurufen, wird eine Ausnahme ausgelöst.  
  
 Nach dem Aufrufen einer der folgenden Abrufmethoden kann das SQLXML\-Objekt nicht mehr gelesen oder geschrieben werden: getSource, getCharacterStream, getBinaryStream und getString.  
  
 Nach dem Aufrufen einer der folgenden Festlegungsmethoden kann das SQLXML\-Objekt nicht mehr gelesen oder geschrieben werden: setResult, setCharacterStream, setBinaryStream und setString.  
  
## Siehe auch  
 [Unterstützen von XML-Daten](../content/Supporting-XML-Data.md)  
  
  