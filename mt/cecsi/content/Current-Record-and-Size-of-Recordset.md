---
title: "Current Record and Size of Recordset"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e63ff331-8655-4be7-82c6-e6cd6cc9d16d
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
# Current Record and Size of Recordset
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="1276c7d0a3ec30d44e6f9f15860866d8" id="tgt1" class="tgtSentence">This section describes how to locate the current position of the cursor in the sample <legacyBold>Recordset</legacyBold> in <legacyLink xlink:href="74aad8a6-06cc-4a2c-811a-d78f9b741d84">JScript Code Example to Return a Recordset</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="f4cfc297cdc203c8b373458138afa5b1" id="tgt2" class="tgtSentence">Current Record</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="3c2ac6cc17fea82ded07f4bcc5980cd0" id="tgt3" class="tgtSentence">The current record in the dataset corresponds to that pointed by the position of the cursor of the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="2ab20a86daf4a94cecbd3eccb51f226a" id="tgt4" class="tgtSentence"> When a <legacyBold>Recordset</legacyBold> object is returned from the data source as the result of calling <legacyBold>Recordset.Open</legacyBold>, <legacyBold>Command.Execute</legacyBold>, or <legacyBold>Connection.Execute</legacyBold> (including <legacyBold>Connection.NamedCommand</legacyBold> and <legacyBold>Connection.StoredProcedure</legacyBold>), the cursor is set to point at the first record.</caps:sentence>
            <caps:sentence sentenceid="f60338a5761b1469e0d4e6645cde3bf1" id="tgt5" class="tgtSentence"> In the sample dataset, the initial current record is the "Uncle Bob's Organic Dried Pears" item.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="d4fbcd9b4f010b45830980df3fb1c97b" id="tgt6" class="tgtSentence">Size of Recordset</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="2bd3a536236d403a80e7352297729f3f" id="tgt7" class="tgtSentence">To find out the size of a <legacyBold>Recordset</legacyBold> object, get the value of the <legacyBold>Recordset.RecordCount</legacyBold> property.</caps:sentence>
            <caps:sentence sentenceid="d139f2d13e4a58ab89f234b12be014c1" id="tgt8" class="tgtSentence"> This value is a long integer that indicates the number of records in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="cdeeb37002133c2e9c6d5920ce3cda52" id="tgt9" class="tgtSentence"> If the dataset is returned from the OLEDB Provider for Microsoft SQL Server, this value gives the number of rows returned.</caps:sentence>
            <caps:sentence sentenceid="af60bfd661f1112381fd3f8107c42125" id="tgt10" class="tgtSentence"> Reading the <legacyBold>RecordCount</legacyBold> property on a closed <legacyBold>Recordset</legacyBold> causes an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="28f8af3b8c0e2db5d8f4bf311e3a6165" id="tgt11" class="tgtSentence">If the number of records cannot be determined, the value of the property is –1.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="d93d20af1b7110f040eba011b62662fb" id="tgt12" class="tgtSentence">The value of the <legacyBold>RecordCount</legacyBold> property also depends on the capabilities of the provider and the type of cursor used.</caps:sentence>
            <caps:sentence sentenceid="58bdce68b601e4dbe1b34fb2982813c1" id="tgt13" class="tgtSentence"> For a forward-only cursor, the value is -1.</caps:sentence>
            <caps:sentence sentenceid="c1737568db11d8645590691c4974960a" id="tgt14" class="tgtSentence"> For a static or keyset cursor, the value is the actual number of records returned in the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="d7e39b76e947aede95559606f71becff" id="tgt15" class="tgtSentence"> For a dynamic cursor, the value is either -1 or the actual number of records, depending on the data source.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1d51fdbe6686b0fd8f2c92d933ffd67a" id="tgt16" class="tgtSentence">A cursor that supports <legacyBold>Recordcount</legacyBold> must work harder, and therefore requires more computing power, than a cursor does not support <legacyBold>Recordcount</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="71b919f002d4b2ea88695be1939435eb" id="tgt17" class="tgtSentence"> If you do not need to know the number of records, using different cursor type might help improve your application's performance, especially if you must deal with a large data set.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f12fde0647d45a4e9dfa8e17c20e0386" id="tgt18" class="tgtSentence">In some cases, a provider or cursor is unable to determine the <legacyBold>RecordCount</legacyBold> value without first fetching all records from the data source.</caps:sentence>
            <caps:sentence sentenceid="e0bcb818647c41e1d617918ca913c3ff" id="tgt19" class="tgtSentence"> To ensure accurate counting, call the <legacyBold>Recordset</legacyBold>.<legacyBold>MoveLast</legacyBold> method before calling <legacyBold>Recordset.RecordCount</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="117834635c382ac30f8fec4095922c46" id="tgt20" class="tgtSentence">The sample <legacyBold>Recordset</legacyBold> object obtained using the <legacyLink xlink:href="74aad8a6-06cc-4a2c-811a-d78f9b741d84">JScript Code Example</legacyLink> uses a forward-only cursor, so calling <legacyBold>RecordCount</legacyBold> on this object always results in –1.</caps:sentence>
            <caps:sentence sentenceid="cc920b82630533af6e4fe9e0c06d4278" id="tgt21" class="tgtSentence"> If you change the line of code that calls the <legacyBold>Recordset</legacyBold>.<legacyBold>Open</legacyBold> method as shown in the following example, the <legacyBold>RecordCount</legacyBold> property will return the actual number of records fetched.</caps:sentence>
          </para>
          <code>oRs.Open sSQL, sCnStr, adOpenStatic, adLockOptimistic, adCmdText </code>
          <para>
            <caps:sentence sentenceid="9e6fbcd73a0d93ec3709d53d48eef76b" id="tgt22" class="tgtSentence">This is because static cursors with the <legacyLink xlink:href="99bc40c4-9181-4ca1-a06f-9a1a914a0b7b">Microsoft OLE DB Provider for SQL Server</legacyLink> support <legacyBold>RecordCount</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="2b44ba10ba802cb44b3c016df7343ab3" id="tgt23" class="tgtSentence"> In this example, there are five records and thus <legacyBold>RecordCount</legacyBold> should yield the value of 5.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt24" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <para>
            <legacyLink xlink:href="c0dd4a0f-478d-4c5e-b5d5-7535f211d064">
              <caps:sentence sentenceid="8d5c643af61d878f8aecf9fa3c084c4f" id="tgt25" class="tgtSentence">Boundaries of a Recordset</caps:sentence>
            </legacyLink>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This section describes how to locate the current position of the cursor in the sample <legacyBold>Recordset</legacyBold> in <legacyLink xlink:href="74aad8a6-06cc-4a2c-811a-d78f9b741d84">JScript Code Example to Return a Recordset</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Current Record</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">The current record in the dataset corresponds to that pointed by the position of the cursor of the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> When a <legacyBold>Recordset</legacyBold> object is returned from the data source as the result of calling <legacyBold>Recordset.Open</legacyBold>, <legacyBold>Command.Execute</legacyBold>, or <legacyBold>Connection.Execute</legacyBold> (including <legacyBold>Connection.NamedCommand</legacyBold> and <legacyBold>Connection.StoredProcedure</legacyBold>), the cursor is set to point at the first record.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> In the sample dataset, the initial current record is the "Uncle Bob's Organic Dried Pears" item.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">Size of Recordset</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src7" class="srcSentence">To find out the size of a <legacyBold>Recordset</legacyBold> object, get the value of the <legacyBold>Recordset.RecordCount</legacyBold> property.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> This value is a long integer that indicates the number of records in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> If the dataset is returned from the OLEDB Provider for Microsoft SQL Server, this value gives the number of rows returned.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> Reading the <legacyBold>RecordCount</legacyBold> property on a closed <legacyBold>Recordset</legacyBold> causes an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">If the number of records cannot be determined, the value of the property is –1.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">The value of the <legacyBold>RecordCount</legacyBold> property also depends on the capabilities of the provider and the type of cursor used.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> For a forward-only cursor, the value is -1.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence"> For a static or keyset cursor, the value is the actual number of records returned in the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
            <caps:sentence id="src15" class="srcSentence"> For a dynamic cursor, the value is either -1 or the actual number of records, depending on the data source.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src16" class="srcSentence">A cursor that supports <legacyBold>Recordcount</legacyBold> must work harder, and therefore requires more computing power, than a cursor does not support <legacyBold>Recordcount</legacyBold>.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> If you do not need to know the number of records, using different cursor type might help improve your application's performance, especially if you must deal with a large data set.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src18" class="srcSentence">In some cases, a provider or cursor is unable to determine the <legacyBold>RecordCount</legacyBold> value without first fetching all records from the data source.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> To ensure accurate counting, call the <legacyBold>Recordset</legacyBold>.<legacyBold>MoveLast</legacyBold> method before calling <legacyBold>Recordset.RecordCount</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src20" class="srcSentence">The sample <legacyBold>Recordset</legacyBold> object obtained using the <legacyLink xlink:href="74aad8a6-06cc-4a2c-811a-d78f9b741d84">JScript Code Example</legacyLink> uses a forward-only cursor, so calling <legacyBold>RecordCount</legacyBold> on this object always results in –1.</caps:sentence>
            <caps:sentence id="src21" class="srcSentence"> If you change the line of code that calls the <legacyBold>Recordset</legacyBold>.<legacyBold>Open</legacyBold> method as shown in the following example, the <legacyBold>RecordCount</legacyBold> property will return the actual number of records fetched.</caps:sentence>
          </para>
          <code>oRs.Open sSQL, sCnStr, adOpenStatic, adLockOptimistic, adCmdText </code>
          <para>
            <caps:sentence id="src22" class="srcSentence">This is because static cursors with the <legacyLink xlink:href="99bc40c4-9181-4ca1-a06f-9a1a914a0b7b">Microsoft OLE DB Provider for SQL Server</legacyLink> support <legacyBold>RecordCount</legacyBold>.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> In this example, there are five records and thus <legacyBold>RecordCount</legacyBold> should yield the value of 5.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src24" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <para>
            <legacyLink xlink:href="c0dd4a0f-478d-4c5e-b5d5-7535f211d064">
              <caps:sentence id="src25" class="srcSentence">Boundaries of a Recordset</caps:sentence>
            </legacyLink>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>