---
title: "More About Recordset Persistence"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a9b287f5-04b0-4514-8143-f67879ca9842
caps.latest.revision: 13
caps.handback.revision: 13
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
# More About Recordset Persistence
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="058a3e190e259b762b2c6aaa81e3ca07" id="tgt1" class="tgtSentence">The ADO Recordset object supports storing the contents of a <legacyBold>Recordset</legacyBold> object in a file by using its <legacyLink xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save</legacyLink> method.</caps:sentence>
          <caps:sentence sentenceid="a22080f92e577bdcb921043efabc3928" id="tgt2" class="tgtSentence"> The persistently stored file may exist on a local drive, server, or as a URL on a Web site.</caps:sentence>
          <caps:sentence sentenceid="dd12909924b1c641e31b36da76adcdfc" id="tgt3" class="tgtSentence"> Later, the file can be restored with either the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method of the <legacyBold>Recordset</legacyBold> object or the <legacyLink xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute</legacyLink> method of the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="c18b7b62e0284e49537e2d3b4552954b" id="tgt4" class="tgtSentence">In addition, the <legacyLink xlink:href="92452940-b2a7-456e-94fc-3780c71da33c">GetString</legacyLink> method converts a <legacyBold>Recordset</legacyBold> object to a form in which the columns and rows are delimited with characters you specify.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="3d1dcc6812fc6cab1eb8e16bbb0ad778" id="tgt5" class="tgtSentence">To persist a <legacyBold>Recordset</legacyBold>, begin by converting it to a form that can be stored in a file.</caps:sentence>
          <caps:sentence sentenceid="ca5365f4d34105fc44548b40c1406dac" id="tgt6" class="tgtSentence">
            <legacyBold>Recordset</legacyBold> objects can be stored in the proprietary Advanced Data TableGram (ADTG) format or the open Extensible Markup Language (XML) format.</caps:sentence>
          <caps:sentence sentenceid="924d30f32a309196171834fd51801fcf" id="tgt7" class="tgtSentence"> ADTG examples are shown in the next section.</caps:sentence>
          <caps:sentence sentenceid="e53f1dde39b1b576a8fc12b1844422b0" id="tgt8" class="tgtSentence"> For more information about XML persistence, see <legacyLink xlink:href="f3113ec4-ae31-428f-89c6-bc1024f128ea">Persisting Records in XML format</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="6967fd7668e4c651d5c9b17c23abc465" id="tgt9" class="tgtSentence">Save any pending changes in the persisted file.</caps:sentence>
          <caps:sentence sentenceid="a04691bb47da72e15cfa66056942066e" id="tgt10" class="tgtSentence"> Doing this allows you to issue a query that returns a <legacyBold>Recordset</legacyBold> object, edits the <legacyBold>Recordset</legacyBold>, saves it and the pending changes, later restores the <legacyBold>Recordset</legacyBold>, and then updates the data source with the saved pending changes.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="348e3fefa6bf42ef15c00f3b8d6f79da" id="tgt11" class="tgtSentence">For information about persistently storing <legacyBold>Stream</legacyBold> objects, see <legacyLink xlink:href="ad5bf52c-fd10-4cfa-bf7d-fcedcaa41eea">Streams and Persistence</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="7f94512f324643e7480184038fb5d72c" id="tgt12" class="tgtSentence">For an example of <legacyBold>Recordset</legacyBold> persistence, see the XML Recordset Persistence Scenario.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="1a79a4d60de6718e8e5b326e338ae533" id="tgt13" class="tgtSentence">Example</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="0d81ecb9d0fbddf8bc72f44d5a3b9d6d" id="tgt14" class="tgtSentence">Save a Recordset:</caps:sentence>
            </title>
            <content>
              <code>Dim rs as New ADODB.Recordset
rs.Save "c:\yourFile.adtg", adPersistADTG</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="efcccd2eb3221831f052b7b8b6bd9f1a" id="tgt15" class="tgtSentence">Open a persisted file with Recordset.Open:</caps:sentence>
            </title>
            <content>
              <code>Dim rs as New ADODB.Recordset
rs.Open "c:\yourFile.adtg", "Provider=MSPersist",,,adCmdFile</code>
              <para>
                <caps:sentence sentenceid="83404f81b72d8a80b68ba4ffb21eaefe" id="tgt16" class="tgtSentence">Optionally, if the <legacyBold>Recordset</legacyBold> does not have an active connection, you can accept all the defaults and code the following:</caps:sentence>
              </para>
              <code>Dim rs as New ADODB.Recordset
rs.Open "c:\yourFile.adtg"</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="98f460eb3b77e31811dec2c0420df4c7" id="tgt17" class="tgtSentence">Open a persisted file with Connection.Execute:</caps:sentence>
            </title>
            <content>
              <code>Dim conn as New ADODB.Connection
Dim rs as ADODB.Recordset
conn.Open "Provider=MSPersist"
Set rs = conn.execute("c:\yourFile.adtg")</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="6c40947b36398b66d10d6583c9cc9b8b" id="tgt18" class="tgtSentence">Open a persisted file with RDS.DataControl:</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="a563afda0f88b88889ea6fa145bcfe9c" id="tgt19" class="tgtSentence">In this case, the <legacyBold>Server</legacyBold> property is not set.</caps:sentence>
              </para>
              <code>Dim dc as New RDS.DataControl
dc.Connection = "Provider=MSPersist"
dc.SQL = "c:\yourFile.adtg"
dc.Refresh</code>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="92452940-b2a7-456e-94fc-3780c71da33c">GetString Method</link>
        <link xlink:href="e75ef0dc-2016-4fcc-8918-23311c0d4e02">Microsoft OLE DB Persistence Provider</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
        <link xlink:href="ad5bf52c-fd10-4cfa-bf7d-fcedcaa41eea">Streams and Persistence</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The ADO Recordset object supports storing the contents of a <legacyBold>Recordset</legacyBold> object in a file by using its <legacyLink xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save</legacyLink> method.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The persistently stored file may exist on a local drive, server, or as a URL on a Web site.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Later, the file can be restored with either the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method of the <legacyBold>Recordset</legacyBold> object or the <legacyLink xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute</legacyLink> method of the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">In addition, the <legacyLink xlink:href="92452940-b2a7-456e-94fc-3780c71da33c">GetString</legacyLink> method converts a <legacyBold>Recordset</legacyBold> object to a form in which the columns and rows are delimited with characters you specify.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">To persist a <legacyBold>Recordset</legacyBold>, begin by converting it to a form that can be stored in a file.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence">
            <legacyBold>Recordset</legacyBold> objects can be stored in the proprietary Advanced Data TableGram (ADTG) format or the open Extensible Markup Language (XML) format.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> ADTG examples are shown in the next section.</caps:sentence>
          <caps:sentence id="src8" class="srcSentence"> For more information about XML persistence, see <legacyLink xlink:href="f3113ec4-ae31-428f-89c6-bc1024f128ea">Persisting Records in XML format</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src9" class="srcSentence">Save any pending changes in the persisted file.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> Doing this allows you to issue a query that returns a <legacyBold>Recordset</legacyBold> object, edits the <legacyBold>Recordset</legacyBold>, saves it and the pending changes, later restores the <legacyBold>Recordset</legacyBold>, and then updates the data source with the saved pending changes.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src11" class="srcSentence">For information about persistently storing <legacyBold>Stream</legacyBold> objects, see <legacyLink xlink:href="ad5bf52c-fd10-4cfa-bf7d-fcedcaa41eea">Streams and Persistence</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src12" class="srcSentence">For an example of <legacyBold>Recordset</legacyBold> persistence, see the XML Recordset Persistence Scenario.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src13" class="srcSentence">Example</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src14" class="srcSentence">Save a Recordset:</caps:sentence>
            </title>
            <content>
              <code>Dim rs as New ADODB.Recordset
rs.Save "c:\yourFile.adtg", adPersistADTG</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src15" class="srcSentence">Open a persisted file with Recordset.Open:</caps:sentence>
            </title>
            <content>
              <code>Dim rs as New ADODB.Recordset
rs.Open "c:\yourFile.adtg", "Provider=MSPersist",,,adCmdFile</code>
              <para>
                <caps:sentence id="src16" class="srcSentence">Optionally, if the <legacyBold>Recordset</legacyBold> does not have an active connection, you can accept all the defaults and code the following:</caps:sentence>
              </para>
              <code>Dim rs as New ADODB.Recordset
rs.Open "c:\yourFile.adtg"</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src17" class="srcSentence">Open a persisted file with Connection.Execute:</caps:sentence>
            </title>
            <content>
              <code>Dim conn as New ADODB.Connection
Dim rs as ADODB.Recordset
conn.Open "Provider=MSPersist"
Set rs = conn.execute("c:\yourFile.adtg")</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src18" class="srcSentence">Open a persisted file with RDS.DataControl:</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src19" class="srcSentence">In this case, the <legacyBold>Server</legacyBold> property is not set.</caps:sentence>
              </para>
              <code>Dim dc as New RDS.DataControl
dc.Connection = "Provider=MSPersist"
dc.SQL = "c:\yourFile.adtg"
dc.Refresh</code>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="92452940-b2a7-456e-94fc-3780c71da33c">GetString Method</link>
        <link xlink:href="e75ef0dc-2016-4fcc-8918-23311c0d4e02">Microsoft OLE DB Persistence Provider</link>
        <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
        <link xlink:href="ad5bf52c-fd10-4cfa-bf7d-fcedcaa41eea">Streams and Persistence</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>