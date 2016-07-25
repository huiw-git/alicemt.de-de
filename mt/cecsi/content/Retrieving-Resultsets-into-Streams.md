---
title: "Retrieving Resultsets into Streams"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 996c1321-c926-4f57-8297-85c8c20de974
caps.latest.revision: 11
caps.handback.revision: 11
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
# Retrieving Resultsets into Streams
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b159ea304f6f648d9b0199ae45c6de7d" id="tgt1" class="tgtSentence">Instead of receiving results in the traditional <legacyBold>Recordset</legacyBold> object, ADO can instead retrieve query results into a stream.</caps:sentence>
          <caps:sentence sentenceid="bb80e1ca773594e3717d1555ab8a41d1" id="tgt2" class="tgtSentence"> The ADO <legacyBold>Stream</legacyBold> object (or other objects that support the COM <legacyBold>IStream</legacyBold> interface, such as the ASP <legacyBold>Request</legacyBold> and <legacyBold>Response</legacyBold> objects) can be used to contain these results.</caps:sentence>
          <caps:sentence sentenceid="7fac6637817127fbbee57e3d2c7db9c4" id="tgt3" class="tgtSentence"> One use for this feature is to retrieve results in XML format.</caps:sentence>
          <caps:sentence sentenceid="4d3b7a25a97de916e2b9cd451d4845aa" id="tgt4" class="tgtSentence"> With SQL Server, for example, XML results can be returned in multiple ways, such as using the FOR XML clause with a SQL SELECT query or using an XPath query.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8669057ec1bf23b86d57e834becd410d" id="tgt5" class="tgtSentence">To receive query results in stream format instead of in a <legacyBold>Recordset</legacyBold>, you must specify the <legacyBold>adExecuteStream</legacyBold> constant from <legacyBold>ExecuteOptionEnum</legacyBold> as a parameter of the <legacyBold>Execute</legacyBold> method of a <legacyBold>Command</legacyBold> object.</caps:sentence>
          <caps:sentence sentenceid="a8692fb279c7b7688d28a5e2c179965e" id="tgt6" class="tgtSentence"> If your provider supports this feature, the results will be returned in a stream upon execution.</caps:sentence>
          <caps:sentence sentenceid="374e9a0ac51d3c2bb31c2a1685b3e639" id="tgt7" class="tgtSentence"> You might be required to specify additional provider-specific properties before the code executes.</caps:sentence>
          <caps:sentence sentenceid="9a93a5636370e4740829656cceb1b485" id="tgt8" class="tgtSentence"> For example, with the Microsoft OLE DB Provider for SQL Server, properties such as <legacyBold>Output Stream</legacyBold> in the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Command</legacyBold> object must be specified.</caps:sentence>
          <caps:sentence sentenceid="57eaf02fbda51fcb6d94fec0020b08e8" id="tgt9" class="tgtSentence"> For more information about SQL Server-specific dynamic properties related to this feature, see XML-Related Properties in the SQL Server Books Online.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="0c0fe942640eb3f6fe8f65e48ac20252" id="tgt10" class="tgtSentence">FOR XML Query Example</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="b5141c8270eeced08172d55c44e0b499" id="tgt11" class="tgtSentence">The following example is written in VBScript to the Northwind database:</caps:sentence>
          </para>
          <code>&lt;!-- BeginRecordAndStreamVBS --&gt;
&lt;%@ LANGUAGE = VBScript %&gt;
&lt;%  Option Explicit      %&gt;

&lt;HTML&gt;
&lt;HEAD&gt;
&lt;META NAME="GENERATOR" Content="Microsoft Developer Studio"/&gt;
&lt;META HTTP-EQUIV="Content-Type" content="text/html"; charset="iso-8859-1"&gt;
&lt;TITLE&gt;FOR XML Query Example&lt;/TITLE&gt;

&lt;STYLE&gt;
   BODY
   {
      FONT-FAMILY: Tahoma;
      FONT-SIZE: 8pt;
      OVERFLOW: auto
   }

   H3
   {
      FONT-FAMILY: Tahoma;
      FONT-SIZE: 8pt;
      OVERFLOW: auto
   }
&lt;/STYLE&gt;

&lt;!-- #include file="adovbs.inc" --&gt;
&lt;%
   Response.Write "&lt;H3&gt;Server-side processing&lt;/H3&gt;"

   Response.Write "Page Generated @ " &amp; Now() &amp; "&lt;BR/&gt;"

   Dim adoConn
   Set adoConn = Server.CreateObject("ADODB.Connection")

   Dim sConn
   sConn = "Provider=SQLOLEDB;Data Source=" &amp; _
      Request.ServerVariables("SERVER_NAME") &amp;amp; ";" &amp; _
      Initial Catalog=Northwind;Integrated Security=SSPI;"

   Response.write "Connect String = " &amp; sConn &amp; "&lt;BR/&gt;"

   adoConn.ConnectionString = sConn
   adoConn.CursorLocation = adUseClient

   adoConn.Open

   Response.write "ADO Version = " &amp; adoConn.Version &amp; "&lt;BR/&gt;"
   Response.write "adoConn.State = " &amp; adoConn.State &amp; "&lt;BR/&gt;"

   Dim adoCmd
   Set adoCmd = Server.CreateObject("ADODB.Command")
   Set adoCmd.ActiveConnection = adoConn

   Dim sQuery
   sQuery = "&lt;ROOT xmlns:sql='urn:schemas-microsoft-com:xml-sql'&gt;&lt;sql:query&gt;SELECT * FROM PRODUCTS WHERE ProductName='Gumbr Gummibrchen' FOR XML AUTO&lt;/sql:query&gt;&lt;/ROOT&gt;"

   Response.write "Query String = " &amp; sQuery &amp; "&lt;BR/&gt;"

   Dim adoStreamQuery
   Set adoStreamQuery = Server.CreateObject("ADODB.Stream")
   adoStreamQuery.Open
   adoStreamQuery.WriteText sQuery, adWriteChar
   adoStreamQuery.Position = 0

   adoCmd.CommandStream = adoStreamQuery
   adoCmd.Dialect = "{5D531CB2-E6Ed-11D2-B252-00C04F681B71}"

   Response.write "Pushing XML to client for processing "  &amp; "&lt;BR/&gt;"

   adoCmd.Properties("Output Stream") = Response
   Response.write "&lt;XML ID='MyDataIsle'&gt;"
   adoCmd.Execute , , 1024
   Response.write "&lt;/XML&gt;"

%&gt;

&lt;SCRIPT language="VBScript" For="window" Event="onload"&gt;
   Dim xmlDoc
   Set xmlDoc = MyDataIsle.XMLDocument
   xmlDoc.resolveExternals=false
   xmlDoc.async=false

   If xmlDoc.parseError.Reason &lt;&gt; "" then
      Msgbox "parseError.Reason = " &amp; xmlDoc.parseError.Reason
   End If
            
   Dim root, child
   Set root = xmlDoc.documentElement
   For each child in root.childNodes
      dim OutputXML
      OutputXML = document.all("log").innerHTML
      document.all("log").innerHTML = OutputXML &amp; "&lt;LI&gt;" &amp; child.getAttribute("ProductName") &amp; "&lt;/LI&gt;"
   Next
&lt;/SCRIPT&gt;

&lt;/HEAD&gt;

&lt;BODY&gt;

   &lt;H3&gt;Client-side processing of XML Document MyDataIsle&lt;/H3&gt;
   &lt;UL id=log&gt;
   &lt;/UL&gt;

&lt;/BODY&gt;
&lt;/HTML&gt;
&lt;!-- EndRecordAndStreamVBS --&gt;
</code>
          <para>
            <caps:sentence sentenceid="abd3efb731a4090da223d6bc1c51f63e" id="tgt12" class="tgtSentence">The FOR XML clause instructs SQL Server to return data in the form of an XML document.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="0bdb9d277e11de1af208e9ed7192233b" id="tgt13" class="tgtSentence">FOR XML Syntax</caps:sentence>
            </title>
            <content>
              <code>FOR XML [RAW|AUTO|EXPLICIT]</code>
              <para>
                <caps:sentence sentenceid="3a80446ccba963b885ac44e362249172" id="tgt14" class="tgtSentence">FOR XML RAW generates generic row elements that have column values as attributes.</caps:sentence>
                <caps:sentence sentenceid="0d45dfe781b0858c6e68262017d129fd" id="tgt15" class="tgtSentence"> FOR XML AUTO uses heuristics to generate a hierarchical tree with element names based on table names.</caps:sentence>
                <caps:sentence sentenceid="7ee5def04926663a242660fd97915cee" id="tgt16" class="tgtSentence"> FOR XML EXPLICIT generates a universal table with relationships fully described by metadata.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="9c270046247f46bb1484d0f63d72734f" id="tgt17" class="tgtSentence">An example SQL SELECT FOR XML statement follows:</caps:sentence>
              </para>
              <code>SELECT * FROM PRODUCTS ORDER BY PRODUCTNAME FOR XML AUTO</code>
              <para>
                <caps:sentence sentenceid="e0bcdd1cd63825c95ae57ec9ee80faf6" id="tgt18" class="tgtSentence">The command can be specified in a string as shown earlier, assigned to <legacyBold>CommandText</legacyBold>, or in the form of an XML template query assigned to <legacyBold>CommandStream</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="1e73fd1065a9274b4595a78bc91f100f" id="tgt19" class="tgtSentence"> For more information about XML template queries, see <legacyLink xlink:href="0ac09dbe-2665-411e-8fbb-d1efe6c777be">Command Streams</legacyLink> in ADO or Using Streams for Command Input in the SQL Server Books Online.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="5f3cd67487738d523c06ad5f85263d6b" id="tgt20" class="tgtSentence">As an XML template query, the FOR XML query appears as follows:</caps:sentence>
              </para>
              <code>&lt;sql:query&gt; SELECT * FROM PRODUCTS ORDER BY PRODUCTNAME FOR XML AUTO &lt;/sql:query&gt;</code>
              <para>
                <caps:sentence sentenceid="89594554de483809646dc64bd93b7a74" id="tgt21" class="tgtSentence">This example specifies the ASP <legacyBold>Response</legacyBold> object for the <legacyBold>Output Stream</legacyBold> property:</caps:sentence>
              </para>
              <code>adoCmd.Properties("Output Stream") = Response</code>
              <para>
                <caps:sentence sentenceid="40125ed073bd05b78e2e5aef61b8c2c8" id="tgt22" class="tgtSentence">Next, specify <legacyBold>adExecuteStream</legacyBold> parameter of <legacyBold>Execute</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="de8b95941642fa9601552a3cc514a5ed" id="tgt23" class="tgtSentence"> This example wraps the stream in XML tags to create an XML data island:</caps:sentence>
              </para>
              <code>Response.write "&lt;XML ID=MyDataIsle&gt;"
adoCmd.Execute , , adExecuteStream
Response.write "&lt;/XML&gt;"</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="46b83674d1a52e84f8c820eb64c53574" id="tgt24" class="tgtSentence">Remarks</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="e22721cfe2fbf332e2dab0849edd1686" id="tgt25" class="tgtSentence">At this point, XML has been streamed to the client browser and it is ready to be displayed.</caps:sentence>
                <caps:sentence sentenceid="8842f670f1a1946bf5c8d1831d14a74b" id="tgt26" class="tgtSentence"> This is done by using client-side VBScript to bind the XML document to an instance of the DOM and looping through each child node to build a list of Products in HTML.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Instead of receiving results in the traditional <legacyBold>Recordset</legacyBold> object, ADO can instead retrieve query results into a stream.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The ADO <legacyBold>Stream</legacyBold> object (or other objects that support the COM <legacyBold>IStream</legacyBold> interface, such as the ASP <legacyBold>Request</legacyBold> and <legacyBold>Response</legacyBold> objects) can be used to contain these results.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> One use for this feature is to retrieve results in XML format.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> With SQL Server, for example, XML results can be returned in multiple ways, such as using the FOR XML clause with a SQL SELECT query or using an XPath query.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">To receive query results in stream format instead of in a <legacyBold>Recordset</legacyBold>, you must specify the <legacyBold>adExecuteStream</legacyBold> constant from <legacyBold>ExecuteOptionEnum</legacyBold> as a parameter of the <legacyBold>Execute</legacyBold> method of a <legacyBold>Command</legacyBold> object.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> If your provider supports this feature, the results will be returned in a stream upon execution.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> You might be required to specify additional provider-specific properties before the code executes.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> For example, with the Microsoft OLE DB Provider for SQL Server, properties such as <legacyBold>Output Stream</legacyBold> in the <legacyBold>Properties</legacyBold> collection of the <legacyBold>Command</legacyBold> object must be specified.</caps:sentence>
          <caps:sentence id="src9" class="srcSentence"> For more information about SQL Server-specific dynamic properties related to this feature, see XML-Related Properties in the SQL Server Books Online.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">FOR XML Query Example</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src11" class="srcSentence">The following example is written in VBScript to the Northwind database:</caps:sentence>
          </para>
          <code>&lt;!-- BeginRecordAndStreamVBS --&gt;
&lt;%@ LANGUAGE = VBScript %&gt;
&lt;%  Option Explicit      %&gt;

&lt;HTML&gt;
&lt;HEAD&gt;
&lt;META NAME="GENERATOR" Content="Microsoft Developer Studio"/&gt;
&lt;META HTTP-EQUIV="Content-Type" content="text/html"; charset="iso-8859-1"&gt;
&lt;TITLE&gt;FOR XML Query Example&lt;/TITLE&gt;

&lt;STYLE&gt;
   BODY
   {
      FONT-FAMILY: Tahoma;
      FONT-SIZE: 8pt;
      OVERFLOW: auto
   }

   H3
   {
      FONT-FAMILY: Tahoma;
      FONT-SIZE: 8pt;
      OVERFLOW: auto
   }
&lt;/STYLE&gt;

&lt;!-- #include file="adovbs.inc" --&gt;
&lt;%
   Response.Write "&lt;H3&gt;Server-side processing&lt;/H3&gt;"

   Response.Write "Page Generated @ " &amp; Now() &amp; "&lt;BR/&gt;"

   Dim adoConn
   Set adoConn = Server.CreateObject("ADODB.Connection")

   Dim sConn
   sConn = "Provider=SQLOLEDB;Data Source=" &amp; _
      Request.ServerVariables("SERVER_NAME") &amp;amp; ";" &amp; _
      Initial Catalog=Northwind;Integrated Security=SSPI;"

   Response.write "Connect String = " &amp; sConn &amp; "&lt;BR/&gt;"

   adoConn.ConnectionString = sConn
   adoConn.CursorLocation = adUseClient

   adoConn.Open

   Response.write "ADO Version = " &amp; adoConn.Version &amp; "&lt;BR/&gt;"
   Response.write "adoConn.State = " &amp; adoConn.State &amp; "&lt;BR/&gt;"

   Dim adoCmd
   Set adoCmd = Server.CreateObject("ADODB.Command")
   Set adoCmd.ActiveConnection = adoConn

   Dim sQuery
   sQuery = "&lt;ROOT xmlns:sql='urn:schemas-microsoft-com:xml-sql'&gt;&lt;sql:query&gt;SELECT * FROM PRODUCTS WHERE ProductName='Gumbr Gummibrchen' FOR XML AUTO&lt;/sql:query&gt;&lt;/ROOT&gt;"

   Response.write "Query String = " &amp; sQuery &amp; "&lt;BR/&gt;"

   Dim adoStreamQuery
   Set adoStreamQuery = Server.CreateObject("ADODB.Stream")
   adoStreamQuery.Open
   adoStreamQuery.WriteText sQuery, adWriteChar
   adoStreamQuery.Position = 0

   adoCmd.CommandStream = adoStreamQuery
   adoCmd.Dialect = "{5D531CB2-E6Ed-11D2-B252-00C04F681B71}"

   Response.write "Pushing XML to client for processing "  &amp; "&lt;BR/&gt;"

   adoCmd.Properties("Output Stream") = Response
   Response.write "&lt;XML ID='MyDataIsle'&gt;"
   adoCmd.Execute , , 1024
   Response.write "&lt;/XML&gt;"

%&gt;

&lt;SCRIPT language="VBScript" For="window" Event="onload"&gt;
   Dim xmlDoc
   Set xmlDoc = MyDataIsle.XMLDocument
   xmlDoc.resolveExternals=false
   xmlDoc.async=false

   If xmlDoc.parseError.Reason &lt;&gt; "" then
      Msgbox "parseError.Reason = " &amp; xmlDoc.parseError.Reason
   End If
            
   Dim root, child
   Set root = xmlDoc.documentElement
   For each child in root.childNodes
      dim OutputXML
      OutputXML = document.all("log").innerHTML
      document.all("log").innerHTML = OutputXML &amp; "&lt;LI&gt;" &amp; child.getAttribute("ProductName") &amp; "&lt;/LI&gt;"
   Next
&lt;/SCRIPT&gt;

&lt;/HEAD&gt;

&lt;BODY&gt;

   &lt;H3&gt;Client-side processing of XML Document MyDataIsle&lt;/H3&gt;
   &lt;UL id=log&gt;
   &lt;/UL&gt;

&lt;/BODY&gt;
&lt;/HTML&gt;
&lt;!-- EndRecordAndStreamVBS --&gt;
</code>
          <para>
            <caps:sentence id="src12" class="srcSentence">The FOR XML clause instructs SQL Server to return data in the form of an XML document.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src13" class="srcSentence">FOR XML Syntax</caps:sentence>
            </title>
            <content>
              <code>FOR XML [RAW|AUTO|EXPLICIT]</code>
              <para>
                <caps:sentence id="src14" class="srcSentence">FOR XML RAW generates generic row elements that have column values as attributes.</caps:sentence>
                <caps:sentence id="src15" class="srcSentence"> FOR XML AUTO uses heuristics to generate a hierarchical tree with element names based on table names.</caps:sentence>
                <caps:sentence id="src16" class="srcSentence"> FOR XML EXPLICIT generates a universal table with relationships fully described by metadata.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src17" class="srcSentence">An example SQL SELECT FOR XML statement follows:</caps:sentence>
              </para>
              <code>SELECT * FROM PRODUCTS ORDER BY PRODUCTNAME FOR XML AUTO</code>
              <para>
                <caps:sentence id="src18" class="srcSentence">The command can be specified in a string as shown earlier, assigned to <legacyBold>CommandText</legacyBold>, or in the form of an XML template query assigned to <legacyBold>CommandStream</legacyBold>.</caps:sentence>
                <caps:sentence id="src19" class="srcSentence"> For more information about XML template queries, see <legacyLink xlink:href="0ac09dbe-2665-411e-8fbb-d1efe6c777be">Command Streams</legacyLink> in ADO or Using Streams for Command Input in the SQL Server Books Online.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src20" class="srcSentence">As an XML template query, the FOR XML query appears as follows:</caps:sentence>
              </para>
              <code>&lt;sql:query&gt; SELECT * FROM PRODUCTS ORDER BY PRODUCTNAME FOR XML AUTO &lt;/sql:query&gt;</code>
              <para>
                <caps:sentence id="src21" class="srcSentence">This example specifies the ASP <legacyBold>Response</legacyBold> object for the <legacyBold>Output Stream</legacyBold> property:</caps:sentence>
              </para>
              <code>adoCmd.Properties("Output Stream") = Response</code>
              <para>
                <caps:sentence id="src22" class="srcSentence">Next, specify <legacyBold>adExecuteStream</legacyBold> parameter of <legacyBold>Execute</legacyBold>.</caps:sentence>
                <caps:sentence id="src23" class="srcSentence"> This example wraps the stream in XML tags to create an XML data island:</caps:sentence>
              </para>
              <code>Response.write "&lt;XML ID=MyDataIsle&gt;"
adoCmd.Execute , , adExecuteStream
Response.write "&lt;/XML&gt;"</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src24" class="srcSentence">Remarks</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src25" class="srcSentence">At this point, XML has been streamed to the client browser and it is ready to be displayed.</caps:sentence>
                <caps:sentence id="src26" class="srcSentence"> This is done by using client-side VBScript to bind the XML document to an instance of the DOM and looping through each child node to build a list of Products in HTML.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>