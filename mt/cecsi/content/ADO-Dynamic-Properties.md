---
title: "ADO Dynamic Properties"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d7b06d72-f792-4328-93a2-5006b9e2c581
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
# ADO Dynamic Properties
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="0844bd2f8491684b3f52b3918b57a73f" id="tgt1" class="tgtSentence">Dynamic properties can be added to the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collections of the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink>, <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink>, or <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> objects.</caps:sentence>
          <caps:sentence sentenceid="2a501ee8710506218c316654bc6d78ed" id="tgt2" class="tgtSentence"> The source for these properties is either a data provider, such as the <legacyLink xlink:href="99bc40c4-9181-4ca1-a06f-9a1a914a0b7b">OLE DB Provider for SQL Server</legacyLink>, or a service provider, such as the <legacyLink xlink:href="420d0989-7cfb-4c66-a7b5-f4199d13165d">Microsoft Cursor Service for OLE DB</legacyLink>.</caps:sentence>
          <caps:sentence sentenceid="02d9b7ea9650a19487359580f58241ec" id="tgt3" class="tgtSentence"> Refer to the appropriate data provider or service provider documentation for more information about a specific dynamic property.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8d94c7d2083cd47c78b42d73a098a50e" id="tgt4" class="tgtSentence">The <legacyLink xlink:href="80d389dd-46ef-459f-b0d4-6f712fc4f32d">ADO Dynamic Property Index</legacyLink> provides a cross-reference between the ADO and OLE DB names for each standard OLE DB provider dynamic property.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="725a42d959a49b077e94ee57a2d8a765" id="tgt5" class="tgtSentence">The following dynamic properties are especially interesting, and are also documented in the sources that were mentioned earlier.</caps:sentence>
          <caps:sentence sentenceid="17e0c5ff39614f9bb95f6f954bec0eef" id="tgt6" class="tgtSentence"> Special functionality with ADO is documented in the ADO help topics in the following list.</caps:sentence>
        </para>
        <table>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="0bacd30e713df5c17da3634d67aef690" id="tgt7" class="tgtSentence">
                    <legacyLink xlink:href="a491c4ce-2b04-4c84-be83-3846bde8d16b">Optimize</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a8a2905e1fe5ad8902eed8a22bea5ce7" id="tgt8" class="tgtSentence">Specifies whether an index should be created on this field.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="d32fc847cbcd6c612da3f45ba2a42e00" id="tgt9" class="tgtSentence">
                    <legacyLink xlink:href="c4f001b5-8d16-4d39-a42e-c0e2faaaceaf">Prompt</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c28aee0644e7b026feaf244a74e5e07b" id="tgt10" class="tgtSentence">Specifies whether the OLE DB provider should prompt the user for initialization information.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="80a369b09f7368b0e6a50333eaceebe0" id="tgt11" class="tgtSentence">
                    <legacyLink xlink:href="690229d1-46cc-42e6-a57d-4438251fe248">Reshape Name</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="8a65fc124f0d53e5f74fdb1f9cc29196" id="tgt12" class="tgtSentence">Specifies a name for the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="1b098cc66df364908932560e3547a37f" id="tgt13" class="tgtSentence">
                    <legacyLink xlink:href="4e2bb601-0fe8-4d61-b00e-38341d85a6bb">Resync Command</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="0de9c53071ec0b246adadbafeaa16924" id="tgt14" class="tgtSentence">Specifies a user-supplied command string that the <legacyBold>Resync</legacyBold> method issues to refresh the data in the table named in the <legacyBold>Unique Table</legacyBold> dynamic property.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="b0931f2366439710d1e3f12180fbdb91" id="tgt15" class="tgtSentence">
                    <legacyLink xlink:href="d0e775d8-e353-46a1-ad10-ed4cc240dfaa">Unique Table, Unique Schema, Unique Catalog</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="2bebd68e789e4564e06b277fb5618e4f" id="tgt16" class="tgtSentence">
                    <legacyBold>Unique Table</legacyBold>     Specifies the name of the base table upon which updates, insertions, and deletions are allowed.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="e1fd0148a64b8d3917342fd5f1501db3" id="tgt17" class="tgtSentence">
                    <legacyBold>Unique Schema</legacyBold>     Specifies the schema, or name of the owner of the table.</caps:sentence>
                </para>
                <para>
                  <caps:sentence sentenceid="ff190dda51011628efe6225f08375381" id="tgt18" class="tgtSentence">
                    <legacyBold>Unique Catalog</legacyBold>     Specifies the catalog, or name of the database that contains the table.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="21516617a44dae542e4fbd67bb071306" id="tgt19" class="tgtSentence">
                    <legacyLink xlink:href="8a3bb608-66d7-4128-a3ef-84cb0556de0d">Update Resync</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d43cb67d591cf0a185acec08af2193a7" id="tgt20" class="tgtSentence">Specifies whether the <legacyBold>UpdateBatch</legacyBold> method is followed by an implicit <legacyBold>Resync</legacyBold> method operation, and if so, the scope of that operation.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <relatedTopics>
        <link xlink:href="bfd96a4b-c913-45aa-9e4c-ec86ac364f3a">ADO API Reference</link>
        <link xlink:href="b5e1d26d-b41d-4e35-8c7c-972426473dfb">ADO Collections</link>
        <link xlink:href="c97ed131-1a93-463c-9e61-22f029b0c474">ADO Enumerated Constants</link>
        <link xlink:href="0ce201c3-6657-4c87-ae81-0d7dc5b5a431">ADO Errors</link>
        <link xlink:href="0ded5ad9-8f83-4224-95af-38512783b972">ADO Events</link>
        <link xlink:href="a38c5670-ba28-44f3-bd5b-fcb46880e904">ADO Methods</link>
        <link xlink:href="4aca9838-1ec6-4084-bd63-dc2d17d8ab7d">ADO Object Model</link>
        <link xlink:href="d0b7e254-c89f-4406-b846-a060ef038c30">ADO Objects</link>
        <link xlink:href="0ac0d1a7-6c7a-4f4c-b115-428935e0f98b">ADO Properties</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Dynamic properties can be added to the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collections of the <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink>, <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink>, or <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> objects.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The source for these properties is either a data provider, such as the <legacyLink xlink:href="99bc40c4-9181-4ca1-a06f-9a1a914a0b7b">OLE DB Provider for SQL Server</legacyLink>, or a service provider, such as the <legacyLink xlink:href="420d0989-7cfb-4c66-a7b5-f4199d13165d">Microsoft Cursor Service for OLE DB</legacyLink>.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Refer to the appropriate data provider or service provider documentation for more information about a specific dynamic property.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">The <legacyLink xlink:href="80d389dd-46ef-459f-b0d4-6f712fc4f32d">ADO Dynamic Property Index</legacyLink> provides a cross-reference between the ADO and OLE DB names for each standard OLE DB provider dynamic property.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">The following dynamic properties are especially interesting, and are also documented in the sources that were mentioned earlier.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> Special functionality with ADO is documented in the ADO help topics in the following list.</caps:sentence>
        </para>
        <table>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">
                    <legacyLink xlink:href="a491c4ce-2b04-4c84-be83-3846bde8d16b">Optimize</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">Specifies whether an index should be created on this field.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">
                    <legacyLink xlink:href="c4f001b5-8d16-4d39-a42e-c0e2faaaceaf">Prompt</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">Specifies whether the OLE DB provider should prompt the user for initialization information.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">
                    <legacyLink xlink:href="690229d1-46cc-42e6-a57d-4438251fe248">Reshape Name</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">Specifies a name for the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">
                    <legacyLink xlink:href="4e2bb601-0fe8-4d61-b00e-38341d85a6bb">Resync Command</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">Specifies a user-supplied command string that the <legacyBold>Resync</legacyBold> method issues to refresh the data in the table named in the <legacyBold>Unique Table</legacyBold> dynamic property.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">
                    <legacyLink xlink:href="d0e775d8-e353-46a1-ad10-ed4cc240dfaa">Unique Table, Unique Schema, Unique Catalog</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">
                    <legacyBold>Unique Table</legacyBold>     Specifies the name of the base table upon which updates, insertions, and deletions are allowed.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src17" class="srcSentence">
                    <legacyBold>Unique Schema</legacyBold>     Specifies the schema, or name of the owner of the table.</caps:sentence>
                </para>
                <para>
                  <caps:sentence id="src18" class="srcSentence">
                    <legacyBold>Unique Catalog</legacyBold>     Specifies the catalog, or name of the database that contains the table.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">
                    <legacyLink xlink:href="8a3bb608-66d7-4128-a3ef-84cb0556de0d">Update Resync</legacyLink>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">Specifies whether the <legacyBold>UpdateBatch</legacyBold> method is followed by an implicit <legacyBold>Resync</legacyBold> method operation, and if so, the scope of that operation.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <relatedTopics>
        <link xlink:href="bfd96a4b-c913-45aa-9e4c-ec86ac364f3a">ADO API Reference</link>
        <link xlink:href="b5e1d26d-b41d-4e35-8c7c-972426473dfb">ADO Collections</link>
        <link xlink:href="c97ed131-1a93-463c-9e61-22f029b0c474">ADO Enumerated Constants</link>
        <link xlink:href="0ce201c3-6657-4c87-ae81-0d7dc5b5a431">ADO Errors</link>
        <link xlink:href="0ded5ad9-8f83-4224-95af-38512783b972">ADO Events</link>
        <link xlink:href="a38c5670-ba28-44f3-bd5b-fcb46880e904">ADO Methods</link>
        <link xlink:href="4aca9838-1ec6-4084-bd63-dc2d17d8ab7d">ADO Object Model</link>
        <link xlink:href="d0b7e254-c89f-4406-b846-a060ef038c30">ADO Objects</link>
        <link xlink:href="0ac0d1a7-6c7a-4f4c-b115-428935e0f98b">ADO Properties</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>