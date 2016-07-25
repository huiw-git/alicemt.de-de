---
title: "Saving to the XML DOM Object"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4d20fd28-aaf8-4232-83ce-f9d1e5f93dae
caps.latest.revision: 2
caps.handback.revision: 2
manager: sonalm
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pt-br
  - ru-ru
  - zh-cn
  - zh-tw
---
# Saving to the XML DOM Object
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="65d75d05a1dbb1debefab4a1b48d3531" id="tgt1" class="tgtSentence">You can save a Recordset in XML format to an instance of an MSXML DOM object, as shown in the following Visual Basic code:</caps:sentence>
        </para>
        <code>Dim xDOM As New MSXML.DOMDocument
Dim rsXML As New ADODB.Recordset
Dim sSQL As String, sConn As String
    
sSQL = "SELECT customerid, companyname, contactname FROM customers"
sConn="Provider=Microsoft.Jet.OLEDB.4.0;Data Source=D:\Program Files" &amp; _
        "\Common Files\System\msadc\samples\NWind.mdb"
rsXML.Open sSQL, sConn
rsXML.Save xDOM, adPersistADO   'Save Recordset directly into a DOM tree.
...</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="f3113ec4-ae31-428f-89c6-bc1024f128ea">Persisting Records in XML Format</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">You can save a Recordset in XML format to an instance of an MSXML DOM object, as shown in the following Visual Basic code:</caps:sentence>
        </para>
        <code>Dim xDOM As New MSXML.DOMDocument
Dim rsXML As New ADODB.Recordset
Dim sSQL As String, sConn As String
    
sSQL = "SELECT customerid, companyname, contactname FROM customers"
sConn="Provider=Microsoft.Jet.OLEDB.4.0;Data Source=D:\Program Files" &amp; _
        "\Common Files\System\msadc\samples\NWind.mdb"
rsXML.Open sSQL, sConn
rsXML.Save xDOM, adPersistADO   'Save Recordset directly into a DOM tree.
...</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="f3113ec4-ae31-428f-89c6-bc1024f128ea">Persisting Records in XML Format</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>