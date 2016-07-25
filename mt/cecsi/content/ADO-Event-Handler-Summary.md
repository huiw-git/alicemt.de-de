---
title: "ADO Event Handler Summary"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b34f4472-5e04-4a2c-ab64-38d6eca31a69
caps.latest.revision: 9
caps.handback.revision: 9
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
# ADO Event Handler Summary
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="ef6647816bf22c93bc52504b308641af" id="tgt1" class="tgtSentence">Two ADO objects can raise events: the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object and the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
          <caps:sentence sentenceid="79d7ad6629192048b349650e9cd8ee36" id="tgt2" class="tgtSentence"> The <legacyBold>ConnectionEvent</legacyBold> family pertains to operations on the <legacyBold>Connection</legacyBold> object, and the <legacyBold>RecordsetEvent</legacyBold> family pertains to operations on the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="3dd977526becfeda3c3fdfd3cdaa1391" id="tgt3" class="tgtSentence">             <legacyBold>Connection Events</legacyBold>: Events are issued when a transaction on a connection begins, is committed, or is rolled back; when a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> executes; when a warning occurs during a <legacyBold>Connection Event</legacyBold> operation; or when a <legacyBold>Connection</legacyBold> starts or ends.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="78abd219cbdcc6d8b4b18da90875eb78" id="tgt4" class="tgtSentence">             <legacyBold>Recordset Events</legacyBold>: Events are issued around asynchronous fetch operations as well as when you navigate through the rows of a <legacyBold>Recordset</legacyBold> object, change a field in a row of a <legacyBold>Recordset</legacyBold>, change a row in a <legacyBold>Recordset</legacyBold>, open a <legacyBold>Recordset</legacyBold> with a server-side cursor, close a <legacyBold>Recordset</legacyBold>, or make any change whatsoever in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence sentenceid="75692c8856559130f19312a30d1b222d" id="tgt5" class="tgtSentence">The following tables summarize the events and their descriptions.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="43c2180582c4118a9b4027a800e649eb" id="tgt6" class="tgtSentence">ConnectionEvent</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt7" class="tgtSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="08d9be2565b8af94da17b9692a92a571" id="tgt8" class="tgtSentence">               <legacyLink xlink:href="ec4e4b38-e9c6-4757-b2ef-4e468ae5f1d8">BeginTransComplete, CommitTransComplete, RollbackTransComplete</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="3f4e4052b3bbdefbb527dfa8916b2085" id="tgt9" class="tgtSentence">               <legacyBold>Transaction Management</legacyBold> — Notification that the current transaction on the connection has started, committed, or rolled back.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="8fb420e17e7ab1c9a5ac8dd203145433" id="tgt10" class="tgtSentence">               <legacyLink xlink:href="da561d58-eb58-446c-a4fd-1838c76073c0">WillConnect</legacyLink>, <legacyLink xlink:href="568f5252-d069-4d99-a01b-2ada87ad1304">ConnectComplete, Disconnect</legacyLink></caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="ac4c487c22cf8f90ae1204b3f85a2ff5" id="tgt11" class="tgtSentence">               <legacyBold>Connection Management</legacyBold> — Notification that the current connection will start, has started, or has ended.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="b5cc823eadbfec412ec9cbe8a9002f73" id="tgt12" class="tgtSentence">               <legacyLink xlink:href="dd755e46-f589-48a3-93a9-51ff998d44b5">WillExecute</legacyLink>, <legacyLink xlink:href="62470d42-e511-494c-bec4-ad4591734b7b">ExecuteComplete</legacyLink></caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="ea823108c27b5e836ad361e62dc34eb0" id="tgt13" class="tgtSentence">               <legacyBold>Command Execution Management</legacyBold> — Notification that the execution of the current command on the connection will start or has ended.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="89c038e95d057db9a987af039e7b8eaa" id="tgt14" class="tgtSentence">               <legacyLink xlink:href="468c87dd-e3bc-4084-9941-94d10743d4e9">InfoMessage</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="f87eb6a645ee1b940a3bb50f26893ac1" id="tgt15" class="tgtSentence">               <legacyBold>Informational</legacyBold> — Notification that there is additional information about the current operation.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="86d12022603aab3a0fb6ec7976980322" id="tgt16" class="tgtSentence">RecordsetEvent</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt17" class="tgtSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="1effc0d20f47632fb4ade6169eccace1" id="tgt18" class="tgtSentence">               <legacyLink xlink:href="301716fd-81fc-40eb-8a04-221ef7ab410e">FetchProgress</legacyLink>, <legacyLink xlink:href="a28d3858-566c-468d-b070-d1de4339fbea">FetchComplete</legacyLink></caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="894d594e11c829f0286c93e5b3810a8e" id="tgt19" class="tgtSentence">               <legacyBold>Retrieval Status</legacyBold> — Notification of the progress of a data retrieval operation, or that the retrieval operation has completed.</caps:sentence>
                  <caps:sentence sentenceid="9ed378b69515c783ae4697c01026fb68" id="tgt20" class="tgtSentence"> These events are only available if the <legacyBold>Recordset</legacyBold> was opened using a client-side cursor.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="438a886b71e1d8a1ef08eb9d29098ef0" id="tgt21" class="tgtSentence">               <legacyLink xlink:href="3e49fb89-c45b-4d39-823e-3cc887c59b37">WillChangeField, FieldChangeComplete</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="53c4ab8d9e6c02c3397c647e04eefc00" id="tgt22" class="tgtSentence">               <legacyBold>Field Change Management</legacyBold> — Notification that the value of the current field will change, or has changed.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="99a7decddca2d0ed19ba677760a3a7e0" id="tgt23" class="tgtSentence">               <legacyLink xlink:href="1a3d1042-4f30-4526-a0c7-853c242496db">WillMove, MoveComplete</legacyLink>, <legacyLink xlink:href="475de5e2-f634-4954-9edf-0027a6ba38d6">EndOfRecordset</legacyLink></caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="632641a6e49f2b5a78bcd96a3080c0d7" id="tgt24" class="tgtSentence">               <legacyBold>Navigation Management</legacyBold> — Notification that the current row position in a <legacyBold>Recordset</legacyBold> will change, has changed, or has reached the end of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="f2d42551c9508b3d906bf680ad9a3c8f" id="tgt25" class="tgtSentence">               <legacyLink xlink:href="cbc369fd-63af-4a7d-96ae-efa91b78ca69">WillChangeRecord, RecordChangeComplete</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="61b5d4fe956f1b3da5c9b48d69b1c5e9" id="tgt26" class="tgtSentence">               <legacyBold>Row Change Management</legacyBold> — Notification that something in the current row of the <legacyBold>Recordset</legacyBold> will change, or has changed.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="7fcd5d1c8d68cbd8ffe9a98994fc99b1" id="tgt27" class="tgtSentence">               <legacyLink xlink:href="d5d44659-e0d9-46d9-a297-99c43555082f">WillChangeRecordset, RecordsetChangeComplete</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="60a89c973c9e5297a4d6d2ef57ed28c9" id="tgt28" class="tgtSentence">               <legacyBold>Recordset Change Management</legacyBold> — Notification that something in the current <legacyBold>Recordset</legacyBold> will change, or has changed.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <relatedTopics>
        <link xlink:href="eded7e8c-a25f-46a6-bc2b-32d89a54d1bc">ADO Event Instantiation by Language</link>
        <link xlink:href="0ded5ad9-8f83-4224-95af-38512783b972">ADO Events</link>
        <link xlink:href="bd5c5afa-d301-4899-acda-40f98a6afa4d">Event Parameters</link>
        <link xlink:href="a86c8a02-dd69-420d-8a47-0188b339858d">How Event Handlers Work Together</link>
        <link xlink:href="f3327ea0-635a-43d4-bd78-c1674f62f1a2">Types of Events</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Two ADO objects can raise events: the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object and the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The <legacyBold>ConnectionEvent</legacyBold> family pertains to operations on the <legacyBold>Connection</legacyBold> object, and the <legacyBold>RecordsetEvent</legacyBold> family pertains to operations on the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src3" class="srcSentence">             <legacyBold>Connection Events</legacyBold>: Events are issued when a transaction on a connection begins, is committed, or is rolled back; when a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> executes; when a warning occurs during a <legacyBold>Connection Event</legacyBold> operation; or when a <legacyBold>Connection</legacyBold> starts or ends.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">             <legacyBold>Recordset Events</legacyBold>: Events are issued around asynchronous fetch operations as well as when you navigate through the rows of a <legacyBold>Recordset</legacyBold> object, change a field in a row of a <legacyBold>Recordset</legacyBold>, change a row in a <legacyBold>Recordset</legacyBold>, open a <legacyBold>Recordset</legacyBold> with a server-side cursor, close a <legacyBold>Recordset</legacyBold>, or make any change whatsoever in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            </para>
          </listItem>
        </list>
        <para>
          <caps:sentence id="src5" class="srcSentence">The following tables summarize the events and their descriptions.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">ConnectionEvent</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">               <legacyLink xlink:href="ec4e4b38-e9c6-4757-b2ef-4e468ae5f1d8">BeginTransComplete, CommitTransComplete, RollbackTransComplete</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">               <legacyBold>Transaction Management</legacyBold> — Notification that the current transaction on the connection has started, committed, or rolled back.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">               <legacyLink xlink:href="da561d58-eb58-446c-a4fd-1838c76073c0">WillConnect</legacyLink>, <legacyLink xlink:href="568f5252-d069-4d99-a01b-2ada87ad1304">ConnectComplete, Disconnect</legacyLink></caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">               <legacyBold>Connection Management</legacyBold> — Notification that the current connection will start, has started, or has ended.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">               <legacyLink xlink:href="dd755e46-f589-48a3-93a9-51ff998d44b5">WillExecute</legacyLink>, <legacyLink xlink:href="62470d42-e511-494c-bec4-ad4591734b7b">ExecuteComplete</legacyLink></caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">               <legacyBold>Command Execution Management</legacyBold> — Notification that the execution of the current command on the connection will start or has ended.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">               <legacyLink xlink:href="468c87dd-e3bc-4084-9941-94d10743d4e9">InfoMessage</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">               <legacyBold>Informational</legacyBold> — Notification that there is additional information about the current operation.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">RecordsetEvent</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src17" class="srcSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">               <legacyLink xlink:href="301716fd-81fc-40eb-8a04-221ef7ab410e">FetchProgress</legacyLink>, <legacyLink xlink:href="a28d3858-566c-468d-b070-d1de4339fbea">FetchComplete</legacyLink></caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">               <legacyBold>Retrieval Status</legacyBold> — Notification of the progress of a data retrieval operation, or that the retrieval operation has completed.</caps:sentence>
                  <caps:sentence id="src20" class="srcSentence"> These events are only available if the <legacyBold>Recordset</legacyBold> was opened using a client-side cursor.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src21" class="srcSentence">               <legacyLink xlink:href="3e49fb89-c45b-4d39-823e-3cc887c59b37">WillChangeField, FieldChangeComplete</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src22" class="srcSentence">               <legacyBold>Field Change Management</legacyBold> — Notification that the value of the current field will change, or has changed.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src23" class="srcSentence">               <legacyLink xlink:href="1a3d1042-4f30-4526-a0c7-853c242496db">WillMove, MoveComplete</legacyLink>, <legacyLink xlink:href="475de5e2-f634-4954-9edf-0027a6ba38d6">EndOfRecordset</legacyLink></caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src24" class="srcSentence">               <legacyBold>Navigation Management</legacyBold> — Notification that the current row position in a <legacyBold>Recordset</legacyBold> will change, has changed, or has reached the end of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src25" class="srcSentence">               <legacyLink xlink:href="cbc369fd-63af-4a7d-96ae-efa91b78ca69">WillChangeRecord, RecordChangeComplete</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src26" class="srcSentence">               <legacyBold>Row Change Management</legacyBold> — Notification that something in the current row of the <legacyBold>Recordset</legacyBold> will change, or has changed.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src27" class="srcSentence">               <legacyLink xlink:href="d5d44659-e0d9-46d9-a297-99c43555082f">WillChangeRecordset, RecordsetChangeComplete</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src28" class="srcSentence">               <legacyBold>Recordset Change Management</legacyBold> — Notification that something in the current <legacyBold>Recordset</legacyBold> will change, or has changed.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <relatedTopics>
        <link xlink:href="eded7e8c-a25f-46a6-bc2b-32d89a54d1bc">ADO Event Instantiation by Language</link>
        <link xlink:href="0ded5ad9-8f83-4224-95af-38512783b972">ADO Events</link>
        <link xlink:href="bd5c5afa-d301-4899-acda-40f98a6afa4d">Event Parameters</link>
        <link xlink:href="a86c8a02-dd69-420d-8a47-0188b339858d">How Event Handlers Work Together</link>
        <link xlink:href="f3327ea0-635a-43d4-bd78-c1674f62f1a2">Types of Events</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>