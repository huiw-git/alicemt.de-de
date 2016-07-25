---
title: "Streams and Persistence"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ad5bf52c-fd10-4cfa-bf7d-fcedcaa41eea
caps.latest.revision: 8
caps.handback.revision: 8
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
# Streams and Persistence
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="d6af77a153bfdc1872237fed0809a0d3" id="tgt1" class="tgtSentence">The <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object <legacyLink xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save</legacyLink> method stores, or <legacyItalic>persists</legacyItalic>, a <legacyBold>Recordset</legacyBold> in a file, and the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method restores the <legacyBold>Recordset</legacyBold> from that file.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="0007d1c7eb94229c09b6d34f35716ed0" id="tgt2" class="tgtSentence">With ADO 2.7 or later, the <legacyBold>Save</legacyBold> and <legacyBold>Open</legacyBold> methods can persist a <legacyBold>Recordset</legacyBold> to a <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object as well.</caps:sentence>
          <caps:sentence sentenceid="6b5e3029af9ae732c0c626ab2ee22e58" id="tgt3" class="tgtSentence"> This feature is especially useful when working with Remote Data Service (RDS) and Active Server Pages (ASP).</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="441ed0e43634dd89082383472a3710f7" id="tgt4" class="tgtSentence">For more information about how persistence can be used by itself on ASP pages, see the current ASP documentation.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="fb9b1b621ff87999081f8d19be21507c" id="tgt5" class="tgtSentence">The following are a few scenarios that show how <legacyBold>Stream</legacyBold> objects and persistence can be used.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="5b8f19b87240ec67e950ca7b6990ba67" id="tgt6" class="tgtSentence">Scenario 1</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="acececd24a391e74c835ddde18f52141" id="tgt7" class="tgtSentence">This scenario simply saves a <legacyBold>Recordset</legacyBold> to a file and then to a <legacyBold>Stream</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="19f35c59887e53a9f73cdd8c8ce6115a" id="tgt8" class="tgtSentence"> It then opens the persisted stream into another <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <code>Dim rs1 As ADODB.Recordset
Dim rs2 As ADODB.Recordset
Dim stm As ADODB.Stream

Set rs1 = New ADODB.Recordset
Set rs2 = New ADODB.Recordset
Set stm = New ADODB.Stream

rs1.<codeFeaturedElement xmlns="">Open</codeFeaturedElement>   "SELECT * FROM Customers", "Provider=sqloledb;" &amp; _
        "Data Source=MyServer;Initial Catalog=Northwind;" &amp; _
        "Integrated Security=SSPI;""", adopenStatic, adLockReadOnly, adCmdText
rs1.<codeFeaturedElement xmlns="">Save</codeFeaturedElement> "c:\myfolder\mysubfolder\myrs.xml", <codeFeaturedElement xmlns="">adPersistXML</codeFeaturedElement>
rs1.<codeFeaturedElement xmlns="">Save</codeFeaturedElement> stm, <codeFeaturedElement xmlns="">adPersistXML</codeFeaturedElement>
rs2.<codeFeaturedElement xmlns="">Open</codeFeaturedElement> stm</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="5d8d5ab1fe17049238826a6224568136" id="tgt9" class="tgtSentence">Scenario 2</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e1d05dc131e46f6e05d40ce80d160b36" id="tgt10" class="tgtSentence">This scenario persists a <legacyBold>Recordset</legacyBold> into a <legacyBold>Stream</legacyBold> in XML format.</caps:sentence>
            <caps:sentence sentenceid="473212e3d9dce03c4611d627e77cdf7f" id="tgt11" class="tgtSentence"> It then reads the <legacyBold>Stream</legacyBold> into a string that you can examine, manipulate, or display.</caps:sentence>
          </para>
          <code>Dim rs As ADODB.Recordset
Dim stm As ADODB.Stream
Dim strRst As String

Set rs = New ADODB.Recordset
Set stm = New ADODB.Stream

' Open, save, and close the recordset. 
rs.<codeFeaturedElement xmlns="">Open</codeFeaturedElement> "SELECT * FROM Customers", "Provider=sqloledb;" &amp; _
        "Data Source=MyServer;Initial Catalog=Northwind;" &amp; _
        "Integrated Security=SSPI;"""
rs.<codeFeaturedElement xmlns="">Save</codeFeaturedElement> stm, <codeFeaturedElement xmlns="">adPersistXML</codeFeaturedElement>
rs.Close
Set rs = nothing

' Put saved Recordset into a string variable.
strRst = stm.<codeFeaturedElement xmlns="">ReadText</codeFeaturedElement>(adReadAll)

' Examine, manipulate, or display the XML data.
...</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="a9a8f34ece21da3c9caf4d1adb5dbd76" id="tgt12" class="tgtSentence">Scenario 3</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="7c782dfea0c377a295816488133b1c6a" id="tgt13" class="tgtSentence">This example code shows ASP code persisting a <legacyBold>Recordset</legacyBold> as XML directly to the <legacyBold>Response</legacyBold> object:</caps:sentence>
          </para>
          <code>...
&lt;%
response.ContentType = "text/xml"

' Create and open a Recordset.
Set rs = Server.CreateObject("ADODB.Recordset")
rs.Open "select * from Customers", "Provider=sqloledb;" &amp; _
        "Data Source=MyServer;Initial Catalog=Northwind;" &amp; _
        "Integrated Security=SSPI;"""

' Save Recordset directly into output stream.
rs.<codeFeaturedElement xmlns="">Save</codeFeaturedElement> Response, <codeFeaturedElement xmlns="">adPersistXML</codeFeaturedElement> 

' Close Recordset.
rs.Close
Set rs = nothing
%&gt;
...</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="f35ca05ccd815e0709807cfee3e04cb0" id="tgt14" class="tgtSentence">Scenario 4</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b5f4a450af260ff40167b2338334953d" id="tgt15" class="tgtSentence">In this scenario, ASP code writes the contents of the <legacyBold>Recordset</legacyBold> in ADTG format to the client.</caps:sentence>
            <caps:sentence sentenceid="a10adbe9652825a82b9ee15e0daa3db1" id="tgt16" class="tgtSentence"> The <legacyLink xlink:href="420d0989-7cfb-4c66-a7b5-f4199d13165d">Microsoft Cursor Service for OLE DB</legacyLink> can use this data to create a disconnected <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1f907d1e7461c75afe6c16ecaa0cde0c" id="tgt17" class="tgtSentence">A new property on the RDS <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl</legacyLink>, <legacyLink xlink:href="8c56b233-1be8-442c-8d0e-a4c96465bc99">URL</legacyLink>, points to the .asp page that generates the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="66f03b1e1c622b436f68c2ae31883b4a" id="tgt18" class="tgtSentence"> This means a <legacyBold>Recordset</legacyBold> object can be obtained without RDS using the server-side <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">DataFactory</legacyLink> object or the user writing a business object.</caps:sentence>
            <caps:sentence sentenceid="f22c4ed442cb860369b0d7c515620b04" id="tgt19" class="tgtSentence"> This simplifies the RDS programming model significantly.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="8ff3da6f273e88a559e75c6f38089b7d" id="tgt20" class="tgtSentence">Server-side code, named http://server/directory/recordset.asp:</caps:sentence>
          </para>
          <code>&lt;%
Dim rs 
Set rs = Server.CreateObject("ADODB.Recordset")
rs.Open "select au_fname, au_lname, phone from Authors", ""&amp; _
        "Provider=sqloledb;Data Source=MyServer;" &amp; _
        "Initial Catalog=Pubs;Integrated Security=SSPI;"
response.ContentType = "multipart/mixed"
rs.<codeFeaturedElement xmlns="">Save</codeFeaturedElement> response, <codeFeaturedElement xmlns="">adPersistADTG</codeFeaturedElement>
%&gt;</code>
          <para>
            <caps:sentence sentenceid="dad648b7e81d9ebf3e002b7d2a07ab65" id="tgt21" class="tgtSentence">Client-side code:</caps:sentence>
          </para>
          <code>&lt;HTML&gt;
&lt;HEAD&gt;
&lt;TITLE&gt;RDS Query Page&lt;/TITLE&gt;
&lt;/HEAD&gt;
&lt;body&gt;
&lt;CENTER&gt;
&lt;H1&gt;Remote Data Service 2.5&lt;/H1&gt;
&lt;TABLE DATASRC="#DC1"&gt;
   &lt;TR&gt; 
      &lt;TD&gt;&lt;SPAN DATAFLD="au_fname"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
      &lt;TD&gt;&lt;SPAN DATAFLD="au_lname"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
      &lt;TD&gt;&lt;SPAN DATAFLD="phone"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
   &lt;/TR&gt;
&lt;/TABLE&gt;
&lt;BR&gt;

&lt;OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33"
    ID=DC1 HEIGHT=1 WIDTH = 1&gt;
    &lt;PARAM NAME="<codeFeaturedElement xmlns="">URL</codeFeaturedElement>" VALUE="http://server/directory/recordset.asp"&gt;
&lt;/OBJECT&gt;

&lt;/SCRIPT&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;</code>
          <para>
            <caps:sentence sentenceid="c74764efe90b86332ed21a6524eb77c8" id="tgt22" class="tgtSentence">Developers also have the option of using a <legacyBold>Recordset</legacyBold> object on the client:</caps:sentence>
          </para>
          <code>...
function GetRs() 
    {
    rs = CreateObject("ADODB.Recordset");
    rs.<codeFeaturedElement xmlns="">Open</codeFeaturedElement> "http://server/directory/recordset.asp"
    DC1.SourceRecordset = rs;
    }
...</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
        <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record Object</link>
        <link xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object <legacyLink xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save</legacyLink> method stores, or <legacyItalic>persists</legacyItalic>, a <legacyBold>Recordset</legacyBold> in a file, and the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method restores the <legacyBold>Recordset</legacyBold> from that file.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">With ADO 2.7 or later, the <legacyBold>Save</legacyBold> and <legacyBold>Open</legacyBold> methods can persist a <legacyBold>Recordset</legacyBold> to a <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object as well.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> This feature is especially useful when working with Remote Data Service (RDS) and Active Server Pages (ASP).</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">For more information about how persistence can be used by itself on ASP pages, see the current ASP documentation.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">The following are a few scenarios that show how <legacyBold>Stream</legacyBold> objects and persistence can be used.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">Scenario 1</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">This scenario simply saves a <legacyBold>Recordset</legacyBold> to a file and then to a <legacyBold>Stream</legacyBold>.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> It then opens the persisted stream into another <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <code>Dim rs1 As ADODB.Recordset
Dim rs2 As ADODB.Recordset
Dim stm As ADODB.Stream

Set rs1 = New ADODB.Recordset
Set rs2 = New ADODB.Recordset
Set stm = New ADODB.Stream

rs1.<codeFeaturedElement xmlns="">Open</codeFeaturedElement>   "SELECT * FROM Customers", "Provider=sqloledb;" &amp; _
        "Data Source=MyServer;Initial Catalog=Northwind;" &amp; _
        "Integrated Security=SSPI;""", adopenStatic, adLockReadOnly, adCmdText
rs1.<codeFeaturedElement xmlns="">Save</codeFeaturedElement> "c:\myfolder\mysubfolder\myrs.xml", <codeFeaturedElement xmlns="">adPersistXML</codeFeaturedElement>
rs1.<codeFeaturedElement xmlns="">Save</codeFeaturedElement> stm, <codeFeaturedElement xmlns="">adPersistXML</codeFeaturedElement>
rs2.<codeFeaturedElement xmlns="">Open</codeFeaturedElement> stm</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src9" class="srcSentence">Scenario 2</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src10" class="srcSentence">This scenario persists a <legacyBold>Recordset</legacyBold> into a <legacyBold>Stream</legacyBold> in XML format.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> It then reads the <legacyBold>Stream</legacyBold> into a string that you can examine, manipulate, or display.</caps:sentence>
          </para>
          <code>Dim rs As ADODB.Recordset
Dim stm As ADODB.Stream
Dim strRst As String

Set rs = New ADODB.Recordset
Set stm = New ADODB.Stream

' Open, save, and close the recordset. 
rs.<codeFeaturedElement xmlns="">Open</codeFeaturedElement> "SELECT * FROM Customers", "Provider=sqloledb;" &amp; _
        "Data Source=MyServer;Initial Catalog=Northwind;" &amp; _
        "Integrated Security=SSPI;"""
rs.<codeFeaturedElement xmlns="">Save</codeFeaturedElement> stm, <codeFeaturedElement xmlns="">adPersistXML</codeFeaturedElement>
rs.Close
Set rs = nothing

' Put saved Recordset into a string variable.
strRst = stm.<codeFeaturedElement xmlns="">ReadText</codeFeaturedElement>(adReadAll)

' Examine, manipulate, or display the XML data.
...</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src12" class="srcSentence">Scenario 3</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src13" class="srcSentence">This example code shows ASP code persisting a <legacyBold>Recordset</legacyBold> as XML directly to the <legacyBold>Response</legacyBold> object:</caps:sentence>
          </para>
          <code>...
&lt;%
response.ContentType = "text/xml"

' Create and open a Recordset.
Set rs = Server.CreateObject("ADODB.Recordset")
rs.Open "select * from Customers", "Provider=sqloledb;" &amp; _
        "Data Source=MyServer;Initial Catalog=Northwind;" &amp; _
        "Integrated Security=SSPI;"""

' Save Recordset directly into output stream.
rs.<codeFeaturedElement xmlns="">Save</codeFeaturedElement> Response, <codeFeaturedElement xmlns="">adPersistXML</codeFeaturedElement> 

' Close Recordset.
rs.Close
Set rs = nothing
%&gt;
...</code>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src14" class="srcSentence">Scenario 4</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src15" class="srcSentence">In this scenario, ASP code writes the contents of the <legacyBold>Recordset</legacyBold> in ADTG format to the client.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> The <legacyLink xlink:href="420d0989-7cfb-4c66-a7b5-f4199d13165d">Microsoft Cursor Service for OLE DB</legacyLink> can use this data to create a disconnected <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src17" class="srcSentence">A new property on the RDS <legacyLink xlink:href="d85ea4fc-451c-436e-97b8-58f92b149dd0">DataControl</legacyLink>, <legacyLink xlink:href="8c56b233-1be8-442c-8d0e-a4c96465bc99">URL</legacyLink>, points to the .asp page that generates the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> This means a <legacyBold>Recordset</legacyBold> object can be obtained without RDS using the server-side <legacyLink xlink:href="e75240c2-b749-471e-b6ea-98cae232efbe">DataFactory</legacyLink> object or the user writing a business object.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> This simplifies the RDS programming model significantly.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src20" class="srcSentence">Server-side code, named http://server/directory/recordset.asp:</caps:sentence>
          </para>
          <code>&lt;%
Dim rs 
Set rs = Server.CreateObject("ADODB.Recordset")
rs.Open "select au_fname, au_lname, phone from Authors", ""&amp; _
        "Provider=sqloledb;Data Source=MyServer;" &amp; _
        "Initial Catalog=Pubs;Integrated Security=SSPI;"
response.ContentType = "multipart/mixed"
rs.<codeFeaturedElement xmlns="">Save</codeFeaturedElement> response, <codeFeaturedElement xmlns="">adPersistADTG</codeFeaturedElement>
%&gt;</code>
          <para>
            <caps:sentence id="src21" class="srcSentence">Client-side code:</caps:sentence>
          </para>
          <code>&lt;HTML&gt;
&lt;HEAD&gt;
&lt;TITLE&gt;RDS Query Page&lt;/TITLE&gt;
&lt;/HEAD&gt;
&lt;body&gt;
&lt;CENTER&gt;
&lt;H1&gt;Remote Data Service 2.5&lt;/H1&gt;
&lt;TABLE DATASRC="#DC1"&gt;
   &lt;TR&gt; 
      &lt;TD&gt;&lt;SPAN DATAFLD="au_fname"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
      &lt;TD&gt;&lt;SPAN DATAFLD="au_lname"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
      &lt;TD&gt;&lt;SPAN DATAFLD="phone"&gt;&lt;/SPAN&gt;&lt;/TD&gt;
   &lt;/TR&gt;
&lt;/TABLE&gt;
&lt;BR&gt;

&lt;OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33"
    ID=DC1 HEIGHT=1 WIDTH = 1&gt;
    &lt;PARAM NAME="<codeFeaturedElement xmlns="">URL</codeFeaturedElement>" VALUE="http://server/directory/recordset.asp"&gt;
&lt;/OBJECT&gt;

&lt;/SCRIPT&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;</code>
          <para>
            <caps:sentence id="src22" class="srcSentence">Developers also have the option of using a <legacyBold>Recordset</legacyBold> object on the client:</caps:sentence>
          </para>
          <code>...
function GetRs() 
    {
    rs = CreateObject("ADODB.Recordset");
    rs.<codeFeaturedElement xmlns="">Open</codeFeaturedElement> "http://server/directory/recordset.asp"
    DC1.SourceRecordset = rs;
    }
...</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open Method (ADO Recordset)</link>
        <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record Object</link>
        <link xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>