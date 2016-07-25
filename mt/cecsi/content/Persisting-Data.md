---
title: "Persisting Data"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 21c162ca-2845-4dd8-a49d-e715aba8c461
caps.latest.revision: 12
caps.handback.revision: 12
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
# Persisting Data
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="7ec541cc47d003bddd912cb1afa13c77" id="tgt1" class="tgtSentence">Portable computing (for example, using laptops) has generated the need for applications that can run in both a connected and disconnected state.</caps:sentence>
          <caps:sentence sentenceid="a3e766c002273f75457235830f61673f" id="tgt2" class="tgtSentence"> ADO has added support for this by giving the developer the ability to save a client cursor <legacyBold>Recordset</legacyBold> to disk and reload it later.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="de7c2ef08d42a8728f32445024e575df" id="tgt3" class="tgtSentence">There are several scenarios in which you could use this type of feature, including the following:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="0213535636f109ac36d9d5ce2849f9c0" id="tgt4" class="tgtSentence">
                <legacyBold>Traveling:</legacyBold> When taking the application on the road, it is vital to supply the ability to make changes and add new records that can then be reconnected to the database later and committed.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="a31aec3c9ee890de9160a1b978e598c1" id="tgt5" class="tgtSentence">
                <legacyBold>Infrequently updated lookups:</legacyBold> Often in an application, tables are used as lookups—for example, state tax tables.</caps:sentence>
              <caps:sentence sentenceid="f90ef7dd6f774c013d37c9805ce7b02b" id="tgt6" class="tgtSentence"> They are infrequently updated and are read-only.</caps:sentence>
              <caps:sentence sentenceid="c9bdc2834dc66e6b6ddedf418a86b046" id="tgt7" class="tgtSentence"> Instead of rereading this data from the server each time the application is started, the application can simply load the data from a locally persisted <legacyBold>Recordset</legacyBold>.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="96f06eed05606254a5a294174deba735" id="tgt8" class="tgtSentence">In ADO, to save and load <legacyBold>Recordsets</legacyBold>, use the <legacyBold>Recordset.Save</legacyBold> and <legacyBold>Recordset.Open(,,,,adCmdFile)</legacyBold> methods on the ADO <legacyBold>Recordset</legacyBold> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="5f481a61b7cab56ca1440d51ccffa3f5" id="tgt9" class="tgtSentence">You can use the <legacyBold>Recordset</legacyBold> <legacyBold>Save</legacyBold> method to persist your ADO <legacyBold>Recordset</legacyBold> to a file on a disk.</caps:sentence>
          <caps:sentence sentenceid="d1fd1f5c1545d2b521ebad6e435d8bf2" id="tgt10" class="tgtSentence"> (You can also save a <legacyBold>Recordset</legacyBold> to an ADO <legacyBold>Stream</legacyBold> object.</caps:sentence>
          <caps:sentence sentenceid="842694dc0687fa5ecd5d0c20db9975a9" id="tgt11" class="tgtSentence">
            <legacyBold>Stream</legacyBold> objects are discussed later in the guide.)</caps:sentence>
          <caps:sentence sentenceid="73af16961d23d035a219e804fed08d3d" id="tgt12" class="tgtSentence"> Later, you can use the <legacyBold>Open</legacyBold> method to reopen the <legacyBold>Recordset</legacyBold> when you are ready to use it.</caps:sentence>
          <caps:sentence sentenceid="31a3ddcea09664f755e70124e666c04d" id="tgt13" class="tgtSentence"> By default, ADO saves the <legacyBold>Recordset</legacyBold> into the proprietary Microsoft Advanced Data TableGram (ADTG) format.</caps:sentence>
          <caps:sentence sentenceid="d90244eb8b49c0bd2cccf4733472b79c" id="tgt14" class="tgtSentence"> This binary format is specified using the <legacyBold>adPersistADTG</legacyBold> <legacyBold>PersistFormatEnum</legacyBold> value.</caps:sentence>
          <caps:sentence sentenceid="8b2b3307c5e6099bc5966ab2db8f67f6" id="tgt15" class="tgtSentence"> Alternatively, you can choose to save your <legacyBold>Recordset</legacyBold> out as XML instead using <legacyBold>adPersistXML</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="d913b0fe20b92f0da76e557aac7500a3" id="tgt16" class="tgtSentence"> For more information about saving Recordsets as XML, see <legacyLink xlink:href="f3113ec4-ae31-428f-89c6-bc1024f128ea">Persisting Records in XML Format</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="9155e97a740c29021a36cea8ce34b292" id="tgt17" class="tgtSentence">The syntax of the <legacyBold>Save</legacyBold> method is as follows:</caps:sentence>
        </para>
        <code>
        recordset.
        Save
        Destination, PersistFormat
      </code>
        <para>
          <caps:sentence sentenceid="b7a4f26c39ec1397c58b454f5b75d7f4" id="tgt18" class="tgtSentence">The first time you save the <legacyBold>Recordset</legacyBold>, it is optional to specify <legacyItalic>Destination</legacyItalic>.</caps:sentence>
          <caps:sentence sentenceid="44804666c6bc5ed10493b4aacac0feb3" id="tgt19" class="tgtSentence"> If you omit <legacyItalic>Destination</legacyItalic>, a new file will be created with a name set to the value of the <legacyLink xlink:href="a05ba2c9-2821-4343-8607-4de9b764ec91">Source</legacyLink> property of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="095f180502b911ffd453c6edc3d35c16" id="tgt20" class="tgtSentence">Omit <legacyItalic>Destination</legacyItalic> when you subsequently call <legacyBold>Save</legacyBold> after the first save or a run-time error will occur.</caps:sentence>
          <caps:sentence sentenceid="4bbe8ea404e0077f6f66fa33de61e12e" id="tgt21" class="tgtSentence"> If you subsequently call <legacyBold>Save</legacyBold> with a new <legacyItalic>Destination</legacyItalic>, the <legacyBold>Recordset</legacyBold> is saved to the new destination.</caps:sentence>
          <caps:sentence sentenceid="0eda93c474a67f72e5ac3a8167b870e3" id="tgt22" class="tgtSentence"> However, the new destination and the original destination will both be open.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="2bdec670f44d771da3118562eccdc27c" id="tgt23" class="tgtSentence">         <legacyBold>Save</legacyBold> does not close the <legacyBold>Recordset</legacyBold> or <legacyItalic>Destination</legacyItalic>, so you can continue to work with the <legacyBold>Recordset</legacyBold> and save your most recent changes.</caps:sentence>
          <caps:sentence sentenceid="199dd1af08effb5718675a6a5b9c3a8b" id="tgt24" class="tgtSentence">
            <legacyItalic>Destination</legacyItalic> remains open until the <legacyBold>Recordset</legacyBold> is closed, during which time other applications can read but not write to <legacyItalic>Destination</legacyItalic>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="aa699234cef3f01464f3a95f702a4fcf" id="tgt25" class="tgtSentence">For reasons of security, the <legacyBold>Save</legacyBold> method permits only the use of low and custom security settings from a script executed by Microsoft Internet Explorer.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="81aa94f00e75a4de7fbd4c4cc40acfa4" id="tgt26" class="tgtSentence">If the <legacyBold>Save</legacyBold> method is called while an asynchronous <legacyBold>Recordset</legacyBold> fetch, execute, or update operation is in progress, <legacyBold>Save</legacyBold> waits until the asynchronous operation is complete.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="054e595288959f8394d9cb46f621cc4f" id="tgt27" class="tgtSentence">Records are saved beginning with the first row of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="dcf57846fd56bf9fee700c653654b226" id="tgt28" class="tgtSentence"> When the <legacyBold>Save</legacyBold> method is finished, the current row position is moved to the first row of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="7d00b546d630c3e17bffb0ef69fa1426" id="tgt29" class="tgtSentence">For best results, set the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property to <legacyBold>adUseClient</legacyBold> with <legacyBold>Save</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="afd5045f9e5c1354100ecbb831500e1a" id="tgt30" class="tgtSentence"> If your provider does not support all of the functionality necessary to save <legacyBold>Recordset</legacyBold> objects, the Cursor Service will provide that functionality.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="01665ce6b9b63e3e8d78218a2473dd80" id="tgt31" class="tgtSentence">When a <legacyBold>Recordset</legacyBold> is persisted with the <legacyBold>CursorLocation</legacyBold> property set to <legacyBold>adUseServer</legacyBold>, the update capability for the <legacyBold>Recordset</legacyBold> is limited.</caps:sentence>
          <caps:sentence sentenceid="bce77cfc7b2c4d1f6776a7c823c3e6ee" id="tgt32" class="tgtSentence"> Typically, only single-table updates, insertions, and deletions are allowed (dependent on provider functionality).</caps:sentence>
          <caps:sentence sentenceid="553bdb2f81d6170ce7580dd506c16681" id="tgt33" class="tgtSentence"> The <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink> method is also unavailable in this configuration.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="e051486f3ff1092ce75f562c0cd61656" id="tgt34" class="tgtSentence">Because the <legacyItalic>Destination</legacyItalic> parameter can accept any object that supports the OLE DB <legacyBold>IStream</legacyBold> interface, you can save a <legacyBold>Recordset</legacyBold> directly to the ASP <legacyBold>Response</legacyBold> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="76184b22c4c0674eae71daa9a879a4d2" id="tgt35" class="tgtSentence">In the following example, the <legacyBold>Save</legacyBold> and <legacyBold>Open</legacyBold> methods are used to persist a <legacyBold>Recordset</legacyBold> and later reopen it:</caps:sentence>
        </para>
        <code>'BeginPersist
   conn.ConnectionString = _
   "Provider=SQLOLEDB;Data Source=MySQLServer;" _
      &amp; "Integrated Security=SSPI;Initial Catalog=pubs"
   conn.Open

   conn.Execute "create table testtable (dbkey int " &amp; _
      "primary key, field1 char(10))"
   conn.Execute "insert into testtable values (1, 'string1')"

   Set rst.ActiveConnection = conn
   rst.CursorLocation = adUseClient

   rst.Open "select * from testtable", conn, adOpenStatic, _
      adLockBatchOptimistic

   'Change the row on the client
   rst!field1 = "NewValue"

   'Save to a file--the .dat extension is an example; choose
   'your own extension. The changes will be saved in the file
   'as well as the original data.
   MyFile = Dir("c:\temp\temptbl.dat")
   If MyFile &lt;&gt; "" Then
       Kill "c:\temp\temptbl.dat"
   End If
   
   rst.Save "c:\temp\temptbl.dat", adPersistADTG
   Set rst = Nothing

   'Now reload the data from the file
   Set rst = New ADODB.Recordset
   rst.Open "c:\temp\temptbl.dat", , adOpenStatic, _
      adLockBatchOptimistic, adCmdFile

   Debug.Print "After Loading the file from disk"
   Debug.Print "   Current Edited Value: " &amp; rst!field1.Value
   Debug.Print "   Value Before Editing: " &amp; rst!field1.OriginalValue

   'Note that you can reconnect to a connection and
   'submit the changes to the data source
   Set rst.ActiveConnection = conn
   rst.UpdateBatch
'EndPersist</code>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="46b83674d1a52e84f8c820eb64c53574" id="tgt36" class="tgtSentence">Remarks</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="8bb3138ef5145ffb4733f64e5d3dd6e6" id="tgt37" class="tgtSentence">This section contains the following topics.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="1dd049c86163fa0ad65cd69738af014d" id="tgt38" class="tgtSentence">
                  <legacyLink xlink:href="a9b287f5-04b0-4514-8143-f67879ca9842">More About Recordset Persistence</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="db648c6bd7a7f7a8c4446139d81117b6" id="tgt39" class="tgtSentence">
                  <legacyLink xlink:href="d01aeb4d-4e43-450b-b3f2-0c27eaaf9f86">Persisting Filtered and Hierarchical Recordsets</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="3edb9ad224db6d36259e32902cc90e53" id="tgt40" class="tgtSentence">
                  <legacyLink xlink:href="f3113ec4-ae31-428f-89c6-bc1024f128ea">Persisting Records in XML Format</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Portable computing (for example, using laptops) has generated the need for applications that can run in both a connected and disconnected state.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> ADO has added support for this by giving the developer the ability to save a client cursor <legacyBold>Recordset</legacyBold> to disk and reload it later.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">There are several scenarios in which you could use this type of feature, including the following:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">
                <legacyBold>Traveling:</legacyBold> When taking the application on the road, it is vital to supply the ability to make changes and add new records that can then be reconnected to the database later and committed.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">
                <legacyBold>Infrequently updated lookups:</legacyBold> Often in an application, tables are used as lookups—for example, state tax tables.</caps:sentence>
              <caps:sentence id="src6" class="srcSentence"> They are infrequently updated and are read-only.</caps:sentence>
              <caps:sentence id="src7" class="srcSentence"> Instead of rereading this data from the server each time the application is started, the application can simply load the data from a locally persisted <legacyBold>Recordset</legacyBold>.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src8" class="srcSentence">In ADO, to save and load <legacyBold>Recordsets</legacyBold>, use the <legacyBold>Recordset.Save</legacyBold> and <legacyBold>Recordset.Open(,,,,adCmdFile)</legacyBold> methods on the ADO <legacyBold>Recordset</legacyBold> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src9" class="srcSentence">You can use the <legacyBold>Recordset</legacyBold> <legacyBold>Save</legacyBold> method to persist your ADO <legacyBold>Recordset</legacyBold> to a file on a disk.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> (You can also save a <legacyBold>Recordset</legacyBold> to an ADO <legacyBold>Stream</legacyBold> object.</caps:sentence>
          <caps:sentence id="src11" class="srcSentence">
            <legacyBold>Stream</legacyBold> objects are discussed later in the guide.)</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> Later, you can use the <legacyBold>Open</legacyBold> method to reopen the <legacyBold>Recordset</legacyBold> when you are ready to use it.</caps:sentence>
          <caps:sentence id="src13" class="srcSentence"> By default, ADO saves the <legacyBold>Recordset</legacyBold> into the proprietary Microsoft Advanced Data TableGram (ADTG) format.</caps:sentence>
          <caps:sentence id="src14" class="srcSentence"> This binary format is specified using the <legacyBold>adPersistADTG</legacyBold> <legacyBold>PersistFormatEnum</legacyBold> value.</caps:sentence>
          <caps:sentence id="src15" class="srcSentence"> Alternatively, you can choose to save your <legacyBold>Recordset</legacyBold> out as XML instead using <legacyBold>adPersistXML</legacyBold>.</caps:sentence>
          <caps:sentence id="src16" class="srcSentence"> For more information about saving Recordsets as XML, see <legacyLink xlink:href="f3113ec4-ae31-428f-89c6-bc1024f128ea">Persisting Records in XML Format</legacyLink>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src17" class="srcSentence">The syntax of the <legacyBold>Save</legacyBold> method is as follows:</caps:sentence>
        </para>
        <code>
        recordset.
        Save
        Destination, PersistFormat
      </code>
        <para>
          <caps:sentence id="src18" class="srcSentence">The first time you save the <legacyBold>Recordset</legacyBold>, it is optional to specify <legacyItalic>Destination</legacyItalic>.</caps:sentence>
          <caps:sentence id="src19" class="srcSentence"> If you omit <legacyItalic>Destination</legacyItalic>, a new file will be created with a name set to the value of the <legacyLink xlink:href="a05ba2c9-2821-4343-8607-4de9b764ec91">Source</legacyLink> property of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src20" class="srcSentence">Omit <legacyItalic>Destination</legacyItalic> when you subsequently call <legacyBold>Save</legacyBold> after the first save or a run-time error will occur.</caps:sentence>
          <caps:sentence id="src21" class="srcSentence"> If you subsequently call <legacyBold>Save</legacyBold> with a new <legacyItalic>Destination</legacyItalic>, the <legacyBold>Recordset</legacyBold> is saved to the new destination.</caps:sentence>
          <caps:sentence id="src22" class="srcSentence"> However, the new destination and the original destination will both be open.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src23" class="srcSentence">         <legacyBold>Save</legacyBold> does not close the <legacyBold>Recordset</legacyBold> or <legacyItalic>Destination</legacyItalic>, so you can continue to work with the <legacyBold>Recordset</legacyBold> and save your most recent changes.</caps:sentence>
          <caps:sentence id="src24" class="srcSentence">
            <legacyItalic>Destination</legacyItalic> remains open until the <legacyBold>Recordset</legacyBold> is closed, during which time other applications can read but not write to <legacyItalic>Destination</legacyItalic>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src25" class="srcSentence">For reasons of security, the <legacyBold>Save</legacyBold> method permits only the use of low and custom security settings from a script executed by Microsoft Internet Explorer.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src26" class="srcSentence">If the <legacyBold>Save</legacyBold> method is called while an asynchronous <legacyBold>Recordset</legacyBold> fetch, execute, or update operation is in progress, <legacyBold>Save</legacyBold> waits until the asynchronous operation is complete.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src27" class="srcSentence">Records are saved beginning with the first row of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src28" class="srcSentence"> When the <legacyBold>Save</legacyBold> method is finished, the current row position is moved to the first row of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src29" class="srcSentence">For best results, set the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property to <legacyBold>adUseClient</legacyBold> with <legacyBold>Save</legacyBold>.</caps:sentence>
          <caps:sentence id="src30" class="srcSentence"> If your provider does not support all of the functionality necessary to save <legacyBold>Recordset</legacyBold> objects, the Cursor Service will provide that functionality.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src31" class="srcSentence">When a <legacyBold>Recordset</legacyBold> is persisted with the <legacyBold>CursorLocation</legacyBold> property set to <legacyBold>adUseServer</legacyBold>, the update capability for the <legacyBold>Recordset</legacyBold> is limited.</caps:sentence>
          <caps:sentence id="src32" class="srcSentence"> Typically, only single-table updates, insertions, and deletions are allowed (dependent on provider functionality).</caps:sentence>
          <caps:sentence id="src33" class="srcSentence"> The <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink> method is also unavailable in this configuration.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src34" class="srcSentence">Because the <legacyItalic>Destination</legacyItalic> parameter can accept any object that supports the OLE DB <legacyBold>IStream</legacyBold> interface, you can save a <legacyBold>Recordset</legacyBold> directly to the ASP <legacyBold>Response</legacyBold> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src35" class="srcSentence">In the following example, the <legacyBold>Save</legacyBold> and <legacyBold>Open</legacyBold> methods are used to persist a <legacyBold>Recordset</legacyBold> and later reopen it:</caps:sentence>
        </para>
        <code>'BeginPersist
   conn.ConnectionString = _
   "Provider=SQLOLEDB;Data Source=MySQLServer;" _
      &amp; "Integrated Security=SSPI;Initial Catalog=pubs"
   conn.Open

   conn.Execute "create table testtable (dbkey int " &amp; _
      "primary key, field1 char(10))"
   conn.Execute "insert into testtable values (1, 'string1')"

   Set rst.ActiveConnection = conn
   rst.CursorLocation = adUseClient

   rst.Open "select * from testtable", conn, adOpenStatic, _
      adLockBatchOptimistic

   'Change the row on the client
   rst!field1 = "NewValue"

   'Save to a file--the .dat extension is an example; choose
   'your own extension. The changes will be saved in the file
   'as well as the original data.
   MyFile = Dir("c:\temp\temptbl.dat")
   If MyFile &lt;&gt; "" Then
       Kill "c:\temp\temptbl.dat"
   End If
   
   rst.Save "c:\temp\temptbl.dat", adPersistADTG
   Set rst = Nothing

   'Now reload the data from the file
   Set rst = New ADODB.Recordset
   rst.Open "c:\temp\temptbl.dat", , adOpenStatic, _
      adLockBatchOptimistic, adCmdFile

   Debug.Print "After Loading the file from disk"
   Debug.Print "   Current Edited Value: " &amp; rst!field1.Value
   Debug.Print "   Value Before Editing: " &amp; rst!field1.OriginalValue

   'Note that you can reconnect to a connection and
   'submit the changes to the data source
   Set rst.ActiveConnection = conn
   rst.UpdateBatch
'EndPersist</code>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src36" class="srcSentence">Remarks</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src37" class="srcSentence">This section contains the following topics.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src38" class="srcSentence">
                  <legacyLink xlink:href="a9b287f5-04b0-4514-8143-f67879ca9842">More About Recordset Persistence</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src39" class="srcSentence">
                  <legacyLink xlink:href="d01aeb4d-4e43-450b-b3f2-0c27eaaf9f86">Persisting Filtered and Hierarchical Recordsets</legacyLink>           </caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src40" class="srcSentence">
                  <legacyLink xlink:href="f3113ec4-ae31-428f-89c6-bc1024f128ea">Persisting Records in XML Format</legacyLink>           </caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>