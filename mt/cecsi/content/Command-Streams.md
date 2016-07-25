---
title: "Command Streams"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0ac09dbe-2665-411e-8fbb-d1efe6c777be
caps.latest.revision: 10
caps.handback.revision: 10
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
# Command Streams
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="ee814f8061da3ff74cea6a8d55b52b64" id="tgt1" class="tgtSentence">ADO has always supported command input in string format specified by the <legacyBold>CommandText</legacyBold> property.</caps:sentence>
          <caps:sentence sentenceid="2098432df86fc2b1353c386bf4ebf2ae" id="tgt2" class="tgtSentence"> As an alternative, with ADO 2.7 or later, you can also use a stream of information for command input by assigning the stream to the <legacyBold>CommandStream</legacyBold> property.</caps:sentence>
          <caps:sentence sentenceid="deb852a55eb48abd04cf2ba4e537198f" id="tgt3" class="tgtSentence"> You can assign an ADO <legacyBold>Stream</legacyBold> object, or any object that supports the COM <legacyBold>IStream</legacyBold> interface.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="4ffc9edac9899c06028c0c52c2b3a818" id="tgt4" class="tgtSentence">The content of the command stream is simply passed from ADO to your provider, so your provider must support command input by stream for this feature to work.</caps:sentence>
          <caps:sentence sentenceid="371fc61545c7c7770ccc61aa595f37a8" id="tgt5" class="tgtSentence"> For example, SQL Server supports queries in the form of XML templates or OpenXML extensions to Transact-SQL.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="5c5744b8441a6905e637f8cedcf4f9a1" id="tgt6" class="tgtSentence">Because the details of the stream must be interpreted by the provider, you must specify the command dialect by setting the <legacyBold>Dialect</legacyBold> property.</caps:sentence>
          <caps:sentence sentenceid="a87a37a5e15f40944a0a2682bbf6c7eb" id="tgt7" class="tgtSentence"> The value of <legacyBold>Dialect</legacyBold> is a string containing a GUID, which is defined by your provider.</caps:sentence>
          <caps:sentence sentenceid="8b3ff7951d3568815c4c0cb3840665f0" id="tgt8" class="tgtSentence"> For information about valid values for <legacyBold>Dialect</legacyBold> supported by your provider, see your provider documentation.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="4a1ae0f1865bb87d785a7de73d7ee8ef" id="tgt9" class="tgtSentence">XML Template Query Example</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="1a50986d80ecfe853d22ea81454fef43" id="tgt10" class="tgtSentence">The following example is written in VBScript to the Northwind database.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="6b502e719c10fcaf5de8db836d90cfcf" id="tgt11" class="tgtSentence">First, initialize and open the <legacyBold>Stream</legacyBold> object that will be used to contain the query stream:</caps:sentence>
          </para>
          <code>Dim adoStreamQuery
Set adoStreamQuery = Server.CreateObject("ADODB.Stream")
adoStreamQuery.Open</code>
          <para>
            <caps:sentence sentenceid="338e4bbc5c848ad59c3a4773dd624f8f" id="tgt12" class="tgtSentence">The content of the query stream will be an XML template query.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="beb874d3b963ee3eff8fb95aa7d78fe6" id="tgt13" class="tgtSentence">The template query requires a reference to the XML namespace identified by the sql: prefix of the &lt;sql:query&gt; tag.</caps:sentence>
            <caps:sentence sentenceid="d8308e37f9754a3ffe0aba4652ebb052" id="tgt14" class="tgtSentence"> A SQL SELECT statement is included as the content of the XML template and assigned to a string variable as follows:</caps:sentence>
          </para>
          <code>sQuery = "&lt;ROOT xmlns:sql='urn:schemas-microsoft-com:xml-sql'&gt;
&lt;sql:query&gt; SELECT * FROM PRODUCTS ORDER BY PRODUCTNAME &lt;/sql:query&gt;
&lt;/ROOT&gt;"</code>
          <para>
            <caps:sentence sentenceid="2fc3b14d7096db698dec78eceba304b3" id="tgt15" class="tgtSentence">Next, write the string to the stream:</caps:sentence>
          </para>
          <code>adoStreamQuery.WriteText sQuery, adWriteChar
adoStreamQuery.Position = 0</code>
          <para>
            <caps:sentence sentenceid="20fa64f244ddcec597dc4d4790eb8c5e" id="tgt16" class="tgtSentence">Assign adoStreamQuery to the <legacyBold>CommandStream</legacyBold> property of an ADO <legacyBold>Command</legacyBold> object:</caps:sentence>
          </para>
          <code>Dim adoCmd
Set adoCmd  = Server.CreateObject("ADODB.Command"")
adoCmd.CommandStream = adoStreamQuery</code>
          <para>
            <caps:sentence sentenceid="a010205addd69d57a0698ed1d4bf5967" id="tgt17" class="tgtSentence">Specify the command language <legacyBold>Dialect</legacyBold>, which indicates how the SQL Server OLE DB Provider should interpret the command stream.</caps:sentence>
            <caps:sentence sentenceid="8fa78f6f729f5c531a6f2a5ed169f447" id="tgt18" class="tgtSentence"> The dialect specified by a provider-specific GUID:</caps:sentence>
          </para>
          <code>adoCmd.Dialect = "{5D531CB2-E6Ed-11D2-B252-00C04F681B71}"</code>
          <para>
            <caps:sentence sentenceid="b5dda51b9c8a1be24c613627416e2522" id="tgt19" class="tgtSentence">Finally, execute the query and return the results to a <legacyBold>Recordset</legacyBold> object:</caps:sentence>
          </para>
          <code>Set objRS = adoCmd.Execute</code>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">ADO has always supported command input in string format specified by the <legacyBold>CommandText</legacyBold> property.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> As an alternative, with ADO 2.7 or later, you can also use a stream of information for command input by assigning the stream to the <legacyBold>CommandStream</legacyBold> property.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> You can assign an ADO <legacyBold>Stream</legacyBold> object, or any object that supports the COM <legacyBold>IStream</legacyBold> interface.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">The content of the command stream is simply passed from ADO to your provider, so your provider must support command input by stream for this feature to work.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> For example, SQL Server supports queries in the form of XML templates or OpenXML extensions to Transact-SQL.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src6" class="srcSentence">Because the details of the stream must be interpreted by the provider, you must specify the command dialect by setting the <legacyBold>Dialect</legacyBold> property.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> The value of <legacyBold>Dialect</legacyBold> is a string containing a GUID, which is defined by your provider.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> For information about valid values for <legacyBold>Dialect</legacyBold> supported by your provider, see your provider documentation.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src9" class="srcSentence">XML Template Query Example</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src10" class="srcSentence">The following example is written in VBScript to the Northwind database.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">First, initialize and open the <legacyBold>Stream</legacyBold> object that will be used to contain the query stream:</caps:sentence>
          </para>
          <code>Dim adoStreamQuery
Set adoStreamQuery = Server.CreateObject("ADODB.Stream")
adoStreamQuery.Open</code>
          <para>
            <caps:sentence id="src12" class="srcSentence">The content of the query stream will be an XML template query.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src13" class="srcSentence">The template query requires a reference to the XML namespace identified by the sql: prefix of the &lt;sql:query&gt; tag.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> A SQL SELECT statement is included as the content of the XML template and assigned to a string variable as follows:</caps:sentence>
          </para>
          <code>sQuery = "&lt;ROOT xmlns:sql='urn:schemas-microsoft-com:xml-sql'&gt;
&lt;sql:query&gt; SELECT * FROM PRODUCTS ORDER BY PRODUCTNAME &lt;/sql:query&gt;
&lt;/ROOT&gt;"</code>
          <para>
            <caps:sentence id="src15" class="srcSentence">Next, write the string to the stream:</caps:sentence>
          </para>
          <code>adoStreamQuery.WriteText sQuery, adWriteChar
adoStreamQuery.Position = 0</code>
          <para>
            <caps:sentence id="src16" class="srcSentence">Assign adoStreamQuery to the <legacyBold>CommandStream</legacyBold> property of an ADO <legacyBold>Command</legacyBold> object:</caps:sentence>
          </para>
          <code>Dim adoCmd
Set adoCmd  = Server.CreateObject("ADODB.Command"")
adoCmd.CommandStream = adoStreamQuery</code>
          <para>
            <caps:sentence id="src17" class="srcSentence">Specify the command language <legacyBold>Dialect</legacyBold>, which indicates how the SQL Server OLE DB Provider should interpret the command stream.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> The dialect specified by a provider-specific GUID:</caps:sentence>
          </para>
          <code>adoCmd.Dialect = "{5D531CB2-E6Ed-11D2-B252-00C04F681B71}"</code>
          <para>
            <caps:sentence id="src19" class="srcSentence">Finally, execute the query and return the results to a <legacyBold>Recordset</legacyBold> object:</caps:sentence>
          </para>
          <code>Set objRS = adoCmd.Execute</code>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>