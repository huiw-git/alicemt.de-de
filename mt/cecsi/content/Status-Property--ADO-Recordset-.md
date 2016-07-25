---
title: "Status Property (ADO Recordset)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 41d70d89-880f-4850-9d17-19d9790cc8eb
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
# Status Property (ADO Recordset)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="a8d20f7e3c45847b1cb4b398a83a888c" id="tgt1" class="tgtSentence">Indicates the status of the current record with respect to batch updates or other bulk operations.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="217e604856b0d798bf936945129e8393" id="tgt2" class="tgtSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6ca026ee7dc5f4221ad7374825289b92" id="tgt3" class="tgtSentence">Returns a sum of one or more <legacyLink xlink:href="506fdd70-4452-4e83-95d5-c94311988dfa">RecordStatusEnum</legacyLink> values.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="e2d687603ea1a69011e2d8a491b16d77" id="tgt4" class="tgtSentence">Use the <legacyBold>Status</legacyBold> property to see what changes are pending for records modified during batch updating.</caps:sentence>
            <caps:sentence sentenceid="800838d8da6994e80c00c3c612b78332" id="tgt5" class="tgtSentence"> You can also use the <legacyBold>Status</legacyBold> property to view the status of records that fail during bulk operations, such as when you call the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink>, <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink>, or <legacyLink xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch</legacyLink> methods on a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object, or set the <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property on a <legacyBold>Recordset</legacyBold> object to an array of bookmarks.</caps:sentence>
            <caps:sentence sentenceid="5e6e922e729737d8c466cb63e6d3f80f" id="tgt6" class="tgtSentence"> With this property, you can determine how a given record failed and resolve it accordingly.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt7" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e37b4d46-380d-4615-b4bb-e1a7b0851771">Visual Basic Example</link>
        <link xlink:href="194ce221-49bd-4474-ba34-91453d329381">Visual C++ Example</link>
        <link xlink:href="d35cb991-2c5b-4d91-bc07-62104242cae7">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the status of the current record with respect to batch updates or other bulk operations.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Return Value</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Returns a sum of one or more <legacyLink xlink:href="506fdd70-4452-4e83-95d5-c94311988dfa">RecordStatusEnum</legacyLink> values.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">Use the <legacyBold>Status</legacyBold> property to see what changes are pending for records modified during batch updating.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> You can also use the <legacyBold>Status</legacyBold> property to view the status of records that fail during bulk operations, such as when you call the <legacyLink xlink:href="73b355d4-a4c0-434b-bfc4-039b1c76b32e">Resync</legacyLink>, <legacyLink xlink:href="23f9314c-b027-4a51-aeae-50caa2977740">UpdateBatch</legacyLink>, or <legacyLink xlink:href="dbdc2574-e44e-4d95-b03d-4a5d9e9adf3c">CancelBatch</legacyLink> methods on a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object, or set the <legacyLink xlink:href="80263a7a-5d21-45d1-84fc-34b7a9be4c22">Filter</legacyLink> property on a <legacyBold>Recordset</legacyBold> object to an array of bookmarks.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> With this property, you can determine how a given record failed and resolve it accordingly.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e37b4d46-380d-4615-b4bb-e1a7b0851771">Visual Basic Example</link>
        <link xlink:href="194ce221-49bd-4474-ba34-91453d329381">Visual C++ Example</link>
        <link xlink:href="d35cb991-2c5b-4d91-bc07-62104242cae7">Visual J++ Example</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>