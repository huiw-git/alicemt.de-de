---
title: "Fields Collection (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 7c371474-b88f-4730-afa5-44163a0488d5
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
# Fields Collection (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="470461f11aa62902a1bc13d01ced569e" id="tgt1" class="tgtSentence">Contains all the <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> objects of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> or <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="a778ca69e94e3bfd4d53e1860d154d85" id="tgt2" class="tgtSentence">A <legacyBold>Recordset</legacyBold> object has a <legacyBold>Fields</legacyBold> collection made up of <legacyBold>Field</legacyBold> objects.</caps:sentence>
            <caps:sentence sentenceid="36b4e0a1649153562210d038a5ac8329" id="tgt3" class="tgtSentence"> Each <legacyBold>Field</legacyBold> object corresponds to a column in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="69e5919e57d035dd24b160eb3335d277" id="tgt4" class="tgtSentence"> You can populate the <legacyBold>Fields</legacyBold> collection before opening the <legacyBold>Recordset</legacyBold> by calling the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method on the collection.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="b1fb434011f2b9816eba94591fddc976" id="tgt5" class="tgtSentence">See the <legacyBold>Field</legacyBold> object topic for a more detailed explanation of how to use <legacyBold>Field</legacyBold> objects.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="89c24e16eada07ff86b12a7881a65de4" id="tgt6" class="tgtSentence">The <legacyBold>Fields</legacyBold> collection has an <legacyLink xlink:href="f8a9bbed-ba9c-4698-945d-317ad22d2e92">Append</legacyLink> method, which provisionally creates and adds a <legacyBold>Field</legacyBold> object to the collection, and an <legacyBold>Update</legacyBold> method, which finalizes any additions or deletions.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="73cd163480a6ab3dfbf3104c7255ba5d" id="tgt7" class="tgtSentence">A <legacyBold>Record</legacyBold> object has two special fields that can be indexed with <legacyLink xlink:href="be4eda13-d4e4-4d6b-bb0d-3310b0a96fc2">FieldEnum</legacyLink> constants.</caps:sentence>
            <caps:sentence sentenceid="e93ea142a73b25fd968e869e18f63a1d" id="tgt8" class="tgtSentence"> One constant accesses a field containing the default stream for the <legacyBold>Record</legacyBold>, and the other accesses a field containing the absolute URL string for the <legacyBold>Record</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="81f014ab4bf3c6b1b0c663e3d29c6ba7" id="tgt9" class="tgtSentence">Certain providers (for example, the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>) may populate the <legacyBold>Fields</legacyBold> collection with a subset of available fields for the <legacyBold>Record</legacyBold> or <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="fe158be73a20b1264d460e3b23b00ac3" id="tgt10" class="tgtSentence"> Other fields will not be added to the collection until they are first referenced by name or indexed by your code.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="03a64154b5f999efbf7db016712f03e0" id="tgt11" class="tgtSentence">If you attempt to reference a nonexistent field by name, a new <legacyBold>Field</legacyBold> object will be appended to the <legacyBold>Fields</legacyBold> collection with a <legacyLink xlink:href="8cd1f7f4-0a3a-4f07-b8ba-6582e70140ad">Status</legacyLink> of <legacyBold>adFieldPendingInsert</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="d64be3c7100dc18633abc282467c55f9" id="tgt12" class="tgtSentence"> When you call <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink>, ADO will create a new field in your data source if allowed by your provider.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt13" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="8cc13e41-7ed8-40df-9a74-5bf846c14c06">
                  <caps:sentence sentenceid="9a1b3ebafc3d3272660fb80427c935fb" id="tgt14" class="tgtSentence">Fields Collection Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Contains all the <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> objects of a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> or <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">A <legacyBold>Recordset</legacyBold> object has a <legacyBold>Fields</legacyBold> collection made up of <legacyBold>Field</legacyBold> objects.</caps:sentence>
            <caps:sentence id="src3" class="srcSentence"> Each <legacyBold>Field</legacyBold> object corresponds to a column in the <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> You can populate the <legacyBold>Fields</legacyBold> collection before opening the <legacyBold>Recordset</legacyBold> by calling the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method on the collection.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src5" class="srcSentence">See the <legacyBold>Field</legacyBold> object topic for a more detailed explanation of how to use <legacyBold>Field</legacyBold> objects.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src6" class="srcSentence">The <legacyBold>Fields</legacyBold> collection has an <legacyLink xlink:href="f8a9bbed-ba9c-4698-945d-317ad22d2e92">Append</legacyLink> method, which provisionally creates and adds a <legacyBold>Field</legacyBold> object to the collection, and an <legacyBold>Update</legacyBold> method, which finalizes any additions or deletions.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">A <legacyBold>Record</legacyBold> object has two special fields that can be indexed with <legacyLink xlink:href="be4eda13-d4e4-4d6b-bb0d-3310b0a96fc2">FieldEnum</legacyLink> constants.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> One constant accesses a field containing the default stream for the <legacyBold>Record</legacyBold>, and the other accesses a field containing the absolute URL string for the <legacyBold>Record</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">Certain providers (for example, the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>) may populate the <legacyBold>Fields</legacyBold> collection with a subset of available fields for the <legacyBold>Record</legacyBold> or <legacyBold>Recordset</legacyBold>.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> Other fields will not be added to the collection until they are first referenced by name or indexed by your code.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">If you attempt to reference a nonexistent field by name, a new <legacyBold>Field</legacyBold> object will be appended to the <legacyBold>Fields</legacyBold> collection with a <legacyLink xlink:href="8cd1f7f4-0a3a-4f07-b8ba-6582e70140ad">Status</legacyLink> of <legacyBold>adFieldPendingInsert</legacyBold>.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> When you call <legacyLink xlink:href="6b2a9c31-1a7e-40db-8a53-30720d0f6cc1">Update</legacyLink>, ADO will create a new field in your data source if allowed by your provider.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src13" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="8cc13e41-7ed8-40df-9a74-5bf846c14c06">
                  <caps:sentence id="src14" class="srcSentence">Fields Collection Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>